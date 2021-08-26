---
description: Windows Los especificadores de tipo de dispositivo de adquisición de imágenes (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056975"
---
# <a name="wia-device-type-specifiers"></a>Especificadores de tipo de dispositivo WIA

Windows Los especificadores de tipo de dispositivo de adquisición de imágenes (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario. Use la macro \_ GETDEVICE TYPE para obtener estos valores de la propiedad de tipo \_ de dispositivo WIA. Los siguientes son especificadores de tipo de dispositivo WIA válidos: 

| Tipo de dispositivo                 | Significado                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| DeviceDeviceTypeDefault        | Dispositivo WIA genérico. Durante las enumeraciones de dispositivos, esta constante se usa para enumerar todos los dispositivos WIA.                         |
| DeviceDeviceTypeDigitalCamera  | El dispositivo es una cámara. *Este especificador no es compatible con Windows* Vista y versiones *posteriores.*                                     |
| DeviceDeviceTypeScanner        | El dispositivo es un escáner.                                                                                                    |
| DeviceDeviceTypeStreamingVideo | El dispositivo contiene vídeo de streaming. *Este especificador no es compatible con* Windows Server 2003, Windows Vista o versiones *posteriores.* |



 

 

 



