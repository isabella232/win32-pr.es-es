---
title: Cómo registrar un dispositivo con el host del dispositivo
description: Puede registrar un dispositivo en ejecución o un dispositivo no en ejecución.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075761"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="20048-103">Cómo registrar un dispositivo con el host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="20048-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="20048-104">Puede registrar un dispositivo en ejecución o un dispositivo no en ejecución.</span><span class="sxs-lookup"><span data-stu-id="20048-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="20048-105">Registro de un dispositivo en ejecución</span><span class="sxs-lookup"><span data-stu-id="20048-105">Registering a Running Device</span></span>

<span data-ttu-id="20048-106">Los dispositivos se registran mediante la interfaz [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="20048-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="20048-107">Solo los administradores pueden registrar los dispositivos en ejecución.</span><span class="sxs-lookup"><span data-stu-id="20048-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="20048-108">Para registrar un dispositivo que tiene un objeto de control de dispositivo en ejecución, una aplicación debe invocar [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), pasando lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="20048-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="20048-109">Texto de la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-109">The text of the device's description.</span></span>
-   <span data-ttu-id="20048-110">Un puntero **IUnknown** al objeto de control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="20048-111">Una cadena de inicialización que se pasa al método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="20048-112">Ubicación del directorio de recursos.</span><span class="sxs-lookup"><span data-stu-id="20048-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="20048-113">La duración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="20048-114">Parámetro de identificador de dispositivo (parámetro de salida), que es el valor devuelto de esta llamada; en C++ se devuelve un puntero al identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="20048-115">Registro de un dispositivo que no está en ejecución</span><span class="sxs-lookup"><span data-stu-id="20048-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="20048-116">De forma predeterminada, solo los administradores y los usuarios interactivos pueden registrar dispositivos que no están en ejecución.</span><span class="sxs-lookup"><span data-stu-id="20048-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="20048-117">Para registrar un dispositivo con un objeto de control de dispositivo que no se está ejecutando, la aplicación usa el método [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .</span><span class="sxs-lookup"><span data-stu-id="20048-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="20048-118">Para registrar un dispositivo mediante programación con un objeto de control de dispositivo que no se está ejecutando, la aplicación debe invocar [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) y pasarle los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="20048-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="20048-119">Texto de la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-119">The text of the device's description.</span></span>
-   <span data-ttu-id="20048-120">Identificador de programa (ProgID) del objeto de control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="20048-121">Una cadena de inicialización que se pasa al método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="20048-122">IDENTIFICADOR del contenedor.</span><span class="sxs-lookup"><span data-stu-id="20048-122">A container ID.</span></span>
-   <span data-ttu-id="20048-123">Ubicación del directorio de recursos.</span><span class="sxs-lookup"><span data-stu-id="20048-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="20048-124">La duración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="20048-125">Parámetro de identificador de dispositivo (parámetro de salida), que es el valor devuelto de esta llamada; en C++ se devuelve un puntero al identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20048-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="20048-126">Los registros de dispositivos no en ejecución se pueden configurar para que se conserven en los arranques del sistema (los dispositivos no se publican durante la fase de apagado).</span><span class="sxs-lookup"><span data-stu-id="20048-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="20048-127">Por lo tanto, si se configuran de esta manera, los dispositivos se publican y anuncian cada vez que se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="20048-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




