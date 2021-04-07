---
title: Tipo complejo de BitMapValueType
description: Define la asignación entre un valor de bit y un valor de cadena. | Tipo complejo de BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType tipo complejo EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003612"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="fc18c-105">Tipo complejo de BitMapValueType</span><span class="sxs-lookup"><span data-stu-id="fc18c-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="fc18c-106">Define la asignación entre un valor de bit y un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="fc18c-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="fc18c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc18c-107">Attributes</span></span>



| <span data-ttu-id="fc18c-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc18c-108">Name</span></span>    | <span data-ttu-id="fc18c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc18c-109">Type</span></span>                                                              | <span data-ttu-id="fc18c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc18c-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc18c-111">message</span><span class="sxs-lookup"><span data-stu-id="fc18c-111">message</span></span> | [<span data-ttu-id="fc18c-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="fc18c-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="fc18c-113">Valor de la cadena localizada a la que se asigna el valor de bit.</span><span class="sxs-lookup"><span data-stu-id="fc18c-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="fc18c-114">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="fc18c-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="fc18c-115">símbolo</span><span class="sxs-lookup"><span data-stu-id="fc18c-115">symbol</span></span>  | [<span data-ttu-id="fc18c-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="fc18c-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="fc18c-117">Símbolo que se va a usar para hacer referencia a la asignación en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc18c-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="fc18c-118">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="fc18c-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="fc18c-119">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fc18c-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="fc18c-120">value</span><span class="sxs-lookup"><span data-stu-id="fc18c-120">value</span></span>   | [<span data-ttu-id="fc18c-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="fc18c-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="fc18c-122">Valor de bit que se va a asignar al valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="fc18c-122">The bit value to map to the string value.</span></span> <span data-ttu-id="fc18c-123">Debe especificar un número hexadecimal con un solo bit establecido.</span><span class="sxs-lookup"><span data-stu-id="fc18c-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="fc18c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc18c-124">Remarks</span></span>

<span data-ttu-id="fc18c-125">Asigna un valor hexadecimal (el número debe ir precedido de 0x) con un único bit establecido en un nombre.</span><span class="sxs-lookup"><span data-stu-id="fc18c-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc18c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc18c-126">Requirements</span></span>



| <span data-ttu-id="fc18c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc18c-127">Requirement</span></span> | <span data-ttu-id="fc18c-128">Value</span><span class="sxs-lookup"><span data-stu-id="fc18c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc18c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc18c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fc18c-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc18c-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc18c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc18c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fc18c-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc18c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





