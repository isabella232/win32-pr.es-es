---
title: WSDL y contratos de servicio
description: La utilidad Wsutil.exe genera un código auxiliar del lenguaje C según los metadatos WSDL proporcionados, así como definiciones y descripciones de tipos de datos para los tipos de datos descritos por esquemas XML creados por el usuario.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Compatibilidad con WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b273bd97d30aca185f35f31d385e6ab5a0bef4e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882284"
---
# <a name="wsdl-and-service-contracts"></a>WSDL y contratos de servicio

La [ utilidadWsutil.exe](web-service-compiler-tool.md) genera un código auxiliar del lenguaje C según los metadatos WSDL proporcionados, así como definiciones de tipos de datos y descripciones para los tipos de datos descritos por esquemas XML creados por el usuario.


A continuación se muestra un documento WSDL de ejemplo y un esquema XML que sirve de base para la explicación siguiente:

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

En este ejemplo se proporciona un contrato, ISimpleService, con un único método, SimpleMethod. "SimpleMethod" tiene dos parámetros de entrada de tipo **entero**, *a* y *b*, que se envían desde el cliente al servicio. Del mismo modo, SimpleMethod tiene dos parámetros de salida de tipo **entero**, *b* y *c*, que se devuelven al cliente después de completarse correctamente. En la sintaxis de C anotada con SAL, la definición del método aparece como sigue:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

En esta definición, ISimpleService es un contrato de servicio con una única operación de servicio: SimpleMethod.

El archivo de encabezado de salida contiene definiciones y descripciones para la referencia externa. Esto incluye:

