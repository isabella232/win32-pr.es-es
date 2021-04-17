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
# <a name="connecting-to-a-device"></a>Conexión a un dispositivo

> [!Note]  
> Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA). Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

El primer paso en cualquier aplicación o script que use el modelo de scripting de adquisición de imágenes de Windows (WIA) es crear el objeto [**WIA**](-wia-wia.md) . Este objeto proporciona métodos para que obtengan una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) y conecten estos objetos a los dispositivos. También proporciona la capacidad de escuchar eventos de hardware de WIA.

La siguiente línea de código de Microsoft Visual Basic Scripting Edition (VBScript) crea el objeto [**WIA**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Después de crear el objeto [**WIA**](-wia-wia.md) , use el método [**Create**](-wia-iwia-create.md) para conectarse a un dispositivo de hardware WIA.

También puede usar la propiedad [**dispositivos**](-wia-iwia-devices.md) del objeto [**WIA**](-wia-wia.md) para obtener una colección de objetos [**DeviceInfo**](-wia-deviceinfo.md) . Enumere esta colección y use el método [**Create**](-wia-iwiadeviceinfo-create.md) para conectarse a un dispositivo.

 

 
