---
title: Enumeración PreviewDisplayStyle
description: Lo utiliza IResultsViewer PreviewStyle para establecer o determinar el estilo de presentación que se está usando actualmente.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Enumeración PreviewDisplayStyle características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700274"
---
# <a name="previewdisplaystyle-enumeration"></a><span data-ttu-id="056a5-104">Enumeración PreviewDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="056a5-104">PreviewDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="056a5-105">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="056a5-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="056a5-106">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="056a5-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="056a5-107">Usado por [**IResultsViewer::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) para establecer o determinar el estilo de presentación que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="056a5-107">Used by [**IResultsViewer::PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md) to set or determine the display style currently being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="056a5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="056a5-108">Syntax</span></span>


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="056a5-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="056a5-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="056a5-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Vista previa automática**</span><span class="sxs-lookup"><span data-stu-id="056a5-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="056a5-111">Indica la vista previa automática.</span><span class="sxs-lookup"><span data-stu-id="056a5-111">Indicates AutoPreview.</span></span>

</dd> <dt>

<span data-ttu-id="056a5-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span><span class="sxs-lookup"><span data-stu-id="056a5-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span></span>
</dt> <dd>

<span data-ttu-id="056a5-113">Indica RightPreview.</span><span class="sxs-lookup"><span data-stu-id="056a5-113">Indicates RightPreview.</span></span>

</dd> <dt>

<span data-ttu-id="056a5-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span><span class="sxs-lookup"><span data-stu-id="056a5-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span></span>
</dt> <dd>

<span data-ttu-id="056a5-115">Indica BottomPreview.</span><span class="sxs-lookup"><span data-stu-id="056a5-115">Indicates BottomPreview.</span></span>

</dd> <dt>

<span data-ttu-id="056a5-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Novista previa**</span><span class="sxs-lookup"><span data-stu-id="056a5-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="056a5-117">Indica Preview.</span><span class="sxs-lookup"><span data-stu-id="056a5-117">Indicates NoPreview.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="056a5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056a5-118">Requirements</span></span>



| <span data-ttu-id="056a5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="056a5-119">Requirement</span></span> | <span data-ttu-id="056a5-120">Value</span><span class="sxs-lookup"><span data-stu-id="056a5-120">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="056a5-121">IDL</span><span class="sxs-lookup"><span data-stu-id="056a5-121">IDL</span></span><br/> | <dl> <span data-ttu-id="056a5-122"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="056a5-122"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





