---
title: Estructuras (mensajes de entrada de puntero y notificaciones)
description: En los temas de esta sección se proporcionan las especificaciones de referencia para los mensajes de entrada de puntero y las estructuras de notificaciones.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721635"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Mensajes de entrada de puntero y estructuras de notificaciones

En los temas de esta sección se proporcionan las especificaciones de referencia para [los mensajes de entrada de puntero y](messages-and-notifications-portal.md) las estructuras de notificaciones.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Define la matriz que representa una transformación en un consumidor de mensaje. Esta matriz se puede usar para transformar datos de entrada de puntero de coordenadas de cliente a coordenadas de pantalla, mientras que el inverso se puede usar para transformar datos de entrada de puntero de coordenadas de pantalla a coordenadas de cliente. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Contiene información de puntero básica común a todos los tipos de puntero. Las aplicaciones pueden recuperar esta información mediante las funciones [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) y [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) . <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Define la información de lápiz básica común a todos los tipos de puntero. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Define la información básica táctil común a todos los tipos de puntero.<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | Contiene los detalles de entrada de hardware que se pueden usar para predecir los destinos táctiles y ayudar a compensar la latencia de hardware al procesar la entrada táctil y de gestos que contiene datos de distancia y velocidad.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de mensajes de entrada de puntero](wmpointer-reference.md)
</dt> </dl>

 

 





