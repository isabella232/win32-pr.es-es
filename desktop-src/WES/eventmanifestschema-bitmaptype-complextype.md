---
title: Tipo complejo de BitMapType
description: Define una lista de asignaciones de nombre y valor entre valores de bit y valores de cadena.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- BitMapType tipo complejo EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493108"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="0d92f-104">Tipo complejo de BitMapType</span><span class="sxs-lookup"><span data-stu-id="0d92f-104">BitMapType Complex Type</span></span>

<span data-ttu-id="0d92f-105">Define una lista de asignaciones de nombre y valor entre valores de bit y valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="0d92f-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0d92f-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d92f-106">Child elements</span></span>



| <span data-ttu-id="0d92f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d92f-107">Element</span></span>                                                   | <span data-ttu-id="0d92f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d92f-108">Type</span></span>                                                                       | <span data-ttu-id="0d92f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d92f-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="0d92f-110">**mapa**</span><span class="sxs-lookup"><span data-stu-id="0d92f-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="0d92f-111">**BitMapValueType**</span><span class="sxs-lookup"><span data-stu-id="0d92f-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="0d92f-112">Define la asignación entre un valor de bit y un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="0d92f-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0d92f-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d92f-113">Attributes</span></span>



| <span data-ttu-id="0d92f-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d92f-114">Name</span></span>   | <span data-ttu-id="0d92f-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d92f-115">Type</span></span>                                                              | <span data-ttu-id="0d92f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d92f-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d92f-117">name</span><span class="sxs-lookup"><span data-stu-id="0d92f-117">name</span></span>   | <span data-ttu-id="0d92f-118">string</span><span class="sxs-lookup"><span data-stu-id="0d92f-118">string</span></span>                                                            | <span data-ttu-id="0d92f-119">El nombre del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="0d92f-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0d92f-120">símbolo</span><span class="sxs-lookup"><span data-stu-id="0d92f-120">symbol</span></span> | [<span data-ttu-id="0d92f-121">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="0d92f-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="0d92f-122">Símbolo que se va a usar para hacer referencia a las asignaciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0d92f-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="0d92f-123">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="0d92f-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="0d92f-124">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0d92f-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0d92f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d92f-125">Requirements</span></span>



| <span data-ttu-id="0d92f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d92f-126">Requirement</span></span> | <span data-ttu-id="0d92f-127">Value</span><span class="sxs-lookup"><span data-stu-id="0d92f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d92f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d92f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d92f-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d92f-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d92f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d92f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d92f-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d92f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





