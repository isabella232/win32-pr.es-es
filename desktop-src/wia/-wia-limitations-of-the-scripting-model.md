---
description: 'Más información sobre: Limitaciones del modelo de scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitaciones del modelo de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208067"
---
# <a name="limitations-of-the-scripting-model"></a>Limitaciones del modelo de scripting

> [!Note]  
> Este sistema de scripting se ha reemplazado por Windows de automatización de adquisición de imágenes (WIA). Consulte [Windows capa de automatización de adquisición de imágenes.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

El Windows de scripting de adquisición de imágenes (WIA) expone un subconjunto de funcionalidad de WIA. En la tabla siguiente se proporcionan descripciones de las limitaciones del modelo de scripting. 

| Funcionalidad de WIA               | Limitación del modelo de scripting                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supresión de la interfaz de usuario  | No se puede suprimir la interfaz de usuario para establecer propiedades de transferencia o dispositivo.                                                                                                                                                                                               |
| Configurar propiedades              | No se puede establecer (escribir) ninguna propiedad de dispositivo o elemento.                                                                                                                                                                                                                        |
| Registro de eventos de devolución de llamada | Solo puede recibir notificaciones de tres eventos especificados: [**OnTransferComplete,**](-wia--iwiaevents-ontransfercomplete.md) [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)y [**OnDeviceDisconnected.**](-wia--iwiaevents-ondevicedisconnected.md) |
| Control de errores                 | No se pueden controlar los errores de WIA.                                                                                                                                                                                                                                                |



 

 

 
