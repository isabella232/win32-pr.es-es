---
title: Extensiones de dispositivo para la transferencia de metadatos acelerada
description: Extensiones de dispositivo para la transferencia de metadatos acelerada
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Windows Media Player, transferencia acelerada de metadatos
- Windows Media Player, transferencia acelerada de metadatos
- transferencia acelerada de metadatos
- metadatos, transferencia acelerada
- extensiones de dispositivo, transferencia acelerada de metadatos
- extensiones, transferencia de metadatos acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075973"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="c4903-111">Extensiones de dispositivo para la transferencia de metadatos acelerada</span><span class="sxs-lookup"><span data-stu-id="c4903-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="c4903-112">Windows Media Player 10 incorporó la funcionalidad nueva y extendida para la sincronización de archivos multimedia digitales con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="c4903-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="c4903-113">Los usuarios pueden conectar un dispositivo a un equipo, transferir contenido al dispositivo y, a continuación, desconectar el dispositivo para disfrutar del contenido fuera del equipo.</span><span class="sxs-lookup"><span data-stu-id="c4903-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="c4903-114">Cuando el usuario vuelve a conectar el dispositivo al equipo, es posible que el contenido almacenado en el dispositivo haya cambiado desde la conexión anterior.</span><span class="sxs-lookup"><span data-stu-id="c4903-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="c4903-115">Por ejemplo, simplemente reproducir un archivo multimedia digital determinado hace que el recuento de reproducción de ese elemento cambie.</span><span class="sxs-lookup"><span data-stu-id="c4903-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="c4903-116">Dado que los dispositivos portátiles actuales pueden almacenar grandes cantidades de contenido multimedia digital, el proceso de detección de cambios sería demasiado lento si se requería Windows Media Player para enumerar e inspeccionar cada elemento multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="c4903-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="c4903-117">En su lugar, los fabricantes de dispositivos portátiles pueden implementar una funcionalidad especial para habilitar Windows Media Player 10 o una versión posterior para recuperar de forma eficaz la información sobre los cambios realizados en el contenido almacenado en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4903-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="c4903-118">En las secciones siguientes se describen las convenciones que se usan para implementar esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c4903-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="c4903-119">Acerca de los metadatos</span><span class="sxs-lookup"><span data-stu-id="c4903-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="c4903-120">Extensiones de dispositivo MTP para transferencia de metadatos</span><span class="sxs-lookup"><span data-stu-id="c4903-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="c4903-121">Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos</span><span class="sxs-lookup"><span data-stu-id="c4903-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="c4903-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4903-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4903-123">**Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c4903-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




