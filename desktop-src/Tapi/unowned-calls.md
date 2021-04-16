---
description: Para evitar que las llamadas no pertenecientes estén en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Llamadas no propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677419"
---
# <a name="unowned-calls"></a><span data-ttu-id="4111f-103">Llamadas no propiedad</span><span class="sxs-lookup"><span data-stu-id="4111f-103">Unowned Calls</span></span>

<span data-ttu-id="4111f-104">Para evitar que las llamadas no pertenecientes estén en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4111f-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="4111f-105">En la versión 2,0 de TAPI y versiones posteriores, TAPI llama a la función [**\_ LineDrop de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) para quitar la llamada.</span><span class="sxs-lookup"><span data-stu-id="4111f-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="4111f-106">El proveedor de servicios puede conocer de antemano si hay o no una aplicación disponible para tomar posesión de una nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="4111f-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="4111f-107">TAPI siempre informa al proveedor de servicios de los tipos de medios para los que hay una aplicación disponible mediante la función [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .</span><span class="sxs-lookup"><span data-stu-id="4111f-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="4111f-108">Por ejemplo, si un proveedor de servicios determina que hay una llamada activa en la línea que tiene el \_ modo LINEMEDIAMODE INTERACTIVEVOICE, debe comprobar la detección de medios predeterminada antes de generar los mensajes [**\_ NEWCALL**](line-newcall.md) de línea y [**\_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4111f-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="4111f-109">Si la detección de medios predeterminada muestra que ninguna aplicación está buscando una \_ llamada a LINEMEDIAMODE INTERACTIVEVOICE, el proveedor de servicios no debe enviar los mensajes porque TAPI lo quitará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4111f-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
