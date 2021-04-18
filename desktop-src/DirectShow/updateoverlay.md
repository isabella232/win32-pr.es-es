---
description: El evento UpdateOverlay se envía cuando se mueve o se cambia el tamaño de la superficie superpuesto, o cuando su clave de color ha cambiado.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671723"
---
# <a name="updateoverlay"></a><span data-ttu-id="51cf0-103">UpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="51cf0-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="51cf0-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="51cf0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="51cf0-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="51cf0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="51cf0-106">El evento **UpdateOverlay** se envía cuando se mueve o se cambia el tamaño de la superficie superpuesto, o cuando su clave de color ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="51cf0-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="51cf0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51cf0-107">Remarks</span></span>

<span data-ttu-id="51cf0-108">Las aplicaciones nunca deben preocuparse por la superficie de superposición cuyo tamaño se ha cambiado o que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="51cf0-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="51cf0-109">Todo esto se controla internamente.</span><span class="sxs-lookup"><span data-stu-id="51cf0-109">This is all handled internally.</span></span> <span data-ttu-id="51cf0-110">Pero este evento también se envía cuando cambia la clave de color.</span><span class="sxs-lookup"><span data-stu-id="51cf0-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="51cf0-111">Esto significa que si una aplicación hospeda MSWebDVD como un control sin ventana y muestra botones flotantes en la parte superior de la superficie de vídeo en el modo de pantalla completa, debe responder a este evento obteniendo el nuevo valor de la propiedad **ColorKey** para que pueda dibujar los botones correctamente.</span><span class="sxs-lookup"><span data-stu-id="51cf0-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cf0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51cf0-112">Requirements</span></span>



| <span data-ttu-id="51cf0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="51cf0-113">Requirement</span></span> | <span data-ttu-id="51cf0-114">Value</span><span class="sxs-lookup"><span data-stu-id="51cf0-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51cf0-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51cf0-115">Header</span></span><br/> | <dl> <span data-ttu-id="51cf0-116"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="51cf0-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




