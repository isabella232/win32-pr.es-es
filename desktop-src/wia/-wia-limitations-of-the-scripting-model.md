---
description: 'Más información acerca de: limitaciones del modelo de scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitaciones del modelo de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666497"
---
# <a name="limitations-of-the-scripting-model"></a>Limitaciones del modelo de scripting

> [!Note]  
> Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA). Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

El modelo de scripting de adquisición de imágenes de Windows (WIA) expone un subconjunto de la funcionalidad de WIA. En la tabla siguiente se proporcionan descripciones de las limitaciones del modelo de scripting. 

| Funcionalidad WIA               | Restricción del modelo de scripting                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supresión de la interfaz de usuario  | No se puede suprimir la interfaz de usuario para establecer las propiedades de dispositivo/transferencia.                                                                                                                                                                                               |
| Configurar propiedades              | No se puede establecer (escribir) ninguna propiedad de dispositivo o elemento.                                                                                                                                                                                                                        |
| Registrar eventos de devolución de llamada | Solo puede recibir notificaciones para tres eventos especificados: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)y [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Control de errores                 | No se pueden controlar los errores de WIA.                                                                                                                                                                                                                                                |



 

 

 
