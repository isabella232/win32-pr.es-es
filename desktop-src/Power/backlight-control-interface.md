---
description: La interfaz de control de retroiluminación es una interfaz IOCTL normalizada para controlar el brillo de la retroiluminación de la LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaz de control de retroiluminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667231"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="8c809-103">Interfaz de control de retroiluminación</span><span class="sxs-lookup"><span data-stu-id="8c809-103">Backlight Control Interface</span></span>

<span data-ttu-id="8c809-104">La interfaz de control de retroiluminación es una interfaz IOCTL normalizada para controlar el brillo de la retroiluminación de la LCD.</span><span class="sxs-lookup"><span data-stu-id="8c809-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="8c809-105">Las aplicaciones que requieren el control mediante programación del brillo de la luz de luz o que proporcionan controles para que el usuario lo hagan deben usar esta interfaz en lugar de una interfaz de propiedad. de lo contrario, el sistema no puede consultar el brillo actual del hardware y puede quedar sin sincronizar.</span><span class="sxs-lookup"><span data-stu-id="8c809-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="8c809-106">El primer paso es consultar en el dispositivo el brillo compatible mediante el código de control de [**\_ \_ \_ \_ brillo compatible con la consulta de vídeo ioctl**](ioctl-video-query-supported-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="8c809-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="8c809-107">Esta operación devuelve un búfer que especifica los niveles de brillo disponibles.</span><span class="sxs-lookup"><span data-stu-id="8c809-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="8c809-108">Después, puede consultar el dispositivo para ver el brillo de la pantalla actual mediante la [**consulta de vídeo ioctl mostrar el código de control de \_ \_ \_ \_ brillo**](ioctl-video-query-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="8c809-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="8c809-109">Esta operación devuelve la configuración actual del brillo (AC) actual alterno, el brillo actual (DC) y el estado de la energía.</span><span class="sxs-lookup"><span data-stu-id="8c809-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="8c809-110">Para cambiar el brillo de la pantalla, use el código de control de [**\_ \_ \_ \_ brillo del conjunto de vídeos de ioctl**](ioctl-video-set-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="8c809-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="8c809-111">Puede establecer el brillo de la AC, el brillo del controlador de dominio o ambos.</span><span class="sxs-lookup"><span data-stu-id="8c809-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c809-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c809-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c809-113">Acerca de la administración de energía</span><span class="sxs-lookup"><span data-stu-id="8c809-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



