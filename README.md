Yandex handbook "JAVA Basics" answers
добавляем в финансовое приложение условные выражения яндекс практикум

public class Practicum {
    public static void main(String[] args) {
        double rateUSD = 81.9;
        double rateEUR = 87.7;
        double rateCNY = 11.49;
    
        System.out.println("Введите сумму рублей для конвертации:");
         double roubles = NumberReader.getDouble();
        /* Ввод суммы рублей для конвертации
           Сохраните введённое значение в переменную "roubles" 
         */

        System.out.println("Введите номер валюты, в какую перевести рубли:");
        System.out.println("1 – доллары;");
        System.out.println("2 – евро;");
        System.out.println("3 – юани;");
         int command = NumberReader.getInteger();
        

        /* Ввод номера команды
           Сохраните введенное значение в переменную "command" */

        if (command == 1) {
            double totalUSD = roubles / rateUSD;
            if (totalUSD <= 0) {
                System.out.println("Ошибка: некорректные значения.");
            } else {
               System.out.println("Было введено " + roubles + " в долларах это " + totalUSD);
            }
        }     
          else if (command == 2) {
            double totalEUR = roubles / rateEUR;
            if (totalEUR < 0) {
                 System.out.println("Ошибка: некорректные значения.");
            }
        System.out.println("Было введено " + roubles + ", в евро это " + totalEUR);
        }         
        else if (command == 3) {
            double totalCNY = roubles / rateCNY;
            if (totalCNY < 0) {
                 System.out.println("Ошибка: некорректные значения.");
        }
        System.out.println("Было введено " + roubles + ", в юанях это " + totalCNY);
        } else {
            System.out.println("Такой команды нет.");
        }
        
        System.out.println("Работа с программой завершена."); // Вывод сообщения о завершении работы программы
    }
}
