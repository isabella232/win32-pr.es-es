---
title: Habilitar la sincronización con Windows Media Player
description: Habilitar la sincronización con Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Administrador de dispositivos, sincronización con Windows Media Player
- Administrador de dispositivos, sincronización con Media Player de Windows
- Guía de programación, sincronización con Windows Media Player
- proveedores de servicios, sincronización con Windows Media Player
- crear proveedores de servicios, sincronización con Windows Media Player
- sincronización con Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695486"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="90e98-109">Habilitar la sincronización con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="90e98-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="90e98-110">Puede habilitar un dispositivo para que participe en la sincronización automática con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="90e98-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="90e98-111">La sincronización automática significa que cuando un dispositivo sincronizado designado por el usuario se conecta al equipo, Windows Media Player descargará, actualizará o eliminará automáticamente archivos del dispositivo sin necesidad de proporcionar ninguna entrada adicional por parte del usuario.</span><span class="sxs-lookup"><span data-stu-id="90e98-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="90e98-112">De forma predeterminada, los siguientes dispositivos están sincronizados con Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="90e98-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="90e98-113">Dispositivos MTP</span><span class="sxs-lookup"><span data-stu-id="90e98-113">MTP devices</span></span>
-   <span data-ttu-id="90e98-114">Dispositivos de almacenamiento masivo</span><span class="sxs-lookup"><span data-stu-id="90e98-114">Mass-storage devices</span></span>
-   <span data-ttu-id="90e98-115">Dispositivos Windows CE (Windows Media Player 10 Mobile y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="90e98-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="90e98-116">Para que cualquier otro dispositivo se sincronice con Windows Media Player, deben cumplirse los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="90e98-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="90e98-117">El dispositivo debe anunciar una interfaz de dispositivo PAP {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span><span class="sxs-lookup"><span data-stu-id="90e98-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="90e98-118">Los objetos de dispositivo devueltos por el proveedor de servicios deben admitir la interfaz **IMDSPDevice3** .</span><span class="sxs-lookup"><span data-stu-id="90e98-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="90e98-119">El parámetro de dispositivo UseExtendedWmdm debe establecerse en un valor **DWORD** de 1.</span><span class="sxs-lookup"><span data-stu-id="90e98-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="90e98-120">Consulte [parámetros del dispositivo](device-parameters.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="90e98-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="90e98-121">El proveedor de servicios debe implementar las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="90e98-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="90e98-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="90e98-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="90e98-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="90e98-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="90e98-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="90e98-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="90e98-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90e98-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e98-126">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="90e98-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="90e98-127">**Parámetros del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="90e98-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




