---
description: El <iconReference> elemento especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.
title: Elemento iconReference (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997441"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="2f79a-104">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="2f79a-105">El <iconReference> elemento especifica un icono personalizado para esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2f79a-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="2f79a-106">Este elemento es opcional y no tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="2f79a-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f79a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f79a-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="2f79a-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2f79a-108">Element Information</span></span>



| <span data-ttu-id="2f79a-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2f79a-109">Parent Element</span></span>                                                               | <span data-ttu-id="2f79a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f79a-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2f79a-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="2f79a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f79a-112">Remarks</span></span>

<span data-ttu-id="2f79a-113">La referencia de icono debe especificarse en un formato adecuado para la función [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) .</span><span class="sxs-lookup"><span data-stu-id="2f79a-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="2f79a-114">Por ejemplo: `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="2f79a-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f79a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f79a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f79a-116">Elemento folderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="2f79a-117">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="2f79a-118">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="2f79a-119">Name (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="2f79a-120">Elemento ownerSID (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="2f79a-121">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="2f79a-122">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="2f79a-123">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="2f79a-124">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="2f79a-125">version (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="2f79a-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



