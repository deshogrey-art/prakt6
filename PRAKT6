#include <iostream>
using namespace std;

int main()
{
    int N;

    // Проверка количества дней
    do
    {
        cout << "Введите количество дней в месяце (1-31): ";
        cin >> N;
    }
    while (N < 1 || N > 31);

    double temperatures[31];

    // Ввод температур
    for (int i = 0; i < N; i++)
    {
        cout << "Температура за день " << i + 1 << ": ";
        cin >> temperatures[i];
    }

    // Вывод массива
    cout << "\nТемпературы за месяц: ";
    for (int i = 0; i < N; i++)
    {
        cout << temperatures[i] << " ";
    }

    // Поиск максимума, минимума, среднего и дней ниже нуля
    double maxTemp = temperatures[0];
    double minTemp = temperatures[0];
    double sum = 0;
    int belowZero = 0;

    for (int i = 0; i < N; i++)
    {
        if (temperatures[i] > maxTemp)
            maxTemp = temperatures[i];

        if (temperatures[i] < minTemp)
            minTemp = temperatures[i];

        sum += temperatures[i];

        if (temperatures[i] < 0)
            belowZero++;
    }

    cout << "\nСамая высокая температура: " << maxTemp;
    cout << "\nСамая низкая температура: " << minTemp;
    cout << "\nСредняя температура: " << sum / N;
    cout << "\nКоличество дней ниже 0: " << belowZero;

    // =========================
    // Доп. задание 1
    // =========================

    double x;
    cout << "\n\nВведите число x: ";
    cin >> x;

    int newSize = 0;

    for (int i = 0; i < N; i++)
    {
        if (temperatures[i] <= x)
        {
            temperatures[newSize] = temperatures[i];
            newSize++;
        }
    }

    N = newSize;

    cout << "Массив после удаления элементов больше " << x << ": ";
    for (int i = 0; i < N; i++)
    {
        cout << temperatures[i] << " ";
    }

    // =========================
    // Доп. задание 2
    // =========================

    if (N > 0)
    {
        int k = 1;

        for (int i = 1; i < N; i++)
        {
            if (temperatures[i] != temperatures[i - 1])
            {
                temperatures[k] = temperatures[i];
                k++;
            }
        }

        N = k;
    }

    cout << "\nМассив после удаления одинаковых подряд идущих элементов: ";
    for (int i = 0; i < N; i++)
    {
        cout << temperatures[i] << " ";
    }

    cout << endl;

    return 0;
}
