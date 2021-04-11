---
description: El método PlayChaptersAutoStop inicia la reproducción en el capítulo especificado en el título especificado y el número de capítulos especificados.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274692"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="465bb-103">Método PlayChaptersAutoStop</span><span class="sxs-lookup"><span data-stu-id="465bb-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="465bb-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="465bb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="465bb-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="465bb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="465bb-106">El `PlayChaptersAutoStop` método inicia la reproducción en el capítulo especificado en el título especificado y para el número de capítulos especificado.</span><span class="sxs-lookup"><span data-stu-id="465bb-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="465bb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="465bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="465bb-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="465bb-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="465bb-109">Especifica el título como valor entero.</span><span class="sxs-lookup"><span data-stu-id="465bb-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="465bb-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="465bb-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="465bb-111">Especifica el capítulo Inicio como valor entero.</span><span class="sxs-lookup"><span data-stu-id="465bb-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="465bb-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span><span class="sxs-lookup"><span data-stu-id="465bb-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="465bb-113">Especifica el número de capítulos que se reproducirán como valor entero.</span><span class="sxs-lookup"><span data-stu-id="465bb-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="465bb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="465bb-114">Return Value</span></span>

<span data-ttu-id="465bb-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="465bb-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="465bb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="465bb-116">Remarks</span></span>

<span data-ttu-id="465bb-117">En el momento en que se ha reproducido el último capítulo, este método hace que se envíe a la aplicación una notificación de evento de [**\_ \_ \_ reparo de capítulos del DVD**](ec-dvd-chapter-autostop.md) de la CE.</span><span class="sxs-lookup"><span data-stu-id="465bb-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



