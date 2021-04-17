---
title: Enumeración ResultsDisplayStyle
description: Lo utiliza IResultsViewer ResultsStyle para establecer o determinar cómo se muestran los resultados.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Enumeración ResultsDisplayStyle características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700114"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="35d2e-104">Enumeración ResultsDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="35d2e-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="35d2e-105">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="35d2e-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="35d2e-106">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="35d2e-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="35d2e-107">Usado por [**IResultsViewer:: ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) para establecer o determinar cómo se muestran los resultados.</span><span class="sxs-lookup"><span data-stu-id="35d2e-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d2e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35d2e-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="35d2e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="35d2e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="35d2e-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span><span class="sxs-lookup"><span data-stu-id="35d2e-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="35d2e-111">Indica que los resultados se muestran como iconos pequeños.</span><span class="sxs-lookup"><span data-stu-id="35d2e-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="35d2e-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span><span class="sxs-lookup"><span data-stu-id="35d2e-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="35d2e-113">Indica que los resultados se muestran como iconos grandes.</span><span class="sxs-lookup"><span data-stu-id="35d2e-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35d2e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d2e-114">Requirements</span></span>



| <span data-ttu-id="35d2e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d2e-115">Requirement</span></span> | <span data-ttu-id="35d2e-116">Value</span><span class="sxs-lookup"><span data-stu-id="35d2e-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35d2e-117">IDL</span><span class="sxs-lookup"><span data-stu-id="35d2e-117">IDL</span></span><br/> | <dl> <span data-ttu-id="35d2e-118"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35d2e-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





