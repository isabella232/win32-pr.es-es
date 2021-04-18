---
title: External. templateBeingDisplayedInLocalLibrary
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Media Player de Windows externa. templateBeingDisplayedInLocalLibrary
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699724"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="c9b57-105">External. templateBeingDisplayedInLocalLibrary</span><span class="sxs-lookup"><span data-stu-id="c9b57-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="c9b57-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="c9b57-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c9b57-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="c9b57-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c9b57-108">La propiedad **templateBeingDisplayedInLocalLibrary** indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c9b57-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b57-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9b57-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="c9b57-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c9b57-110">Possible Values</span></span>

<span data-ttu-id="c9b57-111">Esta propiedad es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9b57-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="c9b57-112">**True** indica que la fuente se muestra en el control de vista de árbol de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c9b57-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b57-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9b57-113">Remarks</span></span>

<span data-ttu-id="c9b57-114">Una página de detección que representa una fuente para una lista de reproducción dinámica puede mostrar un botón que permite al usuario "guardar" la fuente en su biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c9b57-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="c9b57-115">Guardar la fuente, en este contexto, significa que algunos metadatos se guardan en el equipo del usuario y que la fuente aparece bajo el nodo **listas de reproducción** en el control de vista de árbol de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c9b57-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="c9b57-116">El script de la página de detección puede inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** para determinar si el usuario ya ha guardado la fuente en la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c9b57-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="c9b57-117">Si el usuario ya ha guardado la fuente, la página de detección no debe mostrar el botón Guardar.</span><span class="sxs-lookup"><span data-stu-id="c9b57-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="c9b57-118">Una página de detección que representa una fuente de radio debe inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** por la misma razón.</span><span class="sxs-lookup"><span data-stu-id="c9b57-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b57-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b57-119">Requirements</span></span>



| <span data-ttu-id="c9b57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b57-120">Requirement</span></span> | <span data-ttu-id="c9b57-121">Value</span><span class="sxs-lookup"><span data-stu-id="c9b57-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b57-122">Versión</span><span class="sxs-lookup"><span data-stu-id="c9b57-122">Version</span></span><br/> | <span data-ttu-id="c9b57-123">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c9b57-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="c9b57-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9b57-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9b57-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9b57-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b57-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9b57-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b57-127">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="c9b57-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





