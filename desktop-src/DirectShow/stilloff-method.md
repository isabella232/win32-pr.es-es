---
description: El método StillOff reanuda la reproducción y cancela el modo todavía.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Método StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687868"
---
# <a name="stilloff-method"></a><span data-ttu-id="acea4-103">Método StillOff</span><span class="sxs-lookup"><span data-stu-id="acea4-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="acea4-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="acea4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="acea4-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="acea4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="acea4-106">El `StillOff` método reanuda la reproducción y cancela el modo todavía.</span><span class="sxs-lookup"><span data-stu-id="acea4-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="acea4-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acea4-107">Return Value</span></span>

<span data-ttu-id="acea4-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="acea4-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acea4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acea4-109">Remarks</span></span>

<span data-ttu-id="acea4-110">El [navegador de DVD](dvd-navigator-filter.md) entra en modo todavía cuando encuentra un marco fijo creado en el disco. Notifica a la aplicación mediante el envío de un \_ DVD \_ de EC todavía \_ en el evento.</span><span class="sxs-lookup"><span data-stu-id="acea4-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="acea4-111">El modo todavía es diferente del explorador de DVD que se encuentra en un estado de pausa debido a una operación de usuario.</span><span class="sxs-lookup"><span data-stu-id="acea4-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="acea4-112">La llamada a `StillOff` reanuda la reproducción del modo todavía, pero no reinicia el navegador de DVD cuando está en un estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="acea4-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



