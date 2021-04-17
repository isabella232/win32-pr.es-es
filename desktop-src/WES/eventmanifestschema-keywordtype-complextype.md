---
title: Tipo complejo de KeywordType
description: Define una palabra clave que identifica una categoría de eventos. | Tipo complejo de KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- KeywordType tipo complejo EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698090"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="49eb6-105">Tipo complejo de KeywordType</span><span class="sxs-lookup"><span data-stu-id="49eb6-105">KeywordType Complex Type</span></span>

<span data-ttu-id="49eb6-106">Define una palabra clave que identifica una categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="49eb6-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="49eb6-107">Una palabra clave es una etiqueta que se adjunta a un evento para agrupar eventos en función de su uso.</span><span class="sxs-lookup"><span data-stu-id="49eb6-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="49eb6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="49eb6-108">Attributes</span></span>



| <span data-ttu-id="49eb6-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="49eb6-109">Name</span></span>    | <span data-ttu-id="49eb6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="49eb6-110">Type</span></span>                                                              | <span data-ttu-id="49eb6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="49eb6-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49eb6-112">mask</span><span class="sxs-lookup"><span data-stu-id="49eb6-112">mask</span></span>    | [<span data-ttu-id="49eb6-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="49eb6-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="49eb6-114">Máscara de bits que solo debe tener un bit establecido.</span><span class="sxs-lookup"><span data-stu-id="49eb6-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="49eb6-115">El bit representa una categoría de eventos (por ejemplo, eventos de lectura o eventos de escritura).</span><span class="sxs-lookup"><span data-stu-id="49eb6-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="49eb6-116">Puede especificar valores de bit en el intervalo de 0x0000000000000001 a 0x0000800000000000 (bits del 0 al 47).</span><span class="sxs-lookup"><span data-stu-id="49eb6-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="49eb6-117">message</span><span class="sxs-lookup"><span data-stu-id="49eb6-117">message</span></span> | [<span data-ttu-id="49eb6-118">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="49eb6-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="49eb6-119">Nombre para mostrar localizado de la palabra clave.</span><span class="sxs-lookup"><span data-stu-id="49eb6-119">The localized display name for the keyword.</span></span> <span data-ttu-id="49eb6-120">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="49eb6-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="49eb6-121">name</span><span class="sxs-lookup"><span data-stu-id="49eb6-121">name</span></span>    | <span data-ttu-id="49eb6-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="49eb6-122">**QName**</span></span>                                                         | <span data-ttu-id="49eb6-123">Nombre de la palabra clave.</span><span class="sxs-lookup"><span data-stu-id="49eb6-123">The name of the keyword.</span></span> <span data-ttu-id="49eb6-124">El nombre debe ser único en la lista de palabras clave que define el proveedor.</span><span class="sxs-lookup"><span data-stu-id="49eb6-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="49eb6-125">símbolo</span><span class="sxs-lookup"><span data-stu-id="49eb6-125">symbol</span></span>  | [<span data-ttu-id="49eb6-126">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="49eb6-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="49eb6-127">Símbolo que se va a usar para hacer referencia a la palabra clave en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49eb6-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="49eb6-128">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la palabra clave en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="49eb6-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="49eb6-129">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="49eb6-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49eb6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49eb6-130">Remarks</span></span>

<span data-ttu-id="49eb6-131">El archivo Winmeta.xml que se incluye en el Windows SDK contiene una lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="49eb6-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="49eb6-132">Estas palabras clave están reservadas y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="49eb6-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="49eb6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49eb6-133">Requirements</span></span>



| <span data-ttu-id="49eb6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="49eb6-134">Requirement</span></span> | <span data-ttu-id="49eb6-135">Value</span><span class="sxs-lookup"><span data-stu-id="49eb6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49eb6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49eb6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="49eb6-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49eb6-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49eb6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49eb6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="49eb6-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49eb6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





