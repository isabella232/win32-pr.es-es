---
title: Compatibilidad con esquemas
description: WsUtil.exe admite el esquema XSD especificado en el esquema XML.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Servicios Web de compatibilidad de esquemas para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994981"
---
# <a name="schema-support"></a><span data-ttu-id="c5c00-106">Compatibilidad con esquemas</span><span class="sxs-lookup"><span data-stu-id="c5c00-106">Schema support</span></span>

<span data-ttu-id="c5c00-107">WsUtil.exe admite el esquema XSD especificado en el [esquema XML](https://www.w3.org/XML/Schema).</span><span class="sxs-lookup"><span data-stu-id="c5c00-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="c5c00-108">el archivo XSD y WSDL: Type deben tratarse en la misma categoría, con la excepción en WSDL: Type cuando un elemento global puede ser una lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5c00-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="c5c00-109">Wsutil.exe genera descripciones de elementos para todas las definiciones de elementos globales que se pueden usar en el serializador, con una salida adicional para la estructura de parámetros especificada en la [compatibilidad con WSDL](wsdl-support.md).</span><span class="sxs-lookup"><span data-stu-id="c5c00-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="c5c00-110">Nivel de compatibilidad de esquema XSD</span><span class="sxs-lookup"><span data-stu-id="c5c00-110">XSD Schema Support Level</span></span>

<span data-ttu-id="c5c00-111">WsUtil.exe no admite la extensión completa del esquema XSD.</span><span class="sxs-lookup"><span data-stu-id="c5c00-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="c5c00-112">El nivel de compatibilidad actual se define en el [nivel de compatibilidad del esquema](schema-support-level.md).</span><span class="sxs-lookup"><span data-stu-id="c5c00-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="c5c00-113">Generación de identificadores</span><span class="sxs-lookup"><span data-stu-id="c5c00-113">Identifier generation</span></span>

<span data-ttu-id="c5c00-114">Es posible que el nombre de elemento o el nombre de tipo del esquema no sea un identificador de C válido y los nombres se hayan normalizado para los nombres de C válidos generados.</span><span class="sxs-lookup"><span data-stu-id="c5c00-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="c5c00-115">Los caracteres de identificador de C no válidos se convierten en el nombre hexadecimal y un carácter de subrayado ' \_ ' se puede anteponer al nombre si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c5c00-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="c5c00-116">Los tipos anónimos se denominan después del nombre del elemento envolvente, pero llevan el carácter de subrayado " \_ " para evitar el conflicto de nombres.</span><span class="sxs-lookup"><span data-stu-id="c5c00-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="c5c00-117">Los nombres de tipos globales se conservan tal como están después de normalizarse los caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="c5c00-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="c5c00-118">Los tipos anónimos anidados tienen como prefijo el nombre del tipo primario.</span><span class="sxs-lookup"><span data-stu-id="c5c00-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="c5c00-119">Para cada definición de elemento global, wsutil.exe genera [**una \_ \_ Descripción del elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) en la estructura de descripción global.</span><span class="sxs-lookup"><span data-stu-id="c5c00-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="c5c00-120">Para cada definición de tipo global, wsutil.exe genera una descripción de tipo en la estructura de descripción global a la que hace referencia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c5c00-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="c5c00-121">Para cada campo de la estructura, wsutil.exe genera una [**\_ \_ Descripción de campo WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) incrustada como parte de la estructura del gabinete.</span><span class="sxs-lookup"><span data-stu-id="c5c00-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="c5c00-122">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="c5c00-122">Simple Types</span></span>

<span data-ttu-id="c5c00-123">Los tipos de valor, como se enumeran en el [**\_ \_ tipo de valor WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), se tratan como tipos simples.</span><span class="sxs-lookup"><span data-stu-id="c5c00-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="c5c00-124">Observe que \_ \_ el tipo de valor WS es realmente un subconjunto de [**\_ tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="c5c00-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="c5c00-125">Incluye tipos de datos integrales básicos y flotantes, así como decimales, WS \_ DateTime y UUID.</span><span class="sxs-lookup"><span data-stu-id="c5c00-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="c5c00-126">En el modelo de servicio, en los tipos simples se pasan por valor, mientras que out y in, los tipos simples se pasan por referencia.</span><span class="sxs-lookup"><span data-stu-id="c5c00-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="c5c00-127">Wsutil crear una descripción del elemento simple como la siguiente para el elemento global que contiene tipos simples.</span><span class="sxs-lookup"><span data-stu-id="c5c00-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="c5c00-128">Wsutil genera la descripción del elemento siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5c00-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="c5c00-129">Esta estructura se genera como parte de la estructura de descripción global generada en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c5c00-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="c5c00-130">Matrices</span><span class="sxs-lookup"><span data-stu-id="c5c00-130">Arrays</span></span>

<span data-ttu-id="c5c00-131">El elemento con maxOccurs mayor que 1 o Sequence con un solo elemento, y el elemento secundario tiene un maxOccurs mayor que 1, se trata como una matriz.</span><span class="sxs-lookup"><span data-stu-id="c5c00-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="c5c00-132">En el caso de un elemento de matriz en el esquema, wsutil.exe genera dos campos: un campo de recuento que no va en el cable y un campo de puntero que contiene el tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="c5c00-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="c5c00-133">El archivo de encabezado contiene la definición de la estructura de C para la matriz, con la cuenta de campo que especifica el recuento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c5c00-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="c5c00-134">A continuación se indica parte del prototipo LocalDefinition que describe la matriz:</span><span class="sxs-lookup"><span data-stu-id="c5c00-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="c5c00-135">A continuación se enumeran las definiciones generadas de las descripciones anteriores, observe la \_ asignación de campos de elemento de repetición WS \_ \_ \_ que indica el campo como un campo de matriz.</span><span class="sxs-lookup"><span data-stu-id="c5c00-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="c5c00-136">Si la matriz es un campo de parámetro en el mensaje de entrada/salida, se generarían dos parámetros reales para el método.</span><span class="sxs-lookup"><span data-stu-id="c5c00-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="c5c00-137">Si la matriz es un parámetro out o in, out, habrá un nivel adicional de direccionamiento indirecto para ambos campos en paramStruct.</span><span class="sxs-lookup"><span data-stu-id="c5c00-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="c5c00-138">Intervalo en matriz</span><span class="sxs-lookup"><span data-stu-id="c5c00-138">Range on Array</span></span>

<span data-ttu-id="c5c00-139">Se recomienda el procedimiento recomendado de no especificar maxOccur = "unbounded" para las matrices.</span><span class="sxs-lookup"><span data-stu-id="c5c00-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="c5c00-140">En su lugar, se debe especificar un número entero fijo para establecer un límite superior de recuentos de matrices permitido.</span><span class="sxs-lookup"><span data-stu-id="c5c00-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="c5c00-141">Range es compatible con los tipos enteros, así como con cadenas, matrices de bytes y matrices genéricas.</span><span class="sxs-lookup"><span data-stu-id="c5c00-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="c5c00-142">Heurística para encapsulado en lugar de una matriz desempaquetada</span><span class="sxs-lookup"><span data-stu-id="c5c00-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="c5c00-143">A veces, las matrices se ajustan dentro de otra estructura para incrustarse en una estructura de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c5c00-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="c5c00-144">En ese caso, deberíamos quitar la capa de contenedor intermedia.</span><span class="sxs-lookup"><span data-stu-id="c5c00-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="c5c00-145">WsUtil.exe genera el mismo prototipo y descripciones que SimpleArray descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c5c00-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="c5c00-146">Wsutil detecta que SimpleArrayWrapper es un contenedor en torno a SimpleArray y solo genera las siguientes estructuras, con una estructura independiente para SimpleArray</span><span class="sxs-lookup"><span data-stu-id="c5c00-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="c5c00-147">wsutil.exe genera las siguientes definiciones para el prototipo coincidente anterior, observa que en la descripción del campo se rellenan los campos nombre del contenedor y espacio de nombres del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c5c00-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="c5c00-148">Estructuras</span><span class="sxs-lookup"><span data-stu-id="c5c00-148">Structures</span></span>

<span data-ttu-id="c5c00-149">Un complexType con varios elementos en una secuencia es una estructura.</span><span class="sxs-lookup"><span data-stu-id="c5c00-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="c5c00-150">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="c5c00-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="c5c00-151">Wsutil.exe genera un prototipo de estructura como:</span><span class="sxs-lookup"><span data-stu-id="c5c00-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="c5c00-152">wsutil genera el siguiente prototipo para LocalDefinition:</span><span class="sxs-lookup"><span data-stu-id="c5c00-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="c5c00-153">La definición de la estructura es similar a la siguiente, con dos descripciones de campo en la estructura.</span><span class="sxs-lookup"><span data-stu-id="c5c00-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="c5c00-154">Para admitir la extensibilidad, las estructuras incrustadas siempre se definen pasadas por referencia.</span><span class="sxs-lookup"><span data-stu-id="c5c00-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="c5c00-155">En el servicio, todas las estructuras out o in, out se pasan con un puntero doble para permitir una extensión futura de la estructura, así como para permitir la estructura nillable.</span><span class="sxs-lookup"><span data-stu-id="c5c00-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="c5c00-156">Estructuras recursivas</span><span class="sxs-lookup"><span data-stu-id="c5c00-156">Recursive Structures</span></span>

<span data-ttu-id="c5c00-157">Se admiten las estructuras recursivas y los tipos incrustados se pasan por referencia.</span><span class="sxs-lookup"><span data-stu-id="c5c00-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="c5c00-158">Para el WSDL siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5c00-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="c5c00-159">Wsutil genera las siguientes definiciones de tipo, así como las descripciones de tipos:</span><span class="sxs-lookup"><span data-stu-id="c5c00-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="c5c00-160">La definición se genera como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c5c00-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="c5c00-161">Herencia de estructura</span><span class="sxs-lookup"><span data-stu-id="c5c00-161">Structure inheritence</span></span>

<span data-ttu-id="c5c00-162">wsutil admite la extensión de tipo complejo, donde un tipo complejo es una extensión a otro tipo complejo.</span><span class="sxs-lookup"><span data-stu-id="c5c00-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="c5c00-163">El fragmento XSD anterior indica que DerivedLinkList deriva de LinkList.</span><span class="sxs-lookup"><span data-stu-id="c5c00-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="c5c00-164">Wsutil.exe genera rutinas auxiliares para C y C++ con el fin de facilitar a la aplicación la configuración de la información de tipo del tipo base y los tipos derivados.</span><span class="sxs-lookup"><span data-stu-id="c5c00-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="c5c00-165">En el código siguiente, \_ la \_ macro WS CPLUSPLUS se usa para diferenciar la definición del lenguaje C y C++:</span><span class="sxs-lookup"><span data-stu-id="c5c00-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="c5c00-166">En el ayudante de estilo de C, antes de serialiation, la aplicación llama a wsutil rutina generada LinkList \_ init para inicializar la estructura y establecer la descripción de tipo en Linklist Descripción de tipo.</span><span class="sxs-lookup"><span data-stu-id="c5c00-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="c5c00-167">Después de la deserialización, la aplicación puede llamar a LinkList \_ como \_ DerivedLinkList para obtener el tipo derivado.</span><span class="sxs-lookup"><span data-stu-id="c5c00-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="c5c00-168">Para recuperar la información de tipo en tiempo de ejecución, wsutil genera el primer campo de tipo base con el tipo de [**\_ \_ Descripción de struct de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* y la asignación de campos de asignación de [**\_ campo de atributo de tipo \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) para describir la información de xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="c5c00-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="c5c00-169">La aplicación puede establecer o comprobar directamente el campo para determinar el tipo real de estructuras.</span><span class="sxs-lookup"><span data-stu-id="c5c00-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="c5c00-170">Por ejemplo, el código siguiente establece el tipo de la estructura para que sea DrivedLinkList:</span><span class="sxs-lookup"><span data-stu-id="c5c00-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="c5c00-171">Una vez deserializada la estructura, la aplicación puede comparar directamente la descripción de tipo para determinar el tipo deserializado:</span><span class="sxs-lookup"><span data-stu-id="c5c00-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="c5c00-172">wsutil generar la clase para la estructura base y la estructura derivada.</span><span class="sxs-lookup"><span data-stu-id="c5c00-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="c5c00-173">El constructor predeterminado inicializa el tipo y la descripción del tipo coincidente.</span><span class="sxs-lookup"><span data-stu-id="c5c00-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="c5c00-174">La rutina AsDerivedType ayuda a realizar una conversión de tipos segura entre tipos.</span><span class="sxs-lookup"><span data-stu-id="c5c00-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="c5c00-175">nillable</span><span class="sxs-lookup"><span data-stu-id="c5c00-175">nillable</span></span>

<span data-ttu-id="c5c00-176">el atributo nillable es compatible con cadenas, estructuras y matrices de bytes.</span><span class="sxs-lookup"><span data-stu-id="c5c00-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="c5c00-177">El \_ atributo nillable de campo WS se \_ agregará a los campos con el atributo nillable.</span><span class="sxs-lookup"><span data-stu-id="c5c00-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="c5c00-178">El puntero se establecerá en **null** si un elemento es nillable.</span><span class="sxs-lookup"><span data-stu-id="c5c00-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="c5c00-179">Un campo nillable en una estructura se trata como un puntero.</span><span class="sxs-lookup"><span data-stu-id="c5c00-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="c5c00-180">Una estructura de parámetros con el atributo nillable se pasará por referencia.</span><span class="sxs-lookup"><span data-stu-id="c5c00-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="c5c00-181">punteros</span><span class="sxs-lookup"><span data-stu-id="c5c00-181">pointers</span></span>

<span data-ttu-id="c5c00-182">El tipo de valor se debe pasar por valor o por referencia para los parámetros out.</span><span class="sxs-lookup"><span data-stu-id="c5c00-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="c5c00-183">El puntero Double no se permite excepto para las estructuras de solo salida.</span><span class="sxs-lookup"><span data-stu-id="c5c00-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="c5c00-184">Sin parámetros</span><span class="sxs-lookup"><span data-stu-id="c5c00-184">Parameterless</span></span>

<span data-ttu-id="c5c00-185">Recuerde la explicación anterior del nombre "Parameters" de la parte del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5c00-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="c5c00-186">Si se especifica, se intentará generar un fotograma combinado para el mensaje de entrada y salida para la operación de servicio resultante.</span><span class="sxs-lookup"><span data-stu-id="c5c00-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="c5c00-187">Si no se especifica, la operación de servicio resultante contendrá mensajes de entrada y salida como Structs como parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5c00-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="c5c00-188">Por lo tanto, para la operación SimpleMethod, la firma del servicio y el cliente se verán como.</span><span class="sxs-lookup"><span data-stu-id="c5c00-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="c5c00-189">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c5c00-189">Security</span></span>

<span data-ttu-id="c5c00-190">Vea la sección de seguridad en la [herramienta compilador de Wsutil](wsutil-compiler-tool.md) y la [serialización](serialization.md)</span><span class="sxs-lookup"><span data-stu-id="c5c00-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




