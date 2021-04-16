---
description: El método PlayChapter inicia la reproducción del capítulo especificado en el título actual.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Método PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686271"
---
# <a name="playchapter-method"></a><span data-ttu-id="cd05a-103">Método PlayChapter</span><span class="sxs-lookup"><span data-stu-id="cd05a-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="cd05a-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cd05a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cd05a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="cd05a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cd05a-106">El `PlayChapter` método inicia la reproducción del capítulo especificado en el título actual.</span><span class="sxs-lookup"><span data-stu-id="cd05a-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="cd05a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd05a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd05a-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="cd05a-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="cd05a-109">Especifica el índice del capítulo en el título actual como un entero.</span><span class="sxs-lookup"><span data-stu-id="cd05a-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd05a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd05a-110">Return Value</span></span>

<span data-ttu-id="cd05a-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cd05a-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd05a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd05a-112">Remarks</span></span>

<span data-ttu-id="cd05a-113">Cuando se alcanza el final del capítulo especificado, este método continúa reproduciendo capítulos posteriores, si existen.</span><span class="sxs-lookup"><span data-stu-id="cd05a-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="cd05a-114">Si solo quiere reproducir un capítulo especificado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="cd05a-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cd05a-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd05a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd05a-116">**PlayChapterInTitle**</span><span class="sxs-lookup"><span data-stu-id="cd05a-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



