---
title: Propiedades, métodos y eventos
description: Propiedades, métodos y eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Reproductor de Windows Media,properties para el modelo de objetos
- Reproductor de Windows Media,methods para el modelo de objetos
- Reproductor de Windows Media,events para el modelo de objetos
- Reproductor de Windows Media de objetos, propiedades
- Reproductor de Windows Media modelo de objetos, métodos
- Reproductor de Windows Media modelo de objetos, eventos
- object model,properties
- object model,methods
- object model,events
- Reproductor de Windows Media ActiveX control,propiedades para el modelo de objetos
- ActiveX control,propiedades para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,propiedades para el modelo de objetos
- Reproductor de Windows Media Mobile,properties para el modelo de objetos
- Reproductor de Windows Media ActiveX control,methods para el modelo de objetos
- ActiveX control,methods para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,métodos para el modelo de objetos
- Reproductor de Windows Media Mobile,methods para el modelo de objetos
- Reproductor de Windows Media ActiveX control,eventos para el modelo de objetos
- ActiveX control,eventos para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,eventos para el modelo de objetos
- Reproductor de Windows Media Mobile,events para el modelo de objetos
- properties,Reproductor de Windows Media modelo de objetos
- methods,Reproductor de Windows Media object model
- events,Reproductor de Windows Media object model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcc07977bc7ddcd2dd162600d4fa3d2822a3f52f38983ea8427f89d9403ecf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571089"
---
# <a name="properties-methods-and-events"></a>Propiedades, métodos y eventos

Cada objeto tiene métodos y propiedades a través de los cuales puede programar Reproductor de Windows Media control. Un método es una acción que el objeto puede realizar. Una propiedad es un valor de datos que puede leer o cambiar. Por ejemplo, el **método Play** inicia la reproducción de contenido y la propiedad **frameRate** indica la velocidad de fotogramas actual del contenido que se está reproduciendo.

Además, el **objeto Player** genera eventos que le dan la oportunidad de llevar a cabo acciones en momentos específicos. El código se escribe en un controlador de eventos que se ejecutará cuando Reproductor de Windows Media genera el evento correspondiente. Por ejemplo, puede escribir código en un controlador de eventos **PlayStateChange** que determine si el cambio de estado es que el medio finalizó y, si es así, mostrar un cuadro de diálogo que pregunte a los usuarios si quieren volver a reproducir el medio.

> [!Note]  
> Todos los métodos de la Reproductor de Windows Media modelo de objetos son asincrónicos. Si llama a dos métodos en el mismo procedimiento, el segundo método no puede confiar en que el primer método haya completado su acción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> </dl>

 

 




