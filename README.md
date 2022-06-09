#include<iostream>
#include<ctime>
using namespace std;
	
void main()
{
	setlocale(LC_ALL, "ru");
	srand(time(NULL));

	const int SIZE = 10;
	int arr[SIZE];
	bool AlreadyThere;

	for (int i = 0; i < SIZE;)
	{
		AlreadyThere = false;
		int NewRandomValue = rand() % 20;

		for (int j = 0; j < i; j++)
		{
			if (arr[j]==NewRandomValue)
			{
				AlreadyThere = true;
				break;
			}
		}
		if (!AlreadyThere)
		{
			arr[i] = NewRandomValue;
			i++;
		}
	}
	for (int i = 0; i < SIZE; i++)
	{
		cout << arr[i] << endl;
	}
}
