---
description: El método Capture captura una imagen estática del fotograma de vídeo cuando el objeto MSWebDVD está en modo sin ventanas.
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Método Capture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152043"
---
# <a name="capture-method"></a><span data-ttu-id="100e1-103">Método Capture</span><span class="sxs-lookup"><span data-stu-id="100e1-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="100e1-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="100e1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="100e1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="100e1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="100e1-106">El `Capture` método captura una imagen estática del fotograma de vídeo cuando el objeto MSWebDVD está en modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="100e1-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="100e1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="100e1-107">Remarks</span></span>

<span data-ttu-id="100e1-108">Este método captura el fotograma actual a partir de la imagen de DVD-Video y lo pega en una ventana desde la que el usuario puede guardar o editar la imagen.</span><span class="sxs-lookup"><span data-stu-id="100e1-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="100e1-109">El objeto MSWebDVD debe estar en modo sin ventanas para que este método se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="100e1-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 



