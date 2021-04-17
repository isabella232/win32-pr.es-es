---
description: Búsqueda de ubicación de cinta
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Búsqueda de ubicación de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688210"
---
# <a name="tape-location-search"></a><span data-ttu-id="50a8d-103">Búsqueda de ubicación de cinta</span><span class="sxs-lookup"><span data-stu-id="50a8d-103">Tape Location Search</span></span>

<span data-ttu-id="50a8d-104">Aunque los dispositivos DV admiten un comando para buscar por código de tiempo o por número de pista absoluta (ATN), el controlador MSDV no tiene un método estándar, independiente del dispositivo, para tener acceso a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="50a8d-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="50a8d-105">La única opción es enviar un comando AV/C sin formato al controlador, tal como se describe en el tema [emisión de comandos AV/c sin procesar](issuing-raw-av-c-commands.md).</span><span class="sxs-lookup"><span data-stu-id="50a8d-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="50a8d-106">El controlador UVC admite un conjunto de propiedades para las búsquedas de ubicaciones de cinta.</span><span class="sxs-lookup"><span data-stu-id="50a8d-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="50a8d-107">Para enviar un comando de búsqueda, use la interfaz **IKsControl** y establezca la \_ propiedad de transporte ext PROPSETID \_ .</span><span class="sxs-lookup"><span data-stu-id="50a8d-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="50a8d-108">El uso de un conjunto de propiedades es más seguro que el envío de comandos AV/C sin formato al dispositivo, ya que los comandos AV/C omiten el filtro y van directamente al controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50a8d-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50a8d-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50a8d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50a8d-110">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="50a8d-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="50a8d-111">Conjunto de propiedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="50a8d-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



