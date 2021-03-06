# **Отчёт о тестировании приложения Precision**

## Краткое описание

Протестирована работа приложения Precision, задача которого рассчёт итоговой суммы скидок для новых клиентов. На тестирование был взят исполняемый код, отвечающия за суммироавние постоянного бонуса (regularBonus) с фиксированным значением 0,3 и специального бонуса (specialBonus) с фиксированным значением 0,6:
 ```java
public class Main {
  public static void main(String[] args) {
    double regularBonus = 0.3;
    double specialBonus = 0.6;
    double totalBonus = regularBonus + specialBonus;
    System.out.println(totalBonus);
  }
}
```
На основе кода был создан проект в приложении IDEA, код отправлен на исполенение, в поле RUN получены результаты, зафиксированные в багрепорте.

## Описание тестов
Было проведено функциональное тестирование позитивным методом в рамках возможностей приложения Precision по формированию итоговый скидки для новых клиентов.

## Результаты

1. Успешных тестов - 0. Не успешных тестов - 1
2. Баг-репорт: [При суммировании скидок в размере 0,3 и 0,6 в приложении Precision получаем итоговый результат 0.89999](https://github.com/maxim-valov/Precision/issues/1)


## Общие рекомендации

По результатам тестов можно сделать вывод, что в рамках вещественного типа данных DOUBLE для точного выяесления необходимо учесть специфику вычисления бинарных чисел с плавающей запятой, в том числе в среде JAVA.

**Тестирование производилось в следующем окружении**:

* Windows 10x
* OpenJDK 11.0.10+9
* IntelliJ IDEA
