---
title: Elemento Resources (LocalizationType)
description: Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- elemento Resources EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695849"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="0784b-104">Elemento Resources (LocalizationType)</span><span class="sxs-lookup"><span data-stu-id="0784b-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="0784b-105">Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0784b-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0784b-106">El elemento **Resources** se define mediante el tipo complejo de [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0784b-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0784b-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0784b-107">Child elements</span></span>



| <span data-ttu-id="0784b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0784b-108">Element</span></span>                                                                  | <span data-ttu-id="0784b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0784b-109">Type</span></span>                                                                       | <span data-ttu-id="0784b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0784b-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0784b-111">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="0784b-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="0784b-112">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="0784b-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="0784b-113">Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0784b-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0784b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0784b-114">Attributes</span></span>



| <span data-ttu-id="0784b-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0784b-115">Name</span></span>    | <span data-ttu-id="0784b-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0784b-116">Type</span></span>   | <span data-ttu-id="0784b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0784b-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0784b-118">culture</span><span class="sxs-lookup"><span data-stu-id="0784b-118">culture</span></span> | <span data-ttu-id="0784b-119">string</span><span class="sxs-lookup"><span data-stu-id="0784b-119">string</span></span> | <span data-ttu-id="0784b-120">Un nombre de idioma que identifica la referencia cultural de las cadenas localizadas en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="0784b-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="0784b-121">Por ejemplo, "en-US" para inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="0784b-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0784b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0784b-122">Requirements</span></span>



| <span data-ttu-id="0784b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0784b-123">Requirement</span></span> | <span data-ttu-id="0784b-124">Value</span><span class="sxs-lookup"><span data-stu-id="0784b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0784b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0784b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0784b-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0784b-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0784b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0784b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0784b-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0784b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0784b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0784b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="0784b-130">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="0784b-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="0784b-131">**localización (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="0784b-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





