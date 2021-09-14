---
title: Propiedades, métodos y eventos
description: Propiedades, métodos y eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Reproductor de Windows Media,properties para el modelo de objetos
- Reproductor de Windows Media,methods para el modelo de objetos
- Reproductor de Windows Media,events para el modelo de objetos
- Reproductor de Windows Media de objetos, propiedades
- Reproductor de Windows Media modelo de objetos,métodos
- Reproductor de Windows Media modelo de objetos, eventos
- object model,properties
- object model,methods
- object model,events
- Reproductor de Windows Media ActiveX control,propiedades para el modelo de objetos
- ActiveX control,properties para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,propiedades para el modelo de objetos
- Reproductor de Windows Media Mobile,properties para el modelo de objetos
- Reproductor de Windows Media ActiveX control,methods para el modelo de objetos
- ActiveX control,methods para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil, métodos para el modelo de objetos
- Reproductor de Windows Media Mobile,methods para el modelo de objetos
- Reproductor de Windows Media ActiveX control,events para el modelo de objetos
- ActiveX control,events para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil, eventos para el modelo de objetos
- Reproductor de Windows Media Móvil, eventos para el modelo de objetos
- properties,Reproductor de Windows Media modelo de objetos
- methods,Reproductor de Windows Media modelo de objetos
- events,Reproductor de Windows Media modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073242"
---
# <a name="properties-methods-and-events"></a>Propiedades, métodos y eventos

Cada objeto tiene métodos y propiedades a través de los cuales puede programar Reproductor de Windows Media control. Un método es una acción que el objeto puede realizar. Una propiedad es un valor de datos que puede leer o cambiar. Por ejemplo, el **método Play** inicia la reproducción de contenido y la **propiedad frameRate** indica la velocidad de fotogramas actual del contenido que se está reproduciendo.

Además, el **objeto Player** genera eventos que le dan la oportunidad de realizar acciones en momentos específicos. El código se escribe en un controlador de eventos que se ejecutará Reproductor de Windows Media genera el evento correspondiente. Por ejemplo, puede escribir código en un controlador de eventos **PlayStateChange** que determine si el cambio de estado es que el medio finalizó y, si es así, mostrar un cuadro de diálogo que pregunte a los usuarios si quieren volver a reproducir el medio.

> [!Note]  
> Todos los métodos del modelo Reproductor de Windows Media objeto son asincrónicos. Si llama a dos métodos en el mismo procedimiento, el segundo método no puede confiar en que el primer método haya completado su acción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> </dl>

 

 




