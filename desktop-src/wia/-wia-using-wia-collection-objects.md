---
description: Una colección es un objeto que contiene uno o varios objetos . Las colecciones proporcionan una manera eficaz de agrupar objetos similares. Windows Adquisición de imágenes (WIA) proporciona colecciones para los objetos DeviceInfo y Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Uso de objetos de colección de WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 58a4003394bcc163e9013914da6797a504ec16582b8bfac7915d7a49947c18f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813515"
---
# <a name="using-wia-collection-objects"></a>Uso de objetos de colección de WIA

Una colección es un objeto que contiene uno o varios objetos . Las colecciones proporcionan una manera eficaz de agrupar objetos similares. Windows Adquisición de imágenes (WIA) proporciona colecciones para los [**objetos DeviceInfo**](-wia-deviceinfo.md) [**y Item.**](-wia-item.md)

Use colecciones para enumerar los objetos que contienen. Por ejemplo, en el siguiente ejemplo de VBScript se obtiene una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) del método [**Devices**](-wia-iwia-devices.md) y, a continuación, se usa **for... Cada** bucle para recorrer en iteración la colección:


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
> Los objetos de colección WIA se basan en 0.

 

 

 



