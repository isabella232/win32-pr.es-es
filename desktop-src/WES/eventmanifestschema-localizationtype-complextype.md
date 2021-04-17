---
title: Tipo complejo de LocalizationType
description: Define un grupo de recursos localizados al que se hace referencia en el manifiesto. | Tipo complejo de LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType tipo complejo EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698058"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="c487d-105">Tipo complejo de LocalizationType</span><span class="sxs-lookup"><span data-stu-id="c487d-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="c487d-106">Define un grupo de recursos localizados al que se hace referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c487d-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c487d-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c487d-107">Child elements</span></span>



| <span data-ttu-id="c487d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c487d-108">Element</span></span>                                                                         | <span data-ttu-id="c487d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c487d-109">Type</span></span>                                                                       | <span data-ttu-id="c487d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c487d-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c487d-111">**recursos**</span><span class="sxs-lookup"><span data-stu-id="c487d-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="c487d-112">Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c487d-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="c487d-113">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="c487d-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="c487d-114">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="c487d-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="c487d-115">Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c487d-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="c487d-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="c487d-116">Attributes</span></span>



| <span data-ttu-id="c487d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="c487d-117">Name</span></span>            | <span data-ttu-id="c487d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="c487d-118">Type</span></span>   | <span data-ttu-id="c487d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c487d-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c487d-120">culture</span><span class="sxs-lookup"><span data-stu-id="c487d-120">culture</span></span>         | <span data-ttu-id="c487d-121">string</span><span class="sxs-lookup"><span data-stu-id="c487d-121">string</span></span> | <span data-ttu-id="c487d-122">Un nombre de idioma que identifica la referencia cultural de las cadenas localizadas en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c487d-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="c487d-123">Por ejemplo, "en-US" para inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="c487d-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="c487d-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="c487d-124">fallbackCulture</span></span> | <span data-ttu-id="c487d-125">string</span><span class="sxs-lookup"><span data-stu-id="c487d-125">string</span></span> | <span data-ttu-id="c487d-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c487d-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="c487d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c487d-127">Requirements</span></span>



| <span data-ttu-id="c487d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c487d-128">Requirement</span></span> | <span data-ttu-id="c487d-129">Value</span><span class="sxs-lookup"><span data-stu-id="c487d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c487d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c487d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c487d-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c487d-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c487d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c487d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c487d-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c487d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





