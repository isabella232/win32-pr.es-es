---
description: 'Más información sobre: Conexión a un dispositivo'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Conexión a un dispositivo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451225"
---
# <a name="connecting-to-a-device"></a>Conexión a un dispositivo

> [!Note]  
> Este sistema de scripting se ha reemplazado por Windows de automatización de adquisición de imágenes (WIA). Consulte [Windows capa de automatización de adquisición de imágenes.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

El primer paso de cualquier aplicación o script que use el modelo de scripting Windows Image Acquisition (WIA) es crear el [**objeto Wia.**](-wia-wia.md) Este objeto proporciona métodos para obtener una colección de [**objetos DeviceInfo**](-wia-deviceinfo.md) y conectar estos objetos a los dispositivos. También proporciona la capacidad de escuchar eventos de hardware de WIA.

La siguiente línea de código Visual Basic Scripting Edition (VBScript) de Microsoft crea el [**objeto Wia:**](-wia-wia.md)


```
objWia = CreateObject("Wia.Script")
```



Después de crear [**el objeto Wia,**](-wia-wia.md) use su [**método Create**](-wia-iwia-create.md) para conectarse a un dispositivo de hardware WIA.

También puede usar la propiedad [](-wia-iwia-devices.md) Devices del objeto [**Wia**](-wia-wia.md) para obtener una colección de [**objetos DeviceInfo.**](-wia-deviceinfo.md) Enumere esta colección y use [**el método Create**](-wia-iwiadeviceinfo-create.md) para conectarse a un dispositivo.

 

 
