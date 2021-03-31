---
description: TAPI proporciona acceso a una pantalla de teléfonos.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154341"
---
# <a name="display"></a><span data-ttu-id="ced2d-103">Pantalla</span><span class="sxs-lookup"><span data-stu-id="ced2d-103">Display</span></span>

<span data-ttu-id="ced2d-104">TAPI proporciona acceso a la pantalla de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="ced2d-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="ced2d-105">La presentación se modela como un área alfanumérica con filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="ced2d-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="ced2d-106">Las capacidades de dispositivo de un teléfono indican el tamaño de la pantalla de un teléfono como el número de filas y el número de columnas.</span><span class="sxs-lookup"><span data-stu-id="ced2d-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="ced2d-107">Ambos números son cero si el dispositivo telefónico no tiene pantalla.</span><span class="sxs-lookup"><span data-stu-id="ced2d-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="ced2d-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) para escribir información en la pantalla de un dispositivo telefónico abierto y [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) para recuperar el contenido actual de la pantalla de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="ced2d-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="ced2d-109">Cuando se cambia la presentación de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la función de aplicación para notificar a la aplicación sobre el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="ced2d-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="ced2d-110">Los parámetros de este mensaje proporcionan una indicación del cambio.</span><span class="sxs-lookup"><span data-stu-id="ced2d-110">Parameters to this message provide an indication of the change.</span></span>

 

 



