---
description: Una colección es un objeto que contiene uno o más objetos. Las colecciones proporcionan una manera eficaz de agrupar objetos similares. La adquisición de imágenes de Windows (WIA) proporciona colecciones para los objetos DeviceInfo y Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Usar objetos de colección de WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696503"
---
# <a name="using-wia-collection-objects"></a><span data-ttu-id="b705a-105">Usar objetos de colección de WIA</span><span class="sxs-lookup"><span data-stu-id="b705a-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="b705a-106">Una colección es un objeto que contiene uno o más objetos.</span><span class="sxs-lookup"><span data-stu-id="b705a-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="b705a-107">Las colecciones proporcionan una manera eficaz de agrupar objetos similares.</span><span class="sxs-lookup"><span data-stu-id="b705a-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="b705a-108">La adquisición de imágenes de Windows (WIA) proporciona colecciones para los objetos [**DeviceInfo**](-wia-deviceinfo.md) y [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b705a-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="b705a-109">Use recopilaciones para enumerar los objetos que contienen.</span><span class="sxs-lookup"><span data-stu-id="b705a-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="b705a-110">Por ejemplo, en el siguiente ejemplo de VBScript se obtiene una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) del método [**Devices**](-wia-iwia-devices.md) y, a continuación, se usa un objeto **for... Cada** bucle para recorrer en iteración la colección:</span><span class="sxs-lookup"><span data-stu-id="b705a-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> <span data-ttu-id="b705a-111">Los objetos de colección WIA se basan en 0.</span><span class="sxs-lookup"><span data-stu-id="b705a-111">WIA collection objects are 0-based.</span></span>

 

 

 



