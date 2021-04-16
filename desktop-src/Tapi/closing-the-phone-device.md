---
description: La función phoneClose cierra el dispositivo de teléfono especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Cierre del dispositivo teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543003"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="af421-103">Cierre del dispositivo teléfono</span><span class="sxs-lookup"><span data-stu-id="af421-103">Closing the Phone Device</span></span>

<span data-ttu-id="af421-104">La función [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) cierra el dispositivo de teléfono especificado.</span><span class="sxs-lookup"><span data-stu-id="af421-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="af421-105">El dispositivo telefónico también se puede cerrar forzosamente después de que el usuario haya modificado la configuración de ese teléfono o su controlador.</span><span class="sxs-lookup"><span data-stu-id="af421-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="af421-106">Si el usuario desea que los cambios de configuración surtan efecto inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="af421-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="af421-107">Estos mensajes también se pueden enviar de forma no solicitada como resultado de la recuperación del dispositivo telefónico de otra manera.</span><span class="sxs-lookup"><span data-stu-id="af421-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="af421-108">Por lo tanto, una aplicación debe estar preparada para controlar mensajes de [**\_ cierre de teléfono**](phone-close.md) no solicitados.</span><span class="sxs-lookup"><span data-stu-id="af421-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="af421-109">En el momento en que se cierra el dispositivo telefónico, se suprime cualquier respuesta asincrónica pendiente que pertenezca a ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af421-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



