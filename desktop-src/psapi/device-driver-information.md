---
title: Información del controlador de dispositivo
description: Los controladores de dispositivos y los módulos son similares, ya que ambos se basan en archivos PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075346"
---
# <a name="device-driver-information"></a><span data-ttu-id="457a0-103">Información del controlador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="457a0-103">Device Driver Information</span></span>

<span data-ttu-id="457a0-104">Los controladores de dispositivos y los módulos son similares, ya que ambos se basan en archivos PE.</span><span class="sxs-lookup"><span data-stu-id="457a0-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="457a0-105">Sin embargo, mientras que cada proceso tiene su propia lista privada de módulos cargados, los controladores de dispositivos tienen módulos que son globales para el sistema.</span><span class="sxs-lookup"><span data-stu-id="457a0-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="457a0-106">Por lo tanto, PSAPI tiene funciones específicas para obtener la lista de controladores de dispositivos y sus nombres.</span><span class="sxs-lookup"><span data-stu-id="457a0-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="457a0-107">Puede recuperar la dirección de carga de cada controlador de dispositivo mediante una llamada a la función [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) .</span><span class="sxs-lookup"><span data-stu-id="457a0-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="457a0-108">Esta función rellena una matriz de valores de **LPVOID** con las direcciones de carga de todos los controladores de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="457a0-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="457a0-109">La función [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) toma una dirección de carga del controlador como entrada y rellena un búfer con el nombre base del controlador (por ejemplo, Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="457a0-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="457a0-110">Una función relacionada, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), toma los mismos parámetros y devuelve la ruta de acceso al controlador de dispositivo (por ejemplo, C: \\ Windows \\ system32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="457a0-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