-   Definiciones de estructura de C para tipos de elementos globales.
-   Prototipo de operación tal como se define en el archivo actual.
-   Prototipo de tabla de funciones para los contratos especificados en el archivo WSDL.
-   Prototipos de proxy de cliente y código auxiliar de servicio para todas las funciones especificadas en el archivo actual.
-   Estructura [**de datos WS ELEMENT \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) para los elementos de esquema global definidos en el archivo actual.
-   Estructura [**de datos \_ WS MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para todos los mensajes especificados en el archivo actual.
-   Estructura [**de datos WS CONTRACT \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para todos los contratos especificados en el archivo actual.

Se genera una estructura global para encapsular todas las descripciones globales de los tipos de esquema y los tipos de modelo de servicio a los que la aplicación puede hacer referencia. La estructura se denomina mediante un nombre de archivo normalizado. En este ejemplo, Wsutil.exe genera una estructura de definiciones globales denominada "wsdl de ejemplo" que contiene todas las \_ descripciones del servicio web. La definición de estructura se genera en el archivo de código auxiliar.

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

Para las definiciones de elementos globales en el documento de esquema XML (XSD), se genera un prototipo DE DESCRIPCIÓN DE ELEMENTO de [**WS, \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) así como la definición de tipo C correspondiente, para cada uno de los elementos. Los prototipos de las descripciones de elementos para SimpleMethod y SimpleMethodResponse se generan como miembros en la estructura anterior. Las estructuras de C se generan de la siguiente manera:

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

De forma similar para los tipos complejos globales, Wsutil.exe definiciones de estructura de tipo C como las anteriores, sin descripciones de elementos correspondientes.

Para la entrada WSDL, Wsutil.exe genera los siguientes prototipos y definiciones:

-   Se [**genera un prototipo \_ WS MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para la descripción del mensaje. El modelo de servicio y la capa de mensaje pueden usar esta descripción. Las estructuras de descripción del mensaje son campos denominados "messagename" en la estructura global. En este ejemplo, la descripción del mensaje se genera como el campo ISimpleService SimpleMethod InputMessage en la estructura \_ \_ \_ ISimpleService SimpleMethod InputMessage, tal como se especifica en el \_ archivo WSDL.
-   [**WS \_ El \_ prototipo CONTRACT DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) se genera para la descripción del contrato. El modelo de servicio usa esta descripción. Las estructuras de descripción del contrato son campos denominados "contractname" en la estructura global. En este ejemplo, la descripción del contrato se genera como el campo DefaultBinding \_ ISimpleService en la estructura \_ \_ "wsdl de ejemplo".

Las especificaciones de tipo y operación son comunes para el proxy y el código auxiliar, y se generan en ambos archivos. Wsutil.exe genera una copia solo si el proxy y el código auxiliar se generan en el mismo archivo.

## <a name="identifier-generation"></a>Generación de identificadores

Las estructuras C autogeneradas enumeradas anteriormente se crean en función del nombre especificado en el archivo WSDL. Normalmente, un NCName XML no se considera un identificador de C válido y los nombres se normalizan según sea necesario. Los valores hexadecimales no se convierten y las letras comunes como ':', '/' y '.' se convierten en el carácter de subrayado ' ' para mejorar la \_ legibilidad.

## <a name="header-for-the-stub"></a>Encabezado del código auxiliar

Para cada operación del contrato de servicio, se genera una rutina de devolución de llamada denominada &lt; "operationname &gt; Callback". (Por ejemplo, la operación "SimpleMethod" en el contrato de servicio de ejemplo tiene una devolución de llamada generada denominada "SimpleMethodCallback").

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Para cada valor **portType Wsutil.exe** WSDL genera una tabla de funciones que representa **portType**. Cada operación en **portType** tiene un puntero de función correspondiente a la devolución de llamada presente en la tabla de funciones.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Los prototipos de proxy se generan para todas las operaciones. El nombre del prototipo es el nombre de la operación (en este caso, "SimpleMethod") especificado en el archivo WSDL para el contrato de servicio.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Generación de prototipos de descripción solo local

Los archivos proxy ystub contienen la definición de la estructura de definiciones globales, incluidos prototipos y definiciones para las estructuras que contienen descripciones solo locales e implementaciones de código auxiliar de servicio o proxy de cliente.

Todos los prototipos y definiciones locales del archivo de código auxiliar se generan como parte de una estructura de encapsulación. Esta estructura de descripción local general proporciona una jerarquía clara de las descripciones requeridas por la capa de serialización y el modelo de servicio. La estructura de descripción local tiene prototipos similares a los que se muestran a continuación:

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a>Referencia a definiciones de otros archivos

Las definiciones locales pueden hacer referencia a descripciones generadas en otro archivo. Por ejemplo, el mensaje se puede definir en el archivo de código C generado a partir del archivo WSDL, pero el elemento de mensaje se puede definir en otra parte del archivo de código C generado a partir del archivo XSD. En este caso, Wsutil.exe genera una referencia al elemento global desde el archivo que contiene la definición del mensaje, como se muestra a continuación:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Descripciones de elementos globales

Para cada elemento global definido en un archivo wsdl:type o XSD, hay un campo correspondiente denominado **elementName** dentro del **campo GlobalElement.** En este ejemplo, se genera una estructura denominada SimpleMethod:

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

Otras descripciones requeridas por la descripción del elemento se generan como parte de la estructura que lo contiene. Si el elemento es un elemento de tipo simple, solo hay un campo [**WS \_ ELEMENT \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Si el tipo de elemento es una estructura, todos los campos relacionados y las descripciones de la estructura se generan como parte de la estructura del elemento. En este ejemplo, el elemento SimpleMethod es una estructura que contiene dos campos, **a** y **b**. Wsutil.exe genera la estructura de la siguiente manera:

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

Las estructuras incrustadas y los elementos incrustados se generan como subes estructuras según sea necesario.

## <a name="wsdl-related-definitions"></a>Definiciones relacionadas con WSDL

Wsutil.exe genera un campo en la sección WSDL para cada uno de los valores **portType** definidos en el wsdl:service especificado.

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

Wsutil.exe genera un campo f que contiene todas las descripciones necesarias para la operación, una matriz signle de punteros a cada una de las descripciones de la operación para cada método y un [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para el **valor de portType especificado.**

Todas las descripciones necesarias para las operaciones se generan dentro del **campo operationName** en el **valor de portType especificado.** Estos incluyen el [**campo DESCRIPCIÓN DEL ELEMENTO \_ \_ WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) así como la subes structure para los parámetros de entrada y salida s. Del mismo modo, los [**campos WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para el mensaje de entrada y el mensaje de salida opcional se incluyen junto con ; [**WS \_ Campo \_ de lista**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) PARAMETER DESCRIPTION para todos los parámetros de la operación y el campo [**WS OPERATION \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) para la propia operación. En este ejemplo, la estructura de código de la descripción simpleMethod se genera como se muestra a continuación:

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a>Definiciones relacionadas con el diccionario XML

Los nombres y espacios de nombres utilizados en varias descripciones se generan como campos de tipo [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string). Todas estas cadenas se generan como parte de un diccionario de constantes por archivo. La lista de cadenas y el campo DICCIONARIO XML de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominado **dict** en el ejemplo siguiente) se generan como parte del campo de diccionario de la **estructura fileNameLocal.**

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

La matriz de [**cadenas \_ XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)de WS se genera como una serie de campos de tipo **WS \_ XML \_ STRING,** denominados con nombres descriptivos. El código auxiliar generado usa los nombres descriptivos en varias descripciones para mejorar la legibilidad.

Proxy de cliente para operaciones WSDL

Wsutil.exe genera un proxy de cliente para todas las operaciones. Las aplicaciones pueden sobrescribir la firma del método mediante una opción de línea de comandos de prefijo.

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

El llamador de la operación debe pasar un parámetro *de montón* válido. Los parámetros de salida se asignan mediante el valor de MONTÓN de WS \_ especificado en el parámetro *del* montón. La función de llamada puede restablecer o liberar el montón para liberar memoria para todos los parámetros de salida. Si se produce un error en la operación, se puede recuperar información de error detallada adicional del objeto de error opcional si está disponible.

Wsutil.exe genera un código auxiliar de servicio para todas las operaciones descritas en enlace.

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

En la sección anterior se describe el prototipo de la estructura local que contiene todas las definiciones locales solo para el archivo de código auxiliar. En las secciones posteriores se describen las definiciones de las descripciones.

## <a name="wsdl-definition-generation"></a>Generación de definiciones wsdl

Wsutil.exe genera una estructura estática constante **(const static)** denominada<nombre de archivo *\_>* LocalDefinitions de tipo<nombre de servicio *\_>* Local que contiene todas las definiciones solo locales.

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

Se admiten las descripciones de WSDL siguientes:

-   wsdl:service
-   wsdl:binding
-   wsdl:portType
-   wsdl:operation
-   wsdl:message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Procesamiento de wsdl:operation y wsdl:message

Cada operación especificada en el documento WSDL se asigna a una operación de servicio [Wsutil.exe](web-service-compiler-tool.md). La herramienta genera definiciones independientes de las operaciones de servicio para el servidor y el cliente.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

La herramienta evalúa el diseño de los elementos de datos del mensaje de entrada y salida para generar los metadatos de serialización de la infraestructura junto con la firma real de la operación de servicio resultante a la que están asociados los mensajes de entrada y salida.

Los metadatos de cada operación dentro de un **portType** específico tienen entrada y, opcionalmente, un mensaje de salida, cada uno de estos mensajes se asigna a una descripción del [**mensaje de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). En este ejemplo, la entrada y el mensaje de salida de la operación en portType se asignan a inputMessageDescription y, opcionalmente, outputMessageDescription en [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectivamente.

Para cada mensaje WSDL, la herramienta genera [**WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) que hace referencia a la definición [**DE DESCRIPCIÓN DEL \_ ELEMENTO \_ WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) como se muestra a continuación:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

La descripción del mensaje hace referencia a la descripción del elemento de entrada. Dado que el elemento está definido globalmente, la descripción del mensaje hace referencia a la definición global en lugar del elemento estático local. De forma similar, si el elemento se define en otro archivo, Wsutil.exe genera una referencia a la estructura definida globalmente en ese archivo. Por ejemplo, si SimpleMethodResponse se define en otro archivo example.xsd, Wsutil.exe genera lo siguiente en su lugar:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Cada descripción del mensaje contiene la acción y la descripción del elemento específico (un campo de tipo [**WS \_ ELEMENT \_ DESCRIPTION)**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)para todos los elementos de datos del mensaje. En el caso de un mensaje de estilo RPC o un mensaje con varias partes, se crea un elemento contenedor para encapsular la información adicional.

## <a name="rpc-style-support"></a>Compatibilidad con el estilo RPC

Wsutil.exe admite operaciones de estilo de documento y de estilo RPC según la especificación WSDL 1.1 Binding Extension for SOAP 1.2 . Las operaciones de estilo RPC y literal se marcan como OPERACIÓN LITERAL RPC de \_ WS. \_ \_ El modelo de servicio omite el nombre del elemento contenedor del cuerpo de respuesta en las operaciones RPC/literales.

Wsutil.exe no admite de forma nativa operaciones de estilo de codificación. El parámetro WS XML BUFFER se genera para codificar mensajes y los desarrolladores \_ deben rellenar el búfer \_ opaco directamente.

## <a name="multiple-message-parts-support"></a>Compatibilidad con varias partes del mensaje

Wsutil.exe admite varias partes del mensaje en un mensaje. Se puede especificar un mensaje de varias partes de la siguiente manera:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe genera un campo [**WS \_ STRUCT \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para el elemento de mensaje si el mensaje contiene varias partes. Si el mensaje se representa mediante el estilo de documento, Wsutil.exe genera un elemento contenedor con el tipo struct. El elemento contenedor no tiene un nombre o un espacio de nombres específico, y la estructura contenedora contiene todos los elementos de todas las partes como campos. El elemento contenedor es solo para uso interno y no se serializará en el cuerpo del mensaje.

Si el mensaje usa rpc o representación de estilo literal, Wsutil.exe crea un elemento contenedor con el nombre de la operación como nombre del elemento y el espacio de nombres especificado como espacio de nombres de servicio según la especificación de extensión SOAP de WSDL. La estructura del elemento contiene una matriz de campos que representan los tipos especificados en las partes del mensaje. El elemento contenedor se asigna al elemento superior real en el cuerpo del mensaje, como se indica en la especificación SOAP.

En el lado servidor, cada operación da como resultado una definición de tipo de la operación de servicio de servidor resultante. Esta definición de tipo se usa para hacer referencia a la operación en la tabla de funciones como se describió anteriormente. Cada operación también da como resultado la generación de una función de código auxiliar a la que nfrastructure llama en nombre del delegado al método real.

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

Para la operación SimpleMethod, la definición de tipo SimpleMethodOperation se define anteriormente. Tenga en cuenta que el método generado tiene una lista de argumentos expandida con la parte del mensaje para el mensaje de entrada y salida para la operación SimpleMethod como parámetros con nombre.

En el lado cliente, cada operación se asigna a una operación de servicio de proxy.

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a>Procesar wsdl:binding

El modelo de servicio WWSAPI admite la extensión de enlace DESOAP. Para cada enlace hay un **portType asociado.**

El transporte especificado en la extensión de enlace soap solo es de asesoramiento. La aplicación debe proporcionar información de transporte al crear un canal. Actualmente se admiten los enlaces \_ WS HTTP \_ BINDING y WS \_ TCP \_ BINDING.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

En nuestro documento WSDL de ejemplo solo tenemos un **portType** para ISimpleService. El enlace SOAP proporcionado indica el transporte HTTP, que se especifica como WS \_ HTTP \_ BINDING. Tenga en cuenta que esta estructura no tiene decoración estática, ya que esta estructura debe estar disponible para la aplicación.

Procesar wsdl:portType

Cada **portType** en WSDL se conste de una o varias operaciones. La operación debe ser coherente con la extensión de enlace SOAP indicada en wsdl:binding.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

En este ejemplo, el **valor portType** de ISimpleService solo contiene la operación SimpleMethod. Esto es coherente con la sección de enlace, donde solo hay una operación WSDL que se asigna a una acción SOAP.

Puesto que ISimpleService **portType** solo tiene una operación ( SimpleMethod), la tabla de funciones correspondiente solo contiene SimpleMethod como una operación de servicio.

En términos de metadatos, **cada portType** se asigna mediante Wsutil.exe a una [**DESCRIPCIÓN DEL CONTRATO \_ \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Cada operación dentro de **un portType** se asigna a [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

En este ejemplo, **portType,** la herramienta genera [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para ISimpleService. Esta descripción del contrato contiene el número específico de operaciones disponibles en ISimpleService **portType** junto con una matriz de [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) que representa las operaciones individuales definidas en portType para ISimpleService. Puesto que solo hay una operación en ISimpleService portType para ISimpleService, también hay solo una definición **de descripción de operación \_ \_ de WS.**

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a>Procesar wsdl:service

WsUtil.exe usa los servicios para buscar binding/porttypes, y genera una estructura de contrato que describe tipos, mensajes, definiciones de tipo de puerto, y así sucesivamente. Las descripciones del contrato son accesibles externamente y se generan como parte de la estructura de definición global especificada a través del encabezado generado.

WsUtil.exe admite extensiones EndpointReference definidas en wsdl:port. La referencia de punto de conexión se define en WS-ADDRESSING como una manera de describir la información del [punto](endpoint-address.md) de conexión de un servicio. El texto de la extensión de referencia de punto de conexión de entrada guardado como [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), junto con la descripción de la dirección de punto de conexión de [**WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) coincidente se genera en la sección endpointReferences de la estructura global.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

Para crear [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mediante los metadatos generados por WsUtil:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Las cadenas constantes en el proxy de cliente o el código auxiliar de servicio se generan como campos de tipo WS XML STRING y hay un diccionario constante para todas las cadenas del proxy o archivo \_ \_ de código auxiliar. Cada cadena del diccionario se genera como un campo en la parte del diccionario de la estructura local para mejorar la legibilidad.

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a>Procesar wsdl:type

Wsutil.exe solo admite documentos de esquema XML (XSD) en la especificación wsdl:type. Un caso especial es cuando un puerto de mensaje especifica una definición de elemento global. Consulte la sección siguiente para obtener más detalles de la heurística usada en estos casos.

## <a name="parameter-processing-heuristics"></a>Heurística de procesamiento de parámetros

En el modelo de servicio, los mensajes WSDL se asignan a parámetros específicos en un método . Wsutil.exe tiene dos estilos de generación de parámetros: en primer estilo, la operación tiene un parámetro para el mensaje de entrada y un parámetro para el mensaje de salida (si es necesario); en el segundo estilo, Wsutil.exe utiliza una heurística para asignar y expandir los campos de las estructuras de los mensajes de entrada y los mensajes de salida a distintos parámetros de la operación. Los mensajes de entrada y salida deben tener elementos de mensaje de tipo estructura para generar este segundo enfoque.

Wsutil.exe las siguientes reglas al generar parámetros de operación a partir de los mensajes de entrada y salida:

-   Para los mensajes de entrada y salida con varias partes del mensaje, cada parte del mensaje es un parámetro independiente en la operación, con el nombre de la parte del mensaje como nombre del parámetro.
-   Para el mensaje de estilo RPC con una parte del mensaje, la parte del mensaje es un parámetro de la operación, con el nombre de la parte del mensaje como nombre del parámetro.
-   Para los mensajes de entrada y salida de estilo de documento con una parte del mensaje:
    -   Si el nombre de una parte del mensaje es "parameters" y el tipo de elemento es una estructura, cada campo de la estructura se trata como un parámetro independiente y el nombre del campo es el nombre del parámetro.
    -   Si el nombre de la parte del mensaje no es "parameters", el mensaje es un parámetro de la operación con el nombre del mensaje utilizado como nombre de parámetro correspondiente.
-   Para el mensaje de entrada y salida de estilo de documento con un elemento nillable, el mensaje se asigna a un parámetro, con el nombre de la parte del mensaje como nombre del parámetro. Se agrega un nivel adicional de direccionamiento indirecto para indicar que el puntero puede ser **NULL.**
-   Si solo aparece un campo en el elemento de mensaje de entrada, el campo se trata como un \[ parámetro \] in.
-   Si solo aparece un campo en el elemento de mensaje de salida, el campo se trata como un \[ parámetro \] out.
-   Si hay un campo con el mismo nombre y el mismo tipo que aparece tanto en el mensaje de entrada como en el mensaje de salida, el campo se trata como un \[ parámetro de entrada y \] salida.

Las herramientas siguientes se usan para determinar la dirección de los parámetros:

-   Si solo aparece un campo en el elemento de mensaje de entrada, el campo se trata como en solo el parámetro .
-   Si solo aparece un campo en el elemento de mensaje de salida, el campo se trata como un parámetro de solo salida.
-   Si hay un campo con el mismo nombre y el mismo tipo que aparece tanto en el mensaje de entrada como en el mensaje de salida, el campo se trata como un parámetro de entrada y salida.

Wsutil.exe solo admite elementos secuenciados. Rechaza la ordenación no válida con respecto a los parámetros de entrada y salida si Wsutil.exe los parámetros in y out en \[ una sola lista de \] parámetros. Se pueden agregar sufijos a los nombres de parámetro para evitar la colisión de nombres.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Wsutil.exe considera que los campos de tns:SimpleMethod y tns:SimpleMethodResponse son parámetros, como se muestra en las definiciones de parámetros siguientes:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

Wsutil.exe expande la lista de parámetros de los campos de la lista anterior y genera la **estructura ParamStruct** en el ejemplo de código siguiente. El modelo de servicio en tiempo de ejecución puede usar esta estructura para pasar argumentos a los códigos auxiliares de cliente y servidor.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Esta estructura solo se usa para describir el marco de pila en el lado cliente y servidor. No hay ningún cambio en la descripción del mensaje ni en las descripciones de elementos a las que hace referencia la descripción del mensaje.

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

Como regla general, se agrega un nivel de direccionamiento indirecto para todos los \[ parámetros out \] e \[ \] in,out.

## <a name="parameterless-operation"></a>Operación sin parámetros

Para las operaciones de documentos y literales, Wsutil.exe trata la operación como que tiene un parámetro de entrada y un parámetro de salida si:

-   El mensaje de entrada o salida tiene más de una parte.
-   Solo hay una parte del mensaje y el nombre de la parte del mensaje no es "parameters".

.. En el ejemplo anterior, suponiendo que las partes del mensaje se denominan *ParamIn*" y *ParamOut*, la firma del método se convierte en el código siguiente:

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

Wsutil.exe genera una firma de versión para la descripción de la operación, de modo que el motor del modelo de servicio del lado servidor y WsCall pueda comprobar si la descripción generada es aplicable a la plataforma actual.

Esta información de versión se genera como parte de la [**estructura WS \_ OPERATION \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) El número de versión se puede tratar como un selector de arm de unión para que la estructura sea extensible. Actualmente, **versionID** se establece en 1 sin campos posteriores. Las versiones futuras pueden incrementar el número de versión e incluir más campos según sea necesario. Por ejemplo, Wsutil.exe genera actualmente el código siguiente basado en el identificador de versión:

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

En el futuro, se podría expandir de la siguiente manera:

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a>Seguridad

Vea la sección de seguridad del tema [Wsutil Compiler tool](wsutil-compiler-tool.md) .

 

 




