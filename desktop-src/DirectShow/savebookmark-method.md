---
description: El método SaveBookmark guarda la posición actual del disco y el estado del objeto MSWebDVD para que el usuario pueda volver al mismo lugar más adelante.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679437"
---
# <a name="savebookmark-method"></a><span data-ttu-id="751d1-103">Método SaveBookmark</span><span class="sxs-lookup"><span data-stu-id="751d1-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="751d1-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="751d1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="751d1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="751d1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="751d1-106">El `SaveBookmark` método guarda la posición del disco actual y el estado del objeto **MSWebDVD** para que el usuario pueda volver al mismo lugar más adelante.</span><span class="sxs-lookup"><span data-stu-id="751d1-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="751d1-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="751d1-107">Return Value</span></span>

<span data-ttu-id="751d1-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="751d1-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="751d1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="751d1-109">Remarks</span></span>

<span data-ttu-id="751d1-110">Un marcador es una instantánea del estado actual del navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="751d1-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="751d1-111">Esto incluye información como el lugar en el que se reproduce en el disco y los flujos de audio y subimágenes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="751d1-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="751d1-112">Al guardar un marcador, el usuario puede cerrar la aplicación, apagar el equipo y volver más tarde para seguir viendo el disco en el lugar en el que se quedó, con todas las opciones de configuración como antes.</span><span class="sxs-lookup"><span data-stu-id="751d1-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="751d1-113">Solo se puede guardar un marcador en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="751d1-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="751d1-114">Cuando se llama a `SaveBookmark` , se sobrescribe el marcador antiguo.</span><span class="sxs-lookup"><span data-stu-id="751d1-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="751d1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="751d1-115">Requirements</span></span>



| <span data-ttu-id="751d1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="751d1-116">Requirement</span></span> | <span data-ttu-id="751d1-117">Value</span><span class="sxs-lookup"><span data-stu-id="751d1-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="751d1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="751d1-118">Header</span></span><br/> | <dl> <span data-ttu-id="751d1-119"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="751d1-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751d1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="751d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751d1-121">**RestoreBookmark**</span><span class="sxs-lookup"><span data-stu-id="751d1-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




