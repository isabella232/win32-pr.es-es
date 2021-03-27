---
description: El sistema mantiene una caché de los contextos de dispositivo de pantalla que usa para los contextos de dispositivo comunes, primarios y de Windows.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Mostrar caché de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997409"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="09b40-103">Mostrar caché de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="09b40-103">Display Device Context Cache</span></span>

<span data-ttu-id="09b40-104">El sistema mantiene una caché de los contextos de dispositivo de pantalla que usa para los contextos de dispositivo comunes, primarios y de Windows.</span><span class="sxs-lookup"><span data-stu-id="09b40-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="09b40-105">El sistema recupera un contexto de dispositivo de la memoria caché cada vez que una aplicación llama a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; el sistema devuelve el controlador de dominio a la memoria caché cuando la aplicación llama posteriormente a la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) o [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="09b40-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="09b40-106">No hay ningún límite predeterminado en la cantidad de contextos de dispositivo que puede contener una memoria caché; el sistema crea un nuevo contexto de dispositivo de pantalla para la memoria caché si no hay ninguno disponible.</span><span class="sxs-lookup"><span data-stu-id="09b40-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="09b40-107">Dado esto, una aplicación puede tener más de cinco contextos de dispositivo activos de la memoria caché a la vez.</span><span class="sxs-lookup"><span data-stu-id="09b40-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="09b40-108">Sin embargo, la aplicación debe continuar lanzando estos contextos de dispositivo después del uso.</span><span class="sxs-lookup"><span data-stu-id="09b40-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="09b40-109">Dado que se asignan nuevos contextos de dispositivo de pantalla para la memoria caché en el espacio de montón de la aplicación, si no se liberan los contextos de dispositivo, se consume todo el espacio de montón disponible.</span><span class="sxs-lookup"><span data-stu-id="09b40-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="09b40-110">El sistema indica este error devolviendo un error cuando no se puede asignar espacio para el nuevo contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09b40-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="09b40-111">Otras funciones no relacionadas con la memoria caché también pueden devolver errores.</span><span class="sxs-lookup"><span data-stu-id="09b40-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



