---
title: Tipo complejo de ValueMapValueType
description: Define la asignación entre un valor entero y un valor de cadena. | Tipo complejo de ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- ValueMapValueType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424183"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="3f487-105">Tipo complejo de ValueMapValueType</span><span class="sxs-lookup"><span data-stu-id="3f487-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="3f487-106">Define la asignación entre un valor entero y un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="3f487-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="3f487-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f487-107">Attributes</span></span>



| <span data-ttu-id="3f487-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f487-108">Name</span></span>    | <span data-ttu-id="3f487-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f487-109">Type</span></span>                                                              | <span data-ttu-id="3f487-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f487-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f487-111">message</span><span class="sxs-lookup"><span data-stu-id="3f487-111">message</span></span> | [<span data-ttu-id="3f487-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="3f487-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="3f487-113">Valor de la cadena localizada a la que se asigna el valor entero.</span><span class="sxs-lookup"><span data-stu-id="3f487-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="3f487-114">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="3f487-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="3f487-115">símbolo</span><span class="sxs-lookup"><span data-stu-id="3f487-115">symbol</span></span>  | [<span data-ttu-id="3f487-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="3f487-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="3f487-117">Símbolo que se va a usar para hacer referencia a la asignación en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f487-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="3f487-118">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="3f487-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="3f487-119">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3f487-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="3f487-120">value</span><span class="sxs-lookup"><span data-stu-id="3f487-120">value</span></span>   | [<span data-ttu-id="3f487-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="3f487-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="3f487-122">Valor entero que se va a asignar al valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="3f487-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="3f487-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f487-123">Requirements</span></span>



| <span data-ttu-id="3f487-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f487-124">Requirement</span></span> | <span data-ttu-id="3f487-125">Value</span><span class="sxs-lookup"><span data-stu-id="3f487-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f487-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f487-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f487-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3f487-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f487-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f487-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f487-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f487-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





