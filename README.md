#### Spring Context

1. Создайте класс Product (id, title, cost);
2. Создайте компонент ProductService, который хранит в себе List<Product> с 10
видами товаров. В ProductService должен быть метод вывода всех товаров в консоль printAll(),
получения ссылки на Product по имени findByTitle(String title);
3. Создайте компонент Cart (корзина) с возможностью добавления туда товаров add(Product
product);
4. Создайте компонент OrderService, позволяющий из корзины сформировать заказ. Под
формированием заказа подразумевается распечатка всех позиций в консоли, с выводом
итоговой стоимости выбранных товаров.

В ProductService у вас будет List<Product> для его заполнения не стоит использовать конструктор, как
бы мы это делали в обычном проекте. Вместо этого пропишите метод с аннотацией @PostConstruct,
который сработает после подготовки бина к работе, и в нем сделайте всю необходимую
подготовительную работу.

Продемонстрируйте работу приложения в MainApp (ввод из консоли делать не надо, использовать базу данных тоже не надо).