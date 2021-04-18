---
description: La interfaz IWindowsDriverUpdate define las siguientes propiedades.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Propiedades de IWindowsDriverUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686850"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="43edd-103">Propiedades de IWindowsDriverUpdate</span><span class="sxs-lookup"><span data-stu-id="43edd-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="43edd-104">La interfaz [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="43edd-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="43edd-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43edd-105">Property</span></span>                                                                                                    | <span data-ttu-id="43edd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="43edd-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43edd-107">[](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Dirección** de DeviceProblemNumber](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="43edd-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="43edd-108">Obtiene el número de problema del dispositivo que coincide con la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="43edd-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="43edd-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="43edd-110">Obtiene el estado del dispositivo que coincide con la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="43edd-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="43edd-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="43edd-112">Obtiene la clase de la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="43edd-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="43edd-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="43edd-114">Obtiene el identificador de hardware o el identificador compatible que debe coincidir con la actualización del controlador de Windows para poder instalarse.</span><span class="sxs-lookup"><span data-stu-id="43edd-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="43edd-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="43edd-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="43edd-116">Obtiene el nombre invariable de idioma del fabricante de la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="43edd-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="43edd-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="43edd-118">Obtiene el nombre de modelo invariable de idioma del dispositivo para el que está prevista la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="43edd-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="43edd-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="43edd-120">Obtiene el nombre de idioma invariable del proveedor de la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="43edd-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="43edd-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="43edd-122">Obtiene la fecha de la versión del controlador de la actualización del controlador de Windows.</span><span class="sxs-lookup"><span data-stu-id="43edd-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



