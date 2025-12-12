# WSDL

**WSDL (Web Services Description Language)** — это язык описания веб-сервисов на основе XML. WSDL описывает интерфейс SOAP-веб-сервиса.

### Структура WSDL-документа
- **`<types>`:** Определяет типы данных (обычно с помощью [[XSD]]).
- **`<message>`:** Описывает формат сообщений.
- **`<portType>`:** Описывает операции (методы), которые предоставляет сервис.
- **`<binding>`:** Определяет протокол и формат данных для операций.
- **`<service>`:** Определяет адрес (endpoint) сервиса.

### Назначение
WSDL служит "контрактом" между сервером и клиентом. По WSDL можно автоматически сгенерировать код клиента для вызова веб-сервиса.

### Пример использования
```xml
<definitions>
  <types>
    <schema>
      <element name="GetUserRequest">
        <complexType>
          <sequence>
            <element name="userId" type="string"/>
          </sequence>
        </complexType>
      </element>
    </schema>
  </types>
  
  <message name="GetUserInput">
    <part name="body" element="tns:GetUserRequest"/>
  </message>
  
  <portType name="UserService">
    <operation name="GetUser">
      <input message="tns:GetUserInput"/>
    </operation>
  </portType>
</definitions>

```
#### Связанные заметки:

- [[XSD]]
    
- [[SOAP]]
    
- [[REST]] (альтернативный подход)