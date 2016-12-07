#include <iostream>
using namespace std;

void Sort(float massive[], int size) {
	float buf;
	for (int i=size; i>0; i--) {
		for (int j=1; j<size; j++) {
			if (massive[j-1]<massive[j]) {
				buf=massive[j-1]; massive[j-1]=massive[j]; massive[j]=buf;
			}
		}
	}
}
void BinSearch(float* massive, float key, int size) {

	int L=0;
	int R=size-1;
	while (L<=R)
	{
		int mid=(L+R)/2;
		if (key==massive[mid]) {
			cout<<"found: "<<massive[mid]<<" "<<mid; return;
		}
		
	if (int(massive[mid])>int(key))
	L=mid+1;
	if (int(massive[mid])<int(key))
	R=mid-1;
	}
	cout<<"Not found";
}	
int main() {
	int size;
	float* massive;
	cin>>size;
	massive = (float*)malloc(size * sizeof(float));
	cout<<"Input "<<size<<" elements"<<endl;
	for (int i=0; i<size; i++) {
		cin>>massive[i];
	}
	cout << endl;
	for (int i = 0; i < size; i++)
	{
		cout<< massive[i] <<" ";
	}
	cout<<endl;
	Sort(massive, size);
	cout<<"Массив отсортирован"<<endl;
	for (int i = 0; i < size; i++)
	{
		cout<< massive[i] <<" ";
	}
		cout<<endl<<"Введите число для поиска"<<endl;
		float key;
	cin>>key;
	cout<<"Идет поиск"<<endl;
	BinSearch(massive, key, size);
	if (massive[mid] != 0) 
	{cout<<"Элемент "<<massive[mid]<<" Отличен от нуля!"<<endl;}
	else
	{cout<<"Элемент "<<massive[mid]<<" Ноль!"<<endl; end; }
	return 0;
	} }
