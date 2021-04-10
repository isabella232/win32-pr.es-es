---
description: Archivos de encabezado y componentes del sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Archivos de encabezado y componentes del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153407"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="71905-103">Archivos de encabezado y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="71905-103">Header Files and System Components</span></span>

<span data-ttu-id="71905-104">En la tabla siguiente se enumeran los archivos de encabezado que contienen las definiciones de interfaz para los cuatro componentes de audio principales.</span><span class="sxs-lookup"><span data-stu-id="71905-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



|                                              |                              |
|----------------------------------------------|------------------------------|
| <span data-ttu-id="71905-105">Componente de audio principal</span><span class="sxs-lookup"><span data-stu-id="71905-105">Core Audio component</span></span>                         | <span data-ttu-id="71905-106">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="71905-106">Header file</span></span>                  |
| [<span data-ttu-id="71905-107">API de MMDevice</span><span class="sxs-lookup"><span data-stu-id="71905-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="71905-108">Mmdeviceapi. h</span><span class="sxs-lookup"><span data-stu-id="71905-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="71905-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="71905-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="71905-110">Audioclient. h, Audiopolicy. h</span><span class="sxs-lookup"><span data-stu-id="71905-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="71905-111">API de DeviceTopology</span><span class="sxs-lookup"><span data-stu-id="71905-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="71905-112">Devicetopology. h</span><span class="sxs-lookup"><span data-stu-id="71905-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="71905-113">API de EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="71905-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="71905-114">Endpointvolume. h</span><span class="sxs-lookup"><span data-stu-id="71905-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="71905-115">Otro archivo de encabezado, Audiosessiontypes. h, define las constantes que usa WASAPI.</span><span class="sxs-lookup"><span data-stu-id="71905-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="71905-116">Estos archivos de encabezado se encuentran en el directorio% MSSdk% \\ include, donde% MSSdk% es el directorio raíz de la instalación de Windows SDK en el equipo.</span><span class="sxs-lookup"><span data-stu-id="71905-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="71905-117">Cada API de la tabla anterior consta de un conjunto de interfaces COM relacionadas.</span><span class="sxs-lookup"><span data-stu-id="71905-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="71905-118">Dado que algunos aspectos del streaming de audio dependen de la baja latencia y la sincronización precisa, las implementaciones de las API MMDevice, WASAPI, DeviceTopology y EndpointVolume no usan el marco de Microsoft .NET o el entorno de ejecución administrado.</span><span class="sxs-lookup"><span data-stu-id="71905-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="71905-119">Las API de audio principales se implementan en los componentes del sistema de modo usuario Audioses.dll y Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="71905-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="71905-120">Las aplicaciones cliente no tienen acceso directamente a los puntos de entrada de estos archivos dll.</span><span class="sxs-lookup"><span data-stu-id="71905-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="71905-121">En su lugar, los clientes llaman a la función **CoCreateInstance** o **CoCreateInstanceEx** para obtener la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) del objeto de la clase MMDeviceEnumerator.</span><span class="sxs-lookup"><span data-stu-id="71905-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="71905-122">Este objeto enumera los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="71905-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="71905-123">La interfaz de **IMMDeviceEnumerator** forma parte de la API de MMDevice.</span><span class="sxs-lookup"><span data-stu-id="71905-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="71905-124">Desde esta interfaz, los clientes pueden obtener directa o indirectamente las demás interfaces de la API de MMDevice, incluida la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="71905-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="71905-125">**IMMDevice** representa un dispositivo de punto de conexión de audio determinado.</span><span class="sxs-lookup"><span data-stu-id="71905-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="71905-126">A través de **IMMDevice**, los clientes pueden obtener directa o indirectamente las interfaces específicas del dispositivo en WASAPI, la API de DeviceTopology y la API de EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="71905-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="71905-127">Para obtener más información sobre **CoCreateInstance** y **CoCreateInstanceEx**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="71905-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="71905-128">Para obtener más información sobre el acceso a las interfaces en las API de audio principales, consulte [enumeración de dispositivos de audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="71905-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71905-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71905-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71905-130">Acerca de las API de audio de Windows Core</span><span class="sxs-lookup"><span data-stu-id="71905-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



