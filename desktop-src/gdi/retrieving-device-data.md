---
description: 'Las aplicaciones pueden usar las siguientes funciones para recuperar los datos del dispositivo mediante un contexto de dispositivo: GetDeviceCaps y DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recuperación de datos del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984814"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="4d6ae-103">Recuperación de datos del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d6ae-103">Retrieving Device Data</span></span>

<span data-ttu-id="4d6ae-104">Las aplicaciones pueden usar las siguientes funciones para recuperar los datos del dispositivo mediante un contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span><span class="sxs-lookup"><span data-stu-id="4d6ae-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="4d6ae-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera datos de dispositivo generales para los siguientes dispositivos:</span><span class="sxs-lookup"><span data-stu-id="4d6ae-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="4d6ae-106">Tramas, pantallas</span><span class="sxs-lookup"><span data-stu-id="4d6ae-106">Raster displays</span></span>
-   <span data-ttu-id="4d6ae-107">Impresoras matriciales</span><span class="sxs-lookup"><span data-stu-id="4d6ae-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="4d6ae-108">Impresoras de chorro de tinta</span><span class="sxs-lookup"><span data-stu-id="4d6ae-108">Ink-jet printers</span></span>
-   <span data-ttu-id="4d6ae-109">Impresoras láser</span><span class="sxs-lookup"><span data-stu-id="4d6ae-109">Laser printers</span></span>
-   <span data-ttu-id="4d6ae-110">Trazadores gráficos vectoriales</span><span class="sxs-lookup"><span data-stu-id="4d6ae-110">Vector plotters</span></span>
-   <span data-ttu-id="4d6ae-111">Cámaras de tramas</span><span class="sxs-lookup"><span data-stu-id="4d6ae-111">Raster cameras</span></span>

<span data-ttu-id="4d6ae-112">Los datos incluyen las capacidades admitidas del dispositivo, incluida la resolución del dispositivo (para pantallas de vídeo), el formato de color (para pantallas de vídeo y las impresoras de color), el número de objetos gráficos, las capacidades de trama, el dibujo de curva, el dibujo de líneas, el dibujo de polígono y el dibujo de texto.</span><span class="sxs-lookup"><span data-stu-id="4d6ae-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="4d6ae-113">Una aplicación recupera estos datos proporcionando un identificador que identifica el contexto de dispositivo adecuado, así como un índice que especifica el tipo de datos que la función va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4d6ae-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="4d6ae-114">La función [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera datos específicos de las impresoras, incluido el número de bandejas de papel disponibles, las capacidades de dúplex de la impresora, las resoluciones admitidas por la impresora, el tamaño de papel máximo y mínimo admitido, etc.</span><span class="sxs-lookup"><span data-stu-id="4d6ae-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="4d6ae-115">Una aplicación recupera estos datos proporcionando cadenas que especifican un dispositivo de impresora y un puerto, así como un índice que especifica el tipo de datos que la función va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4d6ae-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
