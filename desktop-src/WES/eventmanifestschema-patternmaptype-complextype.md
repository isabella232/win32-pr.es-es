---
title: Tipo complejo de PatternMapType
description: No se utiliza. Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType tipo complejo EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491284"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="b663b-106">Tipo complejo de PatternMapType</span><span class="sxs-lookup"><span data-stu-id="b663b-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="b663b-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b663b-107">Not used.</span></span> <span data-ttu-id="b663b-108">Define una asignación entre dos expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="b663b-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="b663b-109">Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b663b-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b663b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b663b-110">Child elements</span></span>



| <span data-ttu-id="b663b-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b663b-111">Element</span></span>                                                       | <span data-ttu-id="b663b-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b663b-112">Type</span></span>                                                                               | <span data-ttu-id="b663b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b663b-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b663b-114">**mapa**</span><span class="sxs-lookup"><span data-stu-id="b663b-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="b663b-115">**PatternMapValueType**</span><span class="sxs-lookup"><span data-stu-id="b663b-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="b663b-116">Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.</span><span class="sxs-lookup"><span data-stu-id="b663b-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b663b-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="b663b-117">Attributes</span></span>



| <span data-ttu-id="b663b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b663b-118">Name</span></span>   | <span data-ttu-id="b663b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b663b-119">Type</span></span>                                                              | <span data-ttu-id="b663b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b663b-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b663b-121">format</span><span class="sxs-lookup"><span data-stu-id="b663b-121">format</span></span> | <span data-ttu-id="b663b-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="b663b-122">anyURI</span></span>                                                            | <span data-ttu-id="b663b-123">Motor de expresiones regulares que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b663b-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b663b-124">name</span><span class="sxs-lookup"><span data-stu-id="b663b-124">name</span></span>   | <span data-ttu-id="b663b-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="b663b-125">**QName**</span></span>                                                         | <span data-ttu-id="b663b-126">Nombre del mapa de patrones.</span><span class="sxs-lookup"><span data-stu-id="b663b-126">The name of the pattern map.</span></span> <span data-ttu-id="b663b-127">Use el nombre en un elemento de datos para hacer referencia a las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="b663b-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="b663b-128">símbolo</span><span class="sxs-lookup"><span data-stu-id="b663b-128">symbol</span></span> | [<span data-ttu-id="b663b-129">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="b663b-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b663b-130">Símbolo que se va a usar para hacer referencia a las asignaciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b663b-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="b663b-131">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="b663b-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="b663b-132">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b663b-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b663b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b663b-133">Requirements</span></span>



| <span data-ttu-id="b663b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b663b-134">Requirement</span></span> | <span data-ttu-id="b663b-135">Value</span><span class="sxs-lookup"><span data-stu-id="b663b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b663b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b663b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b663b-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b663b-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b663b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b663b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b663b-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b663b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





