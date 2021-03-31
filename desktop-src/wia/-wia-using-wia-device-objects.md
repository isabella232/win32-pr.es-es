---
description: Un dispositivo de imagen se representa en la adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Usar objetos de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154381"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="921f4-103">Usar objetos de dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="921f4-103">Using WIA Device Objects</span></span>

<span data-ttu-id="921f4-104">Un dispositivo de imagen se representa en la adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ).</span><span class="sxs-lookup"><span data-stu-id="921f4-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="921f4-105">Normalmente, la raíz de este árbol de elementos representa el propio dispositivo, mientras que los demás elementos del árbol representan imágenes, para una cámara o regiones de digitalización, para un escáner.</span><span class="sxs-lookup"><span data-stu-id="921f4-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="921f4-106">Las aplicaciones usan el administrador de dispositivos WIA para crear y enumerar dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="921f4-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="921f4-107">En las secciones siguientes se explica cómo crear y usar dispositivos WIA:</span><span class="sxs-lookup"><span data-stu-id="921f4-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="921f4-108">Selección de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="921f4-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="921f4-109">Dispositivos de cámara WIA</span><span class="sxs-lookup"><span data-stu-id="921f4-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="921f4-110">Dispositivos WIA Scanner</span><span class="sxs-lookup"><span data-stu-id="921f4-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



