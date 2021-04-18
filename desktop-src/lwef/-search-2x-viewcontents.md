---
title: Enumeración ViewContents
description: Utilizado por el contenido de IResultsViewer para indicar o establecer cómo se muestra el conjunto de devoluciones de la consulta actual.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Enumeración ViewContents características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700372"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="375b7-104">Enumeración ViewContents</span><span class="sxs-lookup"><span data-stu-id="375b7-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="375b7-105">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="375b7-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="375b7-106">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="375b7-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="375b7-107">Usado por [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) para indicar o establecer cómo se muestra el conjunto de devoluciones de la consulta actual.</span><span class="sxs-lookup"><span data-stu-id="375b7-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="375b7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="375b7-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="375b7-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="375b7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="375b7-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span><span class="sxs-lookup"><span data-stu-id="375b7-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="375b7-111">Indica el tipo de contenido que se muestra en la vista de resultados.</span><span class="sxs-lookup"><span data-stu-id="375b7-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="375b7-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span><span class="sxs-lookup"><span data-stu-id="375b7-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="375b7-113">Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista de Shell.</span><span class="sxs-lookup"><span data-stu-id="375b7-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="375b7-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span><span class="sxs-lookup"><span data-stu-id="375b7-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="375b7-115">Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista de explorador.</span><span class="sxs-lookup"><span data-stu-id="375b7-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="375b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="375b7-116">Requirements</span></span>



| <span data-ttu-id="375b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="375b7-117">Requirement</span></span> | <span data-ttu-id="375b7-118">Value</span><span class="sxs-lookup"><span data-stu-id="375b7-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="375b7-119">IDL</span><span class="sxs-lookup"><span data-stu-id="375b7-119">IDL</span></span><br/> | <dl> <span data-ttu-id="375b7-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="375b7-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





