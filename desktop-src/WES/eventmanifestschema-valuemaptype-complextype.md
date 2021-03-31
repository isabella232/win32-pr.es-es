---
title: Tipo complejo de ValueMapType
description: Define una lista de asignaciones de nombre y valor entre valores enteros y valores de cadena.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- ValueMapType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800937"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="6a9cc-104">Tipo complejo de ValueMapType</span><span class="sxs-lookup"><span data-stu-id="6a9cc-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="6a9cc-105">Define una lista de asignaciones de nombre y valor entre valores enteros y valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6a9cc-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a9cc-106">Child elements</span></span>



| <span data-ttu-id="6a9cc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a9cc-107">Element</span></span>                                                     | <span data-ttu-id="6a9cc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a9cc-108">Type</span></span>                                                                           | <span data-ttu-id="6a9cc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a9cc-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="6a9cc-110">**mapa**</span><span class="sxs-lookup"><span data-stu-id="6a9cc-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="6a9cc-111">**ValueMapValueType**</span><span class="sxs-lookup"><span data-stu-id="6a9cc-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="6a9cc-112">Define la asignación entre un valor entero y un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="6a9cc-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a9cc-113">Attributes</span></span>



| <span data-ttu-id="6a9cc-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a9cc-114">Name</span></span>   | <span data-ttu-id="6a9cc-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a9cc-115">Type</span></span>                                                              | <span data-ttu-id="6a9cc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a9cc-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9cc-117">name</span><span class="sxs-lookup"><span data-stu-id="6a9cc-117">name</span></span>   | <span data-ttu-id="6a9cc-118">string</span><span class="sxs-lookup"><span data-stu-id="6a9cc-118">string</span></span>                                                            | <span data-ttu-id="6a9cc-119">Nombre del mapa de valores.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-119">The name of the value map.</span></span> <span data-ttu-id="6a9cc-120">Use el nombre en un elemento de datos para hacer referencia a las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="6a9cc-121">símbolo</span><span class="sxs-lookup"><span data-stu-id="6a9cc-121">symbol</span></span> | [<span data-ttu-id="6a9cc-122">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="6a9cc-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="6a9cc-123">Símbolo que se va a usar para hacer referencia a las asignaciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="6a9cc-124">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="6a9cc-125">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6a9cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a9cc-126">Requirements</span></span>



| <span data-ttu-id="6a9cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9cc-127">Requirement</span></span> | <span data-ttu-id="6a9cc-128">Value</span><span class="sxs-lookup"><span data-stu-id="6a9cc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a9cc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a9cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9cc-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a9cc-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a9cc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a9cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9cc-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a9cc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





