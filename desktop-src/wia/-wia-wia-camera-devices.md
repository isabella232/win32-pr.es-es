---
description: WIA representa un dispositivo de cámara como un árbol jerárquico de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de cámara WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275449"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="4bcd8-103">Dispositivos de cámara WIA</span><span class="sxs-lookup"><span data-stu-id="4bcd8-103">WIA Camera Devices</span></span>

<span data-ttu-id="4bcd8-104">WIA representa un dispositivo de cámara como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="4bcd8-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="4bcd8-105">El elemento raíz, devuelto desde una llamada al método [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) del administrador de dispositivos de adquisición de imágenes de Windows (WIA), se usa para obtener y establecer la información del dispositivo, para controlar el dispositivo y para iniciar la enumeración de elementos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="4bcd8-106">WIA no admite cámaras en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="4bcd8-107">En el caso de las versiones de Windows, use la API de dispositivo portátil de Windows (WPD) que se describe en el kit de desarrollo de controladores de Windows (DDK) para adquirir imágenes de cámaras.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="4bcd8-108">En el diagrama siguiente se muestra una implementación de cámara de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="4bcd8-109">El elemento raíz de la cámara tiene tres elementos secundarios, dos imágenes y una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="4bcd8-110">La carpeta tiene dos elementos secundarios, ambas imágenes.</span><span class="sxs-lookup"><span data-stu-id="4bcd8-110">The folder has two child items, both pictures.</span></span>

![implementación de la cámara de ejemplo](images/wihierar.gif)

 

 



