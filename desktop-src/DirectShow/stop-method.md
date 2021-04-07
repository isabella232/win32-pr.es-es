---
description: El método Stop detiene la reproducción.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: STOP (método) (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002610"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="0e0f4-103">STOP (método) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="0e0f4-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="0e0f4-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e0f4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0e0f4-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="0e0f4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0e0f4-106">El `Stop` método detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="0e0f4-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="0e0f4-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e0f4-107">Return Value</span></span>

<span data-ttu-id="0e0f4-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0e0f4-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0f4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e0f4-109">Remarks</span></span>

<span data-ttu-id="0e0f4-110">Si [**EnableResetOnStop**](enableresetonstop-property.md) se establece en true, la llamada a `Stop` coloca el navegador de DVD, junto con el resto del gráfico de filtro, en un estado detenido, lo que significa que la próxima vez que el usuario presione el botón **reproducir** , la reproducción comenzará al principio del disco. Si **EnableResetOnStop** se establece en true, la reproducción se reanuda donde se quedó cuando el usuario emite el siguiente comando **Play** .</span><span class="sxs-lookup"><span data-stu-id="0e0f4-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



