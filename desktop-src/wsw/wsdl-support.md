---
title: WSDL y contratos de servicio
description: La utilidad Wsutil.exe genera un código auxiliar de lenguaje C según los metadatos WSDL proporcionados, así como las definiciones de tipos de datos y las descripciones de los tipos de datos descritos por los esquemas XML creados por el usuario.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Compatibilidad con WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797278"
---
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="9f5be-106">WSDL y contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="9f5be-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="9f5be-107">La utilidad [Wsutil.exe](web-service-compiler-tool.md) genera un código auxiliar de lenguaje C según los metadatos WSDL proporcionados, así como las definiciones de tipos de datos y las descripciones de los tipos de datos descritos por los esquemas XML creados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9f5be-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="9f5be-108">A continuación se muestra un documento WSDL de ejemplo y un esquema XML que sirve como base para la explicación siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f5be-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

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

<span data-ttu-id="9f5be-109">En este ejemplo se proporciona un contrato, ISimpleService, con un único método, SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="9f5be-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="9f5be-110">"SimpleMethod" tiene dos parámetros de entrada de tipo **entero**, *a* y *b*, que se envían desde el cliente al servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="9f5be-111">Del mismo modo, SimpleMethod tiene dos parámetros de salida de tipo **entero**, *b* y *c*, que se devuelven al cliente después de la finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="9f5be-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="9f5be-112">En la sintaxis de C anotada en SAL, la definición del método aparece de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9f5be-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="9f5be-113">En esta definición, ISimpleService es un contrato de servicio con una sola operación de servicio: SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="9f5be-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="9f5be-114">El archivo de encabezado de salida contiene definiciones y descripciones para la referencia externa.</span><span class="sxs-lookup"><span data-stu-id="9f5be-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="9f5be-115">Esto incluye:</span><span class="sxs-lookup"><span data-stu-id="9f5be-115">This includes:</span></span>

