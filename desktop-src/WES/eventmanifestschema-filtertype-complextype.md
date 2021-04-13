---
title: Tipo complejo de FilterType
description: Define un filtro de datos que una sesión utiliza para filtrar los eventos en función de los datos de evento.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- Registro de eventos de tipo complejo FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493168"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="362fb-104">Tipo complejo de FilterType</span><span class="sxs-lookup"><span data-stu-id="362fb-104">FilterType Complex Type</span></span>

<span data-ttu-id="362fb-105">Define un filtro de datos que una sesión utiliza para filtrar los eventos en función de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="362fb-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="362fb-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="362fb-106">Attributes</span></span>



| <span data-ttu-id="362fb-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="362fb-107">Name</span></span>    | <span data-ttu-id="362fb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="362fb-108">Type</span></span>                                                              | <span data-ttu-id="362fb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="362fb-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="362fb-110">message</span><span class="sxs-lookup"><span data-stu-id="362fb-110">message</span></span> | [<span data-ttu-id="362fb-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="362fb-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="362fb-112">Descripción localizada del filtro.</span><span class="sxs-lookup"><span data-stu-id="362fb-112">The localized description for the filter.</span></span> <span data-ttu-id="362fb-113">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="362fb-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="362fb-114">name</span><span class="sxs-lookup"><span data-stu-id="362fb-114">name</span></span>    | <span data-ttu-id="362fb-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="362fb-115">**QName**</span></span>                                                         | <span data-ttu-id="362fb-116">Nombre que identifica el filtro.</span><span class="sxs-lookup"><span data-stu-id="362fb-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="362fb-117">símbolo</span><span class="sxs-lookup"><span data-stu-id="362fb-117">symbol</span></span>  | [<span data-ttu-id="362fb-118">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="362fb-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="362fb-119">Símbolo que se va a usar para hacer referencia al filtro en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="362fb-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="362fb-120">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el filtro en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="362fb-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="362fb-121">tid</span><span class="sxs-lookup"><span data-stu-id="362fb-121">tid</span></span>     | <span data-ttu-id="362fb-122">token</span><span class="sxs-lookup"><span data-stu-id="362fb-122">token</span></span>                                                             | <span data-ttu-id="362fb-123">Identificador de plantilla que describe los datos de filtro que la sesión pasa al proveedor cuando habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="362fb-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="362fb-124">value</span><span class="sxs-lookup"><span data-stu-id="362fb-124">value</span></span>   | [<span data-ttu-id="362fb-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="362fb-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="362fb-126">Valor entero que identifica de forma única el filtro en la lista de filtros que se definen.</span><span class="sxs-lookup"><span data-stu-id="362fb-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="362fb-127">version</span><span class="sxs-lookup"><span data-stu-id="362fb-127">version</span></span> | [<span data-ttu-id="362fb-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="362fb-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="362fb-129">Valor entero que identifica esta versión del filtro.</span><span class="sxs-lookup"><span data-stu-id="362fb-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="362fb-130">Si no se especifica, el valor es cero.</span><span class="sxs-lookup"><span data-stu-id="362fb-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="362fb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="362fb-131">Requirements</span></span>



| <span data-ttu-id="362fb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="362fb-132">Requirement</span></span> | <span data-ttu-id="362fb-133">Value</span><span class="sxs-lookup"><span data-stu-id="362fb-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="362fb-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="362fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="362fb-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="362fb-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="362fb-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="362fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="362fb-137">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="362fb-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





