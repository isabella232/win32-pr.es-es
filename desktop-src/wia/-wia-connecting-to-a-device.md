---
description: Más información acerca de cómo conectarse a un dispositivo
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Conexión a un dispositivo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697178"
---
# <a name="connecting-to-a-device"></a><span data-ttu-id="2de51-103">Conexión a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="2de51-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="2de51-104">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="2de51-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="2de51-105">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="2de51-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="2de51-106">El primer paso en cualquier aplicación o script que use el modelo de scripting de adquisición de imágenes de Windows (WIA) es crear el objeto [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="2de51-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="2de51-107">Este objeto proporciona métodos para que obtengan una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) y conecten estos objetos a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2de51-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="2de51-108">También proporciona la capacidad de escuchar eventos de hardware de WIA.</span><span class="sxs-lookup"><span data-stu-id="2de51-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="2de51-109">La siguiente línea de código de Microsoft Visual Basic Scripting Edition (VBScript) crea el objeto [**WIA**](-wia-wia.md) :</span><span class="sxs-lookup"><span data-stu-id="2de51-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="2de51-110">Después de crear el objeto [**WIA**](-wia-wia.md) , use el método [**Create**](-wia-iwia-create.md) para conectarse a un dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="2de51-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="2de51-111">También puede usar la propiedad [**dispositivos**](-wia-iwia-devices.md) del objeto [**WIA**](-wia-wia.md) para obtener una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2de51-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="2de51-112">Enumere esta colección y use el método [**Create**](-wia-iwiadeviceinfo-create.md) para conectarse a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2de51-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