-   <span data-ttu-id="9f5be-116">Definiciones de estructura de C para tipos de elementos globales.</span><span class="sxs-lookup"><span data-stu-id="9f5be-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="9f5be-117">Un prototipo de operación tal y como se define en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="9f5be-118">Un prototipo de tabla de función para los contratos especificados en el archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="9f5be-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="9f5be-119">Los prototipos de proxy de cliente y de código auxiliar de servicio para todas las funciones especificadas en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="9f5be-120">Una estructura de datos de [**\_ \_ Descripción del elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) para los elementos de esquema global definidos en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="9f5be-121">Una estructura de datos de [**\_ \_ Descripción del mensaje de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para todos los mensajes especificados en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="9f5be-122">Una estructura de datos de [**\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para todos los contratos especificados en el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="9f5be-123">Se genera una estructura global para encapsular todas las descripciones globales de los tipos de esquema y los tipos de modelo de servicio a los que puede hacer referencia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="9f5be-124">La estructura se denomina mediante un nombre de archivo normalizado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="9f5be-125">En este ejemplo, Wsutil.exe genera una estructura de definiciones global denominada "ejemplo \_ WSDL" que contiene todas las descripciones del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="9f5be-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="9f5be-126">La definición de la estructura se genera en el archivo de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9f5be-126">The structure definition is generated in the stub file.</span></span>

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

<span data-ttu-id="9f5be-127">Para las definiciones de elementos globales en el documento de esquema XML (XSD), se genera un prototipo de [**\_ \_ Descripción de elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , así como la definición de tipo C correspondiente, para cada uno de los elementos.</span><span class="sxs-lookup"><span data-stu-id="9f5be-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="9f5be-128">Los prototipos de las descripciones de elementos de SimpleMethod y SimpleMethodResponse se generan como miembros en la estructura anterior.</span><span class="sxs-lookup"><span data-stu-id="9f5be-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="9f5be-129">Las estructuras de C se generan como sigue:</span><span class="sxs-lookup"><span data-stu-id="9f5be-129">The C structures are generated as follows:</span></span>

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

<span data-ttu-id="9f5be-130">De forma similar a los tipos complejos globales, Wsutil.exe genera definiciones de estructuras de tipo C como las anteriores, sin descripciones de elementos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="9f5be-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="9f5be-131">En el caso de la entrada WSDL, Wsutil.exe genera los siguientes prototipos y definiciones:</span><span class="sxs-lookup"><span data-stu-id="9f5be-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="9f5be-132">Se genera un prototipo de [**\_ \_ Descripción de mensaje WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para la descripción del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="9f5be-133">Esta descripción puede ser utilizada por el modelo de servicio, así como por el nivel de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="9f5be-134">Las estructuras de Descripción del mensaje son campos denominados "MessageName" en la estructura global.</span><span class="sxs-lookup"><span data-stu-id="9f5be-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="9f5be-135">En este ejemplo, la descripción del mensaje se genera como el \_ campo ISimpleService SimpleMethod \_ InputMessage en la \_ estructura ISimpleService SimpleMethod \_ InputMessage, tal como se especifica en el archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="9f5be-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="9f5be-136">[**WS \_ El \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototipo de Descripción del contrato se genera para la descripción del contrato.</span><span class="sxs-lookup"><span data-stu-id="9f5be-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="9f5be-137">El modelo de servicio utiliza esta descripción.</span><span class="sxs-lookup"><span data-stu-id="9f5be-137">This description is used by service model.</span></span> <span data-ttu-id="9f5be-138">Las estructuras de Descripción del contrato son campos denominados "contractname" en la estructura global.</span><span class="sxs-lookup"><span data-stu-id="9f5be-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="9f5be-139">En este ejemplo, la descripción del contrato se genera como el \_ campo ISimpleService de DefaultBinding en la estructura " \_ example \_ WSDL".</span><span class="sxs-lookup"><span data-stu-id="9f5be-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="9f5be-140">Las especificaciones de operación y tipo son comunes al proxy y el código auxiliar, y se generan en ambos archivos.</span><span class="sxs-lookup"><span data-stu-id="9f5be-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="9f5be-141">Wsutil.exe genera una copia solo si el proxy y el código auxiliar se generan en el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="9f5be-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="9f5be-142">Generación de identificadores</span><span class="sxs-lookup"><span data-stu-id="9f5be-142">Identifier generation</span></span>

<span data-ttu-id="9f5be-143">Las estructuras de C generadas automáticamente en la lista anterior se crean según el nombre especificado en el archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="9f5be-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="9f5be-144">Un NCName XML no se considera normalmente un identificador de C válido y los nombres se normalizan según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f5be-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="9f5be-145">Los valores hexadecimales no se convierten y las letras comunes como ': ', '/' y '. ' se convierten en el carácter de subrayado ' \_ ' para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9f5be-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="9f5be-146">Encabezado del código auxiliar</span><span class="sxs-lookup"><span data-stu-id="9f5be-146">Header for the stub</span></span>

<span data-ttu-id="9f5be-147">Para cada operación del contrato de servicio, se genera una rutina de devolución de llamada denominada " <operationname> callback".</span><span class="sxs-lookup"><span data-stu-id="9f5be-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="9f5be-148">(Por ejemplo, la operación "SimpleMethod" en el contrato de servicio de ejemplo tiene una devolución de llamada generada denominada "SimpleMethodCallback").</span><span class="sxs-lookup"><span data-stu-id="9f5be-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="9f5be-149">Para cada WSDL **portType** Wsutil.exe genera una tabla de funciones que representa **portType**.</span><span class="sxs-lookup"><span data-stu-id="9f5be-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="9f5be-150">Cada operación en **portType** tiene un puntero de función correspondiente a la devolución de llamada presente en la tabla de la función.</span><span class="sxs-lookup"><span data-stu-id="9f5be-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="9f5be-151">Se generan prototipos de proxy para todas las operaciones.</span><span class="sxs-lookup"><span data-stu-id="9f5be-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="9f5be-152">El nombre del prototipo es el nombre de la operación (en este caso, "SimpleMethod") especificado en el archivo WSDL para el contrato de servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="9f5be-153">Generación de prototipos de Descripción solo local</span><span class="sxs-lookup"><span data-stu-id="9f5be-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="9f5be-154">Los archivos de andstub de proxy contienen la definición de la estructura de definiciones global, incluidos los prototipos y las definiciones de las estructuras que contienen descripciones solo de nivel local y implementaciones de código auxiliar de cliente o proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="9f5be-155">Todos los prototipos y definiciones que son locales para el archivo de código auxiliar se generan como parte de una estructura de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="9f5be-156">Esta estructura de Descripción local general proporciona una jerarquía clara de las descripciones requeridas por la capa de serialización y el modelo de servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="9f5be-157">La estructura de Descripción local tiene prototipos similares a los que se muestran a continuación:</span><span class="sxs-lookup"><span data-stu-id="9f5be-157">The local description structure has prototypes similar to the one shown below:</span></span>

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

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="9f5be-158">Referencia a definiciones de otros archivos</span><span class="sxs-lookup"><span data-stu-id="9f5be-158">Referencing definitions from other files</span></span>

<span data-ttu-id="9f5be-159">Las definiciones locales pueden hacer referencia a las descripciones generadas en otro archivo.</span><span class="sxs-lookup"><span data-stu-id="9f5be-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="9f5be-160">Por ejemplo, el mensaje se puede definir en el archivo de código C generado a partir del archivo WSDL, pero el elemento message se puede definir en otro lugar del archivo de código C generado a partir del archivo XSD.</span><span class="sxs-lookup"><span data-stu-id="9f5be-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="9f5be-161">En este caso, Wsutil.exe genera una referencia al elemento global del archivo que contiene la definición del mensaje, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="9f5be-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="9f5be-162">Descripciones de elementos globales</span><span class="sxs-lookup"><span data-stu-id="9f5be-162">Global element descriptions</span></span>

<span data-ttu-id="9f5be-163">Para cada elemento global definido en un archivo WSDL: Type o XSD, hay un campo coincidente denominado **ElementName** dentro del campo **GlobalElement** .</span><span class="sxs-lookup"><span data-stu-id="9f5be-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="9f5be-164">En este ejemplo, se genera una estructura denominada SimpleMethod:</span><span class="sxs-lookup"><span data-stu-id="9f5be-164">In this example, a structure named SimpleMethod is generated:</span></span>

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

<span data-ttu-id="9f5be-165">Se generan otras descripciones requeridas por la descripción del elemento como parte de la estructura contenedora.</span><span class="sxs-lookup"><span data-stu-id="9f5be-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="9f5be-166">Si el elemento es un elemento de tipo simple, solo hay un campo de [**\_ \_ Descripción del elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) .</span><span class="sxs-lookup"><span data-stu-id="9f5be-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="9f5be-167">Si el tipo de elemento es una estructura, todos los campos relacionados y las descripciones de estructura se generan como parte de la estructura del elemento.</span><span class="sxs-lookup"><span data-stu-id="9f5be-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="9f5be-168">En este ejemplo, el elemento SimpleMethod es una estructura que contiene dos campos, **a** y **b**.</span><span class="sxs-lookup"><span data-stu-id="9f5be-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="9f5be-169">Wsutil.exe genera la estructura de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9f5be-169">Wsutil.exe generates the structure as follows:</span></span>

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

<span data-ttu-id="9f5be-170">Las estructuras incrustadas y los elementos incrustados se generan como subestructuras según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f5be-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="9f5be-171">Definiciones relacionadas con WSDL</span><span class="sxs-lookup"><span data-stu-id="9f5be-171">WSDL related definitions</span></span>

<span data-ttu-id="9f5be-172">Wsutil.exe genera un campo en la sección WSDL para cada uno de los valores de **portType** definidos en el WSDL: Service especificado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

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

<span data-ttu-id="9f5be-173">Wsutil.exe genera un campo f que contiene todas las descripciones necesarias para la operación, una matriz inicio de punteros a cada una de las descripciones de la operación de cada método y una [**\_ \_ Descripción del contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para el **portType** especificado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="9f5be-174">Todas las descripciones necesarias para las operaciones se generan dentro del campo **OperationName** en el **portType** especificado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="9f5be-175">Incluyen el campo [**de \_ \_ Descripción del elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , así como la subestructura para los parámetros de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="9f5be-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="9f5be-176">Del mismo modo, los campos de [**\_ \_ Descripción del mensaje WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para el mensaje de entrada y el mensaje de salida opcional se incluyen junto con el; [**WS \_ Campo \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) de lista de descripción de parámetros para todos los parámetros de operación y el campo de descripción de la [**\_ \_ operación WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) para la propia operación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="9f5be-177">En este ejemplo, la estructura de código para la descripción de SimpleMethod se genera como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="9f5be-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

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

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="9f5be-178">Definiciones relacionadas con el Diccionario XML</span><span class="sxs-lookup"><span data-stu-id="9f5be-178">XML dictionary related definitions</span></span>

<span data-ttu-id="9f5be-179">Los nombres y los espacios de nombres utilizados en varias descripciones se generan como campos de tipo [**\_ \_ cadena XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span><span class="sxs-lookup"><span data-stu-id="9f5be-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="9f5be-180">Todas estas cadenas se generan como parte de un diccionario de constantes por archivo.</span><span class="sxs-lookup"><span data-stu-id="9f5be-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="9f5be-181">La lista de cadenas y el campo del [**\_ \_ Diccionario XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominado **dict** en el ejemplo siguiente) se generan como parte del campo Dictionary de la estructura **fileNameLocal** .</span><span class="sxs-lookup"><span data-stu-id="9f5be-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

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

<span data-ttu-id="9f5be-182">La matriz de [**\_ \_ cadenas XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)se genera como una serie de campos de tipo **WS \_ XML \_ String**, denominados con nombres descriptivos.</span><span class="sxs-lookup"><span data-stu-id="9f5be-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="9f5be-183">El código auxiliar generado usa los nombres descriptivos en varias descripciones para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9f5be-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="9f5be-184">Proxy de cliente para las operaciones de WSDL</span><span class="sxs-lookup"><span data-stu-id="9f5be-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="9f5be-185">Wsutil.exe genera un proxy de cliente para todas las operaciones.</span><span class="sxs-lookup"><span data-stu-id="9f5be-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="9f5be-186">Las aplicaciones pueden sobrescribir la firma del método mediante una opción de línea de comandos de prefijo.</span><span class="sxs-lookup"><span data-stu-id="9f5be-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

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

<span data-ttu-id="9f5be-187">El autor de la llamada de operación debe pasar un parámetro de *montón* válido.</span><span class="sxs-lookup"><span data-stu-id="9f5be-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="9f5be-188">Los parámetros de salida se asignan mediante el \_ valor del montón WS especificado en el parámetro *heap* .</span><span class="sxs-lookup"><span data-stu-id="9f5be-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="9f5be-189">La función de llamada puede restablecer o liberar el montón para liberar memoria para todos los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="9f5be-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="9f5be-190">Si se produce un error en la operación, se puede recuperar información de error de detalle adicional del objeto de error opcional si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9f5be-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="9f5be-191">Wsutil.exe genera un código auxiliar de servicio para todas las operaciones que se describen en Binding.</span><span class="sxs-lookup"><span data-stu-id="9f5be-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

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

<span data-ttu-id="9f5be-192">En la sección anterior se describe el prototipo de la estructura local que contiene todas las definiciones locales solo para el archivo de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9f5be-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="9f5be-193">En las secciones siguientes se describen las definiciones de las descripciones.</span><span class="sxs-lookup"><span data-stu-id="9f5be-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="9f5be-194">Generación de definiciones WSDL</span><span class="sxs-lookup"><span data-stu-id="9f5be-194">WSDL Definition Generation</span></span>

<span data-ttu-id="9f5be-195">Wsutil.exe genera una estructura estática constante (**const static**) denominada *<\_ nombre de archivo>* LocalDefinitions del tipo *<\_ nombre del servicio>* local que contiene todas las definiciones solo locales.</span><span class="sxs-lookup"><span data-stu-id="9f5be-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

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

<span data-ttu-id="9f5be-196">Se admiten las siguientes descripciones de WSDL:</span><span class="sxs-lookup"><span data-stu-id="9f5be-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="9f5be-197">WSDL: servicio</span><span class="sxs-lookup"><span data-stu-id="9f5be-197">wsdl:service</span></span>
-   <span data-ttu-id="9f5be-198">WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="9f5be-198">wsdl:binding</span></span>
-   <span data-ttu-id="9f5be-199">WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="9f5be-199">wsdl:portType</span></span>
-   <span data-ttu-id="9f5be-200">WSDL: Operation</span><span class="sxs-lookup"><span data-stu-id="9f5be-200">wsdl:operation</span></span>
-   <span data-ttu-id="9f5be-201">WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="9f5be-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="9f5be-202">Procesando WSDL: Operation y WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="9f5be-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="9f5be-203">Cada operación especificada en el documento WSDL se asigna a una operación de servicio mediante [Wsutil.exe](web-service-compiler-tool.md).</span><span class="sxs-lookup"><span data-stu-id="9f5be-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="9f5be-204">La herramienta genera definiciones independientes de las operaciones de servicio para el servidor y el cliente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

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

<span data-ttu-id="9f5be-205">La herramienta evalúa el diseño de los elementos de datos de mensajes de andOutput de entrada para generar los metadatos de serialización para la infraestructura junto con la firma real de la operación de servicio resultante a la que se asocian los mensajes de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="9f5be-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="9f5be-206">Los metadatos de cada operación dentro de un **portType** específico tienen entrada y, opcionalmente, un mensaje de salida, cada uno de estos mensajes se asigna a una [**\_ \_ Descripción del mensaje de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span><span class="sxs-lookup"><span data-stu-id="9f5be-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="9f5be-207">En este ejemplo, la entrada y el mensaje de salida de la operación en el portType se asignan a inputMessageDescription y, opcionalmente, el outputMessageDescription en la [**\_ \_ Descripción**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) de la operación de WS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="9f5be-208">Para cada mensaje WSDL, la herramienta genera una [**\_ \_ Descripción del mensaje de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) que hace referencia a la definición de la [**\_ \_ Descripción del elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="9f5be-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="9f5be-209">La descripción del mensaje hace referencia a la descripción del elemento de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f5be-209">The message description refers to the input element description.</span></span> <span data-ttu-id="9f5be-210">Dado que el elemento está definido globalmente, la descripción del mensaje hace referencia a la definición global en lugar del elemento estático local.</span><span class="sxs-lookup"><span data-stu-id="9f5be-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="9f5be-211">Del mismo modo, si el elemento se define en otro archivo, Wsutil.exe genera una referencia a la estructura definida globalmente en ese archivo.</span><span class="sxs-lookup"><span data-stu-id="9f5be-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="9f5be-212">Por ejemplo, si SimpleMethodResponse se define en otro archivo. xsd de ejemplo, Wsutil.exe genera lo siguiente en su lugar:</span><span class="sxs-lookup"><span data-stu-id="9f5be-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="9f5be-213">Cada descripción del mensaje contiene la acción y la descripción del elemento específico (un campo de tipo [**WS \_ Element \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) para todos los elementos de datos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="9f5be-214">En el caso de un mensaje de estilo RPC o un mensaje con varias partes, se crea un elemento contenedor para encapsular la información adicional.</span><span class="sxs-lookup"><span data-stu-id="9f5be-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="9f5be-215">Compatibilidad con el estilo RPC</span><span class="sxs-lookup"><span data-stu-id="9f5be-215">RPC style support</span></span>

<span data-ttu-id="9f5be-216">Wsutil.exe admite las operaciones de estilo de documento y de estilo RPC según la extensión de enlace de WSDL 1,1 para la especificación de SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="9f5be-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="9f5be-217">Las operaciones de estilo RPC y literal se marcan como \_ una \_ operación literal WS RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="9f5be-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="9f5be-218">El modelo de servicio omite el nombre del elemento contenedor del cuerpo de respuesta en operaciones RPC/literal.</span><span class="sxs-lookup"><span data-stu-id="9f5be-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="9f5be-219">Wsutil.exe no admite de forma nativa operaciones de estilo de codificación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="9f5be-220">El \_ \_ parámetro de búfer de WS XML se genera para los mensajes de codificación y los desarrolladores deben rellenar el búfer opaco directamente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="9f5be-221">Compatibilidad con varias partes de mensaje</span><span class="sxs-lookup"><span data-stu-id="9f5be-221">Multiple message parts support</span></span>

<span data-ttu-id="9f5be-222">Wsutil.exe admite varias partes de mensaje en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="9f5be-223">Se puede especificar un mensaje de varias partes como se indica A continuación:</span><span class="sxs-lookup"><span data-stu-id="9f5be-223">A multi-part message can be specified as follows:</span></span>

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

<span data-ttu-id="9f5be-224">Wsutil.exe genera un campo de [**\_ \_ tipo de struct de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para el elemento de mensaje si el mensaje contiene varias partes.</span><span class="sxs-lookup"><span data-stu-id="9f5be-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="9f5be-225">Si el mensaje se representa utilizando el estilo de documento, Wsutil.exe genera un elemento contenedor con un tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="9f5be-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="9f5be-226">El elemento contenedor no tiene un nombre o un espacio de nombres específico y la estructura del contenedor contiene todos los elementos de todos los elementos como campos.</span><span class="sxs-lookup"><span data-stu-id="9f5be-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="9f5be-227">El elemento contenedor es solo para uso interno y no se serializará en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="9f5be-228">Si el mensaje usa la representación de estilo RPC o literal, Wsutil.exe crea un elemento contenedor con el nombre de la operación como el nombre del elemento y el espacio de nombres especificado como espacio de nombres de servicio según la especificación de la extensión SOAP WSDL.</span><span class="sxs-lookup"><span data-stu-id="9f5be-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="9f5be-229">La estructura del elemento contiene una matriz de campos que representan los tipos especificados en las partes del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="9f5be-230">El elemento contenedor se asigna al elemento superior real en el cuerpo del mensaje, tal y como se indica en la especificación SOAP.</span><span class="sxs-lookup"><span data-stu-id="9f5be-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="9f5be-231">En el lado del servidor, cada operación da como resultado una definición de tipo de la operación del servicio servidor resultante.</span><span class="sxs-lookup"><span data-stu-id="9f5be-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="9f5be-232">Esta definición de tipo se utiliza para hacer referencia a la operación en la tabla de funciones como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="9f5be-233">Cada operación también da como resultado la generación de una función de código auxiliar que nfrastructure llama en nombre del delegado al método real.</span><span class="sxs-lookup"><span data-stu-id="9f5be-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

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

<span data-ttu-id="9f5be-234">Para la operación SimpleMethod, la definición de tipo SimpleMethodOperation se ha definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="9f5be-235">Tenga en cuenta que el método generado tiene un argumento expandido listwith la parte de mensaje para el mensaje de entrada y salida de la operación SimpleMethod como parámetros con nombre.</span><span class="sxs-lookup"><span data-stu-id="9f5be-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="9f5be-236">En el lado cliente, cada operación se asigna a una operación de servicio de proxy.</span><span class="sxs-lookup"><span data-stu-id="9f5be-236">On the client side each operation is mapped to a proxy service operation.</span></span>

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

## <a name="processing-wsdlbinding"></a><span data-ttu-id="9f5be-237">Procesando WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="9f5be-237">Processing wsdl:binding</span></span>

<span data-ttu-id="9f5be-238">El modelo de servicio WWSAPI admite la extensión de enlace SOAP.</span><span class="sxs-lookup"><span data-stu-id="9f5be-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="9f5be-239">Para cada enlace hay un **portType** asociado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="9f5be-240">El transporte especificado en la extensión de enlace SOAP solo es de asesoramiento.</span><span class="sxs-lookup"><span data-stu-id="9f5be-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="9f5be-241">La aplicación debe proporcionar información de transporte al crear un canal.</span><span class="sxs-lookup"><span data-stu-id="9f5be-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="9f5be-242">Actualmente se admiten los enlaces de enlace \_ http WS \_ y WS \_ TCP \_ .</span><span class="sxs-lookup"><span data-stu-id="9f5be-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

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

<span data-ttu-id="9f5be-243">En nuestro ejemplo de documento WSDL, solo tenemos un **portType** para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="9f5be-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="9f5be-244">El enlace SOAP proporcionado indica el transporte HTTP, que se especifica como \_ enlace http WS \_ .</span><span class="sxs-lookup"><span data-stu-id="9f5be-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="9f5be-245">Tenga en cuenta que esta estructura no tiene decoración estática ya que esta estructura debe estar disponible para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="9f5be-246">Procesando WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="9f5be-246">Processing wsdl:portType</span></span>

<span data-ttu-id="9f5be-247">Cada **portType** de WSDL se compone de una o varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="9f5be-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="9f5be-248">La operación debe ser coherente con la extensión de enlace SOAP indicada en WSDL: Binding.</span><span class="sxs-lookup"><span data-stu-id="9f5be-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

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

<span data-ttu-id="9f5be-249">En este ejemplo, ISimpleService **portType** solo contiene la operación SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="9f5be-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="9f5be-250">Esto es coherente con la sección de enlace donde solo hay una operación WSDL que se asigna a una acción SOAP.</span><span class="sxs-lookup"><span data-stu-id="9f5be-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="9f5be-251">Puesto que ISimpleService **portType** solo tiene una operación--SimpleMethod, la tabla de función correspondiente solo contiene SimpleMethod como una operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="9f5be-252">En términos de metadatos, cada **portType** se asigna mediante Wsutil.exe a una [**Descripción del \_ contrato \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span><span class="sxs-lookup"><span data-stu-id="9f5be-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="9f5be-253">Cada operación dentro de un **portType** está asignada a una descripción de la [**\_ operación \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span><span class="sxs-lookup"><span data-stu-id="9f5be-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="9f5be-254">En este ejemplo, **portType** la herramienta genera [**la \_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="9f5be-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="9f5be-255">Esta descripción del contrato contiene el número específico de operaciones disponibles en el **portType** de ISimpleService junto con una matriz de [**\_ \_ Descripción**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) de la operación de WS que representa las operaciones individuales definidas en el portType para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="9f5be-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="9f5be-256">Dado que solo hay una operación en ISimpleService portType para ISimpleService, solo hay una definición de **la \_ \_ Descripción de la operación WS** .</span><span class="sxs-lookup"><span data-stu-id="9f5be-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

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

## <a name="processing-wsdlservice"></a><span data-ttu-id="9f5be-257">Procesando WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="9f5be-257">Processing wsdl:service</span></span>

<span data-ttu-id="9f5be-258">WsUtil.exe usa los servicios para buscar enlaces/portTypes y genera una estructura de contrato que describe los tipos, el mensaje, las definiciones de portType, etc.</span><span class="sxs-lookup"><span data-stu-id="9f5be-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="9f5be-259">Las descripciones del contrato son accesibles externamente y se generan como parte de la estructura de la definición global especificada mediante el encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="9f5be-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="9f5be-260">WsUtil.exe admite las extensiones de EndpointReference definidas en WSDL: Port.</span><span class="sxs-lookup"><span data-stu-id="9f5be-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="9f5be-261">La referencia de extremo se define en WS-ADDRESSing como una manera de describir la información de [extremo](endpoint-address.md) de un servicio.</span><span class="sxs-lookup"><span data-stu-id="9f5be-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="9f5be-262">El texto de extensión de referencia de extremo de entrada guardado como [**\_ \_ cadena XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), junto con la descripción de la [**dirección de punto de \_ conexión \_ \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) coincidente, se genera en la sección endpointReferences de la estructura global.</span><span class="sxs-lookup"><span data-stu-id="9f5be-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

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

<span data-ttu-id="9f5be-263">Para crear [**la \_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) con los metadatos generados por WsUtil:</span><span class="sxs-lookup"><span data-stu-id="9f5be-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="9f5be-264">Las cadenas de constantes en el proxy de cliente o el código auxiliar de servicio se generan como campos de tipo WS \_ XML \_ String, y hay un diccionario de constantes para todas las cadenas del archivo de proxy o de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9f5be-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="9f5be-265">Cada cadena del diccionario se genera como un campo en la parte del Diccionario de la estructura local para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9f5be-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

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

## <a name="processing-wsdltype"></a><span data-ttu-id="9f5be-266">Procesando WSDL: Type</span><span class="sxs-lookup"><span data-stu-id="9f5be-266">Processing wsdl:type</span></span>

<span data-ttu-id="9f5be-267">Wsutil.exe solo admite documentos de esquema XML (XSD) en la especificación WSDL: Type.</span><span class="sxs-lookup"><span data-stu-id="9f5be-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="9f5be-268">Un caso especial es cuando un puerto de mensajes especifica una definición de elemento global.</span><span class="sxs-lookup"><span data-stu-id="9f5be-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="9f5be-269">Vea la siguiente sección para obtener más detalles sobre la heurística que se usa en estos casos.</span><span class="sxs-lookup"><span data-stu-id="9f5be-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="9f5be-270">Heurística de procesamiento de parámetros</span><span class="sxs-lookup"><span data-stu-id="9f5be-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="9f5be-271">En el modelo de servicio, los mensajes WSDL se asignan a parámetros específicos en un método.</span><span class="sxs-lookup"><span data-stu-id="9f5be-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="9f5be-272">Wsutil.exe tiene dos estilos de generación de parámetros: en el primer estilo, la operación tiene un parámetro para el mensaje de entrada y un parámetro para el mensaje de salida (si es necesario); en el segundo estilo, Wsutil.exe usa una heurística para asignar y expandir los campos de las estructuras para los mensajes de entrada y los mensajes de salida a distintos parámetros en la operación.</span><span class="sxs-lookup"><span data-stu-id="9f5be-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="9f5be-273">Los mensajes de entrada y salida deben tener elementos de mensaje de tipo de estructura para generar este segundo enfoque.</span><span class="sxs-lookup"><span data-stu-id="9f5be-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="9f5be-274">Wsutil.exe usa las siguientes reglas al generar los parámetros de la operación a partir de los mensajes de entrada y salida:</span><span class="sxs-lookup"><span data-stu-id="9f5be-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="9f5be-275">En el caso de los mensajes de entrada y salida con varias partes de mensaje, cada parte de mensaje es un parámetro independiente en la operación, con el nombre de la parte de mensaje como nombre de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f5be-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="9f5be-276">Para el mensaje de estilo RPC con una parte de mensaje, la parte de mensaje es un parámetro de la operación, con el nombre de la parte de mensaje como nombre de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f5be-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="9f5be-277">Para los mensajes de entrada y salida de estilo de documento con una parte de mensaje:</span><span class="sxs-lookup"><span data-stu-id="9f5be-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="9f5be-278">Si el nombre de una parte del mensaje es "Parameters" y el tipo de elemento es una estructura, cada campo de la estructura se trata como un parámetro independiente y el nombre del campo es el nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f5be-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="9f5be-279">Si el nombre de la parte del mensaje no es "Parameters", el mensaje es un parámetro de la operación con el nombre de mensaje utilizado como el nombre de parámetro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="9f5be-280">En el caso de los mensajes de entrada y salida de estilo de documento con el elemento nillable, el mensaje se asigna a un parámetro, con el nombre de la parte de mensaje como nombre de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f5be-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="9f5be-281">Se agrega un nivel de direccionamiento indirecto adicional para indicar que el puntero puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9f5be-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="9f5be-282">Si solo aparece un campo en el elemento de mensaje de entrada, el campo se trata como un \[ \] parámetro in.</span><span class="sxs-lookup"><span data-stu-id="9f5be-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="9f5be-283">Si solo aparece un campo en el elemento de mensaje de salida, el campo se trata como un parámetro de salida \[ \] .</span><span class="sxs-lookup"><span data-stu-id="9f5be-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="9f5be-284">Si hay un campo con el mismo nombre y el mismo tipo que aparece en el mensaje de entrada y en el mensaje de salida, el campo se trata como un \[ parámetro in y out \] .</span><span class="sxs-lookup"><span data-stu-id="9f5be-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="9f5be-285">Las siguientes herramientas se usan para determinar la dirección de los parámetros:</span><span class="sxs-lookup"><span data-stu-id="9f5be-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="9f5be-286">Si un campo aparece solo en el elemento de mensaje de entrada, el campo se trata como solo en el parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f5be-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="9f5be-287">Si un campo aparece solo en el elemento de mensaje de salida, el campo se trata como parámetro de solo salida.</span><span class="sxs-lookup"><span data-stu-id="9f5be-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="9f5be-288">Si hay un campo con el mismo nombre y el mismo tipo que aparece en el mensaje de entrada y en el mensaje de salida, el campo se trata como un parámetro in y out.</span><span class="sxs-lookup"><span data-stu-id="9f5be-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="9f5be-289">Wsutil.exe solo admite elementos secuenciados.</span><span class="sxs-lookup"><span data-stu-id="9f5be-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="9f5be-290">Rechaza el orden no válido con respecto a \[ in, out \] Parameters si Wsutil.exe no puede combinar los parámetros in y out en una única lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f5be-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="9f5be-291">Se pueden agregar sufijos a los nombres de parámetro para evitar conflictos de nombres.</span><span class="sxs-lookup"><span data-stu-id="9f5be-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

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

<span data-ttu-id="9f5be-292">Wsutil.exe considera que los campos de TNS: SimpleMethod y TNS: SimpleMethodResponse ATO son parámetros, tal como se muestra en las definiciones de parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f5be-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

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

<span data-ttu-id="9f5be-293">Wsutil.exe expande la lista de parámetros de los campos de la lista anterior y genera la estructura **ParamStruct** en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="9f5be-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="9f5be-294">El tiempo de ejecución del modelo de servicio puede utilizar esta estructura para pasar argumentos al código auxiliar del cliente y del servidor.</span><span class="sxs-lookup"><span data-stu-id="9f5be-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="9f5be-295">Esta estructura solo se usa para describir el marco de pila en el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9f5be-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="9f5be-296">No hay ningún cambio en la descripción del mensaje o en las descripciones de elementos a las que hace referencia la descripción del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f5be-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

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

<span data-ttu-id="9f5be-297">Como regla general, se agrega un nivel de direccionamiento indirecto para todos los \[ \] parámetros out y \[ in, out \] .</span><span class="sxs-lookup"><span data-stu-id="9f5be-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="9f5be-298">Operación sin parámetros</span><span class="sxs-lookup"><span data-stu-id="9f5be-298">Parameterless operation</span></span>

<span data-ttu-id="9f5be-299">En las operaciones de documento y literales, Wsutil.exe trata la operación como si tuviera un parámetro de entrada y un parámetro de salida si:</span><span class="sxs-lookup"><span data-stu-id="9f5be-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="9f5be-300">El mensaje de entrada o salida tiene más de una parte.</span><span class="sxs-lookup"><span data-stu-id="9f5be-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="9f5be-301">Solo hay una parte del mensaje y el nombre de la parte del mensaje no es "Parameters".</span><span class="sxs-lookup"><span data-stu-id="9f5be-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="9f5be-302">..</span><span class="sxs-lookup"><span data-stu-id="9f5be-302">..</span></span> <span data-ttu-id="9f5be-303">En el ejemplo anterior, suponiendo que las partes del mensaje se denominan *paramen*"y *ParamOut*, la firma del método se convierte en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f5be-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

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

<span data-ttu-id="9f5be-304">Wsutil.exe genera una firma de versión para la descripción de la operación, de modo que el motor de modelo de servicio de WsCall y del servidor puede comprobar si la descripción generada es aplicable para la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="9f5be-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="9f5be-305">Esta información de versión se genera como parte de la estructura de la [**\_ \_ Descripción**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) de la operación de WS.</span><span class="sxs-lookup"><span data-stu-id="9f5be-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="9f5be-306">El número de versión se puede tratar como un selector de ARM de Unión para que la estructura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="9f5be-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="9f5be-307">Actualmente, el **versionID** se establece to1 sin campos posteriores.</span><span class="sxs-lookup"><span data-stu-id="9f5be-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="9f5be-308">Los versiosn futuros pueden incrementar el número de versión e incluir más campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f5be-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="9f5be-309">Por ejemplo, Wsutil.exe actualmente genera el código siguiente en función del identificador de versión:</span><span class="sxs-lookup"><span data-stu-id="9f5be-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

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

<span data-ttu-id="9f5be-310">En el futuro, se podría expandir de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f5be-310">In the future, it could be expanded as follows:</span></span>

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

## <a name="security"></a><span data-ttu-id="9f5be-311">Seguridad</span><span class="sxs-lookup"><span data-stu-id="9f5be-311">Security</span></span>

<span data-ttu-id="9f5be-312">Vea la sección seguridad en el tema de la [herramienta del compilador Wsutil](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="9f5be-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




