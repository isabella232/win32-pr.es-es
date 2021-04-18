---
description: Los especificadores de tipo de dispositivo de adquisición de imágenes de Windows (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715179"
---
# <a name="wia-device-type-specifiers"></a>Especificadores de tipo de dispositivo WIA

Los especificadores de tipo de dispositivo de adquisición de imágenes de Windows (WIA) son constantes que indican el tipo de dispositivo conectado al equipo de un usuario. Use la \_ macro Get STIDEVICE \_ Type para obtener estos valores de la propiedad de tipo de dispositivo WIA. Los siguientes son especificadores de tipo de dispositivo WIA válidos: 

| Tipo de dispositivo                 | Significado                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Dispositivo WIA genérico. Durante las enumeraciones de dispositivos, esta constante se usa para enumerar todos los dispositivos WIA.                         |
| StiDeviceTypeDigitalCamera  | El dispositivo es una cámara. *Este especificador no es compatible con* . Windows Vista *y versiones posteriores.*                                     |
| StiDeviceTypeScanner        | El dispositivo es un escáner.                                                                                                    |
| StiDeviceTypeStreamingVideo | El dispositivo contiene vídeo de streaming. *Este especificador no es compatible con* . Windows Server 2003 *,* Windows Vista *o posterior.* |



 

 

 



