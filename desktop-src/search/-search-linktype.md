---
description: Especifica el tipo de vínculo durante el rastreo o la indexación.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumeración de LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705490"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="9b1b0-103">Enumeración de LINKTYPE</span><span class="sxs-lookup"><span data-stu-id="9b1b0-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="9b1b0-104">\[La enumeración **LINKTYPE** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="9b1b0-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="9b1b0-105">Especifica el tipo de vínculo durante el rastreo o la indexación.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1b0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b1b0-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="9b1b0-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b1b0-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9b1b0-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**URL de LINKTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="9b1b0-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="9b1b0-109">Especifica si se debe indizar el tipo de vínculo URL.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="9b1b0-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**contenido de LINKTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="9b1b0-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="9b1b0-111">Especifica si se debe indizar el contenido del vínculo.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="9b1b0-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**\_relacionado con LINKTYPE**</span><span class="sxs-lookup"><span data-stu-id="9b1b0-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="9b1b0-113">Especifica un vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b1b0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b1b0-114">Remarks</span></span>

<span data-ttu-id="9b1b0-115">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en los equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar las marcas de **LINKTYPE** y las siguientes API: los métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) y [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) y la estructura [**LINKINFO**](-search-linkinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9b1b0-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b1b0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b1b0-116">Requirements</span></span>



| <span data-ttu-id="9b1b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b1b0-117">Requirement</span></span> | <span data-ttu-id="9b1b0-118">Value</span><span class="sxs-lookup"><span data-stu-id="9b1b0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b1b0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b1b0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b1b0-120">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b1b0-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9b1b0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b1b0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b1b0-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b1b0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




