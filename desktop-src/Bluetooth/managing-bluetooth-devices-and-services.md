---
title: Administración de dispositivos y servicios Bluetooth
description: Dos enfoques de programación Bluetooth principales para la programación de Windows con la interfaz de Windows Sockets y la administración de dispositivos directamente con interfaces Bluetooth que no son de socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Administración de dispositivos y servicios Bluetooth
- Dispositivos y servicios Bluetooth, administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149302"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="32a7c-105">Administración de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="32a7c-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="32a7c-106">En esta sección se describe cómo usar la API de Bluetooth para controlar directamente los dispositivos y servicios Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="32a7c-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="32a7c-107">Para obtener información sobre el uso de la interfaz de Windows Sockets para programar Bluetooth en Windows, consulte [compatibilidad con Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="32a7c-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="32a7c-108">Bluetooth no impide que las características de administración de energía interrumpan las transmisiones Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="32a7c-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="32a7c-109">Las aplicaciones habilitadas para Bluetooth pueden supervisar los mensajes de energía para evitar la interrupción.</span><span class="sxs-lookup"><span data-stu-id="32a7c-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="32a7c-110">Para obtener más información, consulte uso de la [Administración de energía](/windows/desktop/Power/using-power-management).</span><span class="sxs-lookup"><span data-stu-id="32a7c-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="32a7c-111">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="32a7c-111">This section contains the following topics.</span></span>

| <span data-ttu-id="32a7c-112">Sección</span><span class="sxs-lookup"><span data-stu-id="32a7c-112">Section</span></span>                                                                               | <span data-ttu-id="32a7c-113">Contenido</span><span class="sxs-lookup"><span data-stu-id="32a7c-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="32a7c-114">Selección de un dispositivo Bluetooth</span><span class="sxs-lookup"><span data-stu-id="32a7c-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="32a7c-115">Describe cómo seleccionar un dispositivo Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="32a7c-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="32a7c-116">Mensajes de DEVICECHANGE de Bluetooth y WM \_</span><span class="sxs-lookup"><span data-stu-id="32a7c-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="32a7c-117">Explica la interacción entre los mensajes Bluetooth y **\_ DEVICECHANGE de WM** .</span><span class="sxs-lookup"><span data-stu-id="32a7c-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 