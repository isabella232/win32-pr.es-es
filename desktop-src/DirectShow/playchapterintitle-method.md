---
description: El método PlayChapterInTitle reproduce el capítulo especificado en el título especificado.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Método PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906296"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="7353c-103">Método PlayChapterInTitle</span><span class="sxs-lookup"><span data-stu-id="7353c-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="7353c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7353c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7353c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7353c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7353c-106">El `PlayChapterInTitle` método reproduce el capítulo especificado en el título especificado.</span><span class="sxs-lookup"><span data-stu-id="7353c-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="7353c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7353c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7353c-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="7353c-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="7353c-109">Especifica el título como valor entero.</span><span class="sxs-lookup"><span data-stu-id="7353c-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="7353c-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="7353c-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="7353c-111">Especifica el capítulo como valor entero.</span><span class="sxs-lookup"><span data-stu-id="7353c-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7353c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7353c-112">Return Value</span></span>

<span data-ttu-id="7353c-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7353c-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7353c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7353c-114">Remarks</span></span>

<span data-ttu-id="7353c-115">Este método inicia la reproducción en el capítulo especificado y, a continuación, continúa jugando indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="7353c-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="7353c-116">Si solo quiere reproducir un capítulo determinado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="7353c-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



