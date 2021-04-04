---
title: Marca de espera
description: Marca de espera
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076380"
---
# <a name="the-wait-flag"></a><span data-ttu-id="1b144-104">Marca de espera</span><span class="sxs-lookup"><span data-stu-id="1b144-104">The Wait Flag</span></span>

<span data-ttu-id="1b144-105">Los comandos MCI normalmente vuelven al usuario inmediatamente, incluso si tardan varios minutos en completar la acción iniciada por el comando.</span><span class="sxs-lookup"><span data-stu-id="1b144-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="1b144-106">Puede usar la marca "Wait" ( \_ espera de MCI) para indicar al dispositivo que espere hasta que se complete la acción solicitada antes de devolver el control a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b144-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="1b144-107">Por ejemplo, el siguiente comando [**Play**](play.md) no devolverá el control a la aplicación hasta que se complete la reproducción:</span><span class="sxs-lookup"><span data-stu-id="1b144-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="1b144-108">El usuario puede cancelar una operación de espera presionando una tecla de salto.</span><span class="sxs-lookup"><span data-stu-id="1b144-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="1b144-109">De forma predeterminada, esta tecla es CTRL + INTER.</span><span class="sxs-lookup"><span data-stu-id="1b144-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="1b144-110">Las aplicaciones pueden volver a definir esta clave mediante el comando [**break**](break.md) (el [**\_ interruptor de MCI**](mci-break.md)).</span><span class="sxs-lookup"><span data-stu-id="1b144-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="1b144-111">(**El \_ salto de MCI** usa la estructura de [**parms de \_ interrupción \_ de MCI**](mci-break-parms.md) ). Cuando se cancela una operación de espera, MCI intenta devolver el control a la aplicación sin interrumpir el comando asociado a la marca "Wait".</span><span class="sxs-lookup"><span data-stu-id="1b144-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




