---
title: Estructuras (mensajes y notificaciones de entrada de puntero)
description: Los temas de esta sección proporcionan las especificaciones de referencia para las estructuras de notificaciones y mensajes de entrada de puntero.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3bc60fc6a78b248328e2bcc44bd8f598d12bd68cc2ed61d970faeed801f62191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666125"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Estructuras de mensajes y notificaciones de entrada de puntero

Los temas de esta sección proporcionan las especificaciones de referencia para las estructuras de notificaciones y mensajes [de entrada de](messages-and-notifications-portal.md) puntero.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Define la matriz que representa una transformación en un consumidor de mensajes. Esta matriz se puede usar para transformar los datos de entrada de puntero de coordenadas de cliente a coordenadas de pantalla, mientras que el inverso se puede usar para transformar los datos de entrada de puntero de coordenadas de pantalla a coordenadas de cliente. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Contiene información básica de puntero común a todos los tipos de puntero. Las aplicaciones pueden recuperar esta información mediante las funciones [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) y [**GetPointerFrameInfoHistory.**](/previous-versions/windows/desktop/api) <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Define información básica del lápiz común a todos los tipos de puntero. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Define información táctil básica común a todos los tipos de puntero.<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | Contiene detalles de entrada de hardware que se pueden usar para predecir destinos táctiles y ayudar a compensar la latencia de hardware al procesar la entrada táctil y de gestos que contiene datos de distancia y velocidad.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de mensajes de entrada de puntero](wmpointer-reference.md)
</dt> </dl>

 

 





