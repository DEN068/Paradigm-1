# Paradigm-1
**Введение и основные типы парадигм**


Задача №1
**Дан список целых чисел numbers. Необходимо написать в императивном стиле процедуру для сортировки числа в списке в порядке убывания. Можно использовать любой алгоритм сортировки**


import java.util.List;

public class SortList {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(4, 2, 9, 5, 1);
        sortListImperative(numbers);
        System.out.println(numbers);
    }

    public static void sortListImperative(List<Integer> numbers) {
        int n = numbers.size();
        boolean swapped;

        do {
            swapped = false;

            for (int i = 0; i < n - 1; i++) {
                if (numbers.get(i) < numbers.get(i + 1)) {
                    int temp = numbers.get(i);
                    numbers.set(i, numbers.get(i + 1));
                    numbers.set(i + 1, temp);
                    swapped = true;
                }
            }

            n--;
        } while (swapped);
    }
}








Задача №2
**Написать точно такую же процедуру, но в декларативном стиле**


import java.util.List;
import java.util.Collections;

public class SortList {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(4, 2, 9, 5, 1);
        sortListDeclarative(numbers);
        System.out.println(numbers);
    }

    public static void sortListDeclarative(List<Integer> numbers) {
        Collections.sort(numbers, Collections.reverseOrder());
    }
}



