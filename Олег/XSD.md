# XSD

**XSD (XML Schema Definition)** — это язык описания структуры XML-документа. XSD определяет, какие элементы и атрибуты могут быть в XML, их типы, порядок и ограничения.

### Основные конструкции
- **`<element>`:** Определяет элемент XML.
- **`<complexType>`:** Определяет составной тип, содержащий другие элементы или атрибуты.
- **`<simpleType>`:** Определяет простой тип (строка, число и т.д.).
- **`<sequence>`:** Элементы должны следовать в определенном порядке.
- **`<choice>`:** Должен быть выбран только один из элементов.

### Чем `sequence` отличается от `choice`?
- **`<sequence>`:** Элементы должны появляться в указанном порядке.
```xml
<xs:sequence>
  <xs:element name="firstname" type="xs:string"/>
  <xs:element name="lastname" type="xs:string"/>
</xs:sequence>
<!-- Правильно: <firstname>John</firstname><lastname>Doe</lastname> -->

- **`<choice>`:** Должен быть выбран только один из элементов.
    

xml

<xs:choice>
  <xs:element name="phone" type="xs:string"/>
  <xs:element name="email" type="xs:string"/>
</xs:choice>
<!-- Правильно: ИЛИ <phone>123</phone> ИЛИ <email>test@test.com</email> -->

### Применение

- Валидация XML-документов.
    
- Описание формата данных для веб-сервисов (SOAP).
    
- Описание конфигурационных файлов.
    

---
```


#### Связанные заметки:

- [[WSDL]]
    
- [[XML]]