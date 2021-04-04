---
description: Las siguientes funciones se usan en la administración de dispositivos.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funciones de administración de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998258"
---
# <a name="device-management-functions"></a><span data-ttu-id="07722-103">Funciones de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="07722-103">Device Management Functions</span></span>

<span data-ttu-id="07722-104">Las siguientes funciones se usan en la administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="07722-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="07722-105">Función</span><span class="sxs-lookup"><span data-stu-id="07722-105">Function</span></span>                                                             | <span data-ttu-id="07722-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="07722-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="07722-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="07722-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="07722-108">Envía un código de control directamente a un controlador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="07722-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="07722-109">**InstallNewDevice**</span><span class="sxs-lookup"><span data-stu-id="07722-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="07722-110">Instala un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07722-110">Installs a new device.</span></span> <span data-ttu-id="07722-111">Se solicita al usuario que seleccione el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07722-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="07722-112">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="07722-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="07722-113">Registra el dispositivo o el tipo de dispositivo para el que una ventana recibirá notificaciones.</span><span class="sxs-lookup"><span data-stu-id="07722-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="07722-114">**UnregisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="07722-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="07722-115">Cierra el identificador de notificación de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="07722-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="07722-116">Las siguientes funciones se usan con las unidades de CD-ROM y DVD.</span><span class="sxs-lookup"><span data-stu-id="07722-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="07722-117">Función</span><span class="sxs-lookup"><span data-stu-id="07722-117">Function</span></span>                                                               | <span data-ttu-id="07722-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="07722-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07722-119">**CdromDisableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="07722-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="07722-120">Deshabilita la reproducción digital para la unidad de CD-ROM o DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="07722-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="07722-121">**CdromEnableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="07722-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="07722-122">Habilita la reproducción digital para la unidad de CD-ROM o DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="07722-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="07722-123">**CdromIsDigitalPlaybackEnabled**</span><span class="sxs-lookup"><span data-stu-id="07722-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="07722-124">Determina si la reproducción digital está habilitada para la unidad de CD-ROM o DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="07722-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="07722-125">**CdromKnownGoodDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="07722-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="07722-126">Determina si la unidad de CD-ROM o DVD especificada tiene una reproducción digital conocida.</span><span class="sxs-lookup"><span data-stu-id="07722-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="07722-127">**DvdLauncher**</span><span class="sxs-lookup"><span data-stu-id="07722-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="07722-128">Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="07722-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
