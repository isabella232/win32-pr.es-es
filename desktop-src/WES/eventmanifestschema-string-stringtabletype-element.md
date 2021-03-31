---
title: Elemento String (StringTableType)
description: Define una cadena traducida.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- elemento de cadena EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996579"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="ed446-104">Elemento String (StringTableType)</span><span class="sxs-lookup"><span data-stu-id="ed446-104">string (StringTableType) Element</span></span>

<span data-ttu-id="ed446-105">Define una cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="ed446-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ed446-106">El elemento de **cadena** se define mediante el tipo complejo de [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ed446-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="ed446-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed446-107">Attributes</span></span>



| <span data-ttu-id="ed446-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ed446-108">Name</span></span>       | <span data-ttu-id="ed446-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed446-109">Type</span></span>   | <span data-ttu-id="ed446-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed446-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed446-111">id</span><span class="sxs-lookup"><span data-stu-id="ed446-111">id</span></span>         | <span data-ttu-id="ed446-112">string</span><span class="sxs-lookup"><span data-stu-id="ed446-112">string</span></span> | <span data-ttu-id="ed446-113">Identificador que identifica de forma única la cadena en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="ed446-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="ed446-114">stringType</span><span class="sxs-lookup"><span data-stu-id="ed446-114">stringType</span></span> | <span data-ttu-id="ed446-115">string</span><span class="sxs-lookup"><span data-stu-id="ed446-115">string</span></span> | <span data-ttu-id="ed446-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ed446-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="ed446-117">value</span><span class="sxs-lookup"><span data-stu-id="ed446-117">value</span></span>      | <span data-ttu-id="ed446-118">string</span><span class="sxs-lookup"><span data-stu-id="ed446-118">string</span></span> | <span data-ttu-id="ed446-119">Cadena localizada.</span><span class="sxs-lookup"><span data-stu-id="ed446-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="ed446-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed446-120">Requirements</span></span>



| <span data-ttu-id="ed446-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed446-121">Requirement</span></span> | <span data-ttu-id="ed446-122">Value</span><span class="sxs-lookup"><span data-stu-id="ed446-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed446-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed446-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed446-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed446-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed446-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed446-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed446-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed446-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed446-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed446-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed446-128">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="ed446-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ed446-129">**stringTable (LocalizationType)**</span><span class="sxs-lookup"><span data-stu-id="ed446-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





