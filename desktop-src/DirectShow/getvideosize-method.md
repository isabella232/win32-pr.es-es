---
description: El método GetVideoSize recupera las dimensiones de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Método GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677197"
---
# <a name="getvideosize-method"></a><span data-ttu-id="d4e32-103">Método GetVideoSize</span><span class="sxs-lookup"><span data-stu-id="d4e32-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="d4e32-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4e32-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d4e32-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d4e32-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d4e32-106">El `GetVideoSize` método recupera las dimensiones de vídeo nativas.</span><span class="sxs-lookup"><span data-stu-id="d4e32-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="d4e32-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4e32-107">Return Value</span></span>

<span data-ttu-id="d4e32-108">Devuelve un objeto [DVDRect](dvdrect-object.md) que contiene cuatro propiedades de lectura y escritura: (superior izquierda) x; (superior izquierda) y, ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="d4e32-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="d4e32-109">Las propiedades **x** e **y** se establecen en cero y las otras dos propiedades reflejan el ancho y el alto del rectángulo del vídeo tal como se creó en el disco.</span><span class="sxs-lookup"><span data-stu-id="d4e32-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



