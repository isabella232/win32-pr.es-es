---
description: 'Cuando un dispositivo se restablece correctamente (IDirect3DDevice9:: RESET) o se crea (IDirect3D9:: CreateDevice) en las operaciones de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores del sistema.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operaciones de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714722"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="02f77-103">Operaciones de Multiple-Monitor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="02f77-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="02f77-104">Cuando un dispositivo se restablece correctamente ([**IDirect3DDevice9:: RESET**](/windows/desktop/api)) o se crea ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) en las operaciones de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="02f77-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="02f77-105">Este estado se conoce como modo exclusivo y el objeto Direct3D posee el modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="02f77-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="02f77-106">El modo exclusivo significa que los dispositivos creados por cualquier otro objeto de Direct3D no pueden asumir operaciones de pantalla completa ni asignar memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02f77-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="02f77-107">Además, cuando un objeto Direct3D asume el modo exclusivo, todos los dispositivos que no sean el que se pusieron en pantalla completa se colocarán en estado perdido.</span><span class="sxs-lookup"><span data-stu-id="02f77-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="02f77-108">Para obtener más información, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="02f77-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="02f77-109">Junto con el modo exclusivo, el objeto de Direct3D se informa de la ventana de enfoque que el dispositivo usará.</span><span class="sxs-lookup"><span data-stu-id="02f77-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="02f77-110">El modo exclusivo se libera cuando el dispositivo de pantalla completa final que posee ese objeto de Direct3D se restablece al modo de ventana o se destruye.</span><span class="sxs-lookup"><span data-stu-id="02f77-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="02f77-111">Los dispositivos se pueden dividir en dos categorías cuando un objeto de Direct3D posee el modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="02f77-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="02f77-112">La primera categoría de dispositivos tiene las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="02f77-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="02f77-113">Los crea el mismo objeto de Direct3D que creó el dispositivo que está en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="02f77-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="02f77-114">Tienen la misma ventana de foco que el dispositivo que está en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="02f77-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="02f77-115">Representan un adaptador diferente de cualquier dispositivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="02f77-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="02f77-116">Los dispositivos de esta categoría no tienen ninguna restricción en cuanto a su capacidad de restablecimiento o creación, y no se colocan en estado perdido.</span><span class="sxs-lookup"><span data-stu-id="02f77-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="02f77-117">Los dispositivos de esta categoría incluso se pueden poner en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="02f77-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="02f77-118">Los dispositivos que no están en la primera categoría: los dispositivos creados por otro objeto de Direct3D, creados con una ventana de foco diferente y creados para un adaptador con un dispositivo que ya está en pantalla completa, no se pueden restablecer y permanecen en estado perdido hasta que se pierde el modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="02f77-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="02f77-119">Como resultado, una aplicación de varios monitores puede poner varios dispositivos en modo de pantalla completa, pero solo si todos estos dispositivos son para adaptadores distintos, se crearon con el mismo objeto de Direct3D y comparten la misma ventana de foco.</span><span class="sxs-lookup"><span data-stu-id="02f77-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f77-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02f77-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f77-121">Presentación de una escena</span><span class="sxs-lookup"><span data-stu-id="02f77-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



