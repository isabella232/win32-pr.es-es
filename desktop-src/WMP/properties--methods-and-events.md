---
title: Propiedades, métodos y eventos
description: Propiedades, métodos y eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Media Player de Windows, propiedades para el modelo de objetos
- Windows Media Player, métodos para el modelo de objetos
- Windows Media Player, eventos para el modelo de objetos
- Modelo de objetos de Windows Media Player, propiedades
- Modelo de objetos de Windows Media Player, métodos
- Modelo de objetos de Windows Media Player, eventos
- modelo de objetos, propiedades
- modelo de objetos, métodos
- modelo de objetos, eventos
- Control ActiveX de Windows Media Player, propiedades para el modelo de objetos
- Control ActiveX, propiedades del modelo de objetos
- Control ActiveX móvil de Windows Media Player, propiedades para el modelo de objetos
- Windows Media Player Mobile, propiedades para el modelo de objetos
- Control ActiveX de Windows Media Player, métodos para el modelo de objetos
- Control ActiveX, métodos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, métodos para el modelo de objetos
- Windows Media Player Mobile, métodos para el modelo de objetos
- Control ActiveX de Windows Media Player, eventos para el modelo de objetos
- Control ActiveX, eventos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, eventos para el modelo de objetos
- Windows Media Player Mobile, eventos para el modelo de objetos
- propiedades, modelo de objetos de Windows Media Player
- métodos, modelo de objetos de Windows Media Player
- eventos, modelo de objetos de Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148817"
---
# <a name="properties-methods-and-events"></a>Propiedades, métodos y eventos

Cada objeto tiene métodos y propiedades a través de los cuales puede programar el control Media Player de Windows. Un método es una acción que el objeto puede llevar A cabo. Una propiedad es un valor de datos que puede leer o cambiar. Por ejemplo, el método **Play** inicia el contenido que se reproduce y la propiedad de **velocidad** de fotogramas indica la velocidad de fotogramas actual del contenido que se reproduce.

Además, el objeto **Player** genera eventos que le ofrecen la oportunidad de llevar a cabo acciones en momentos concretos. El código se escribe en un controlador de eventos que se ejecutará cuando Windows Media Player genere el evento correspondiente. Por ejemplo, puede escribir código en un controlador de eventos **PlayStateChange** que determine si el cambio de estado es que el medio ha finalizado y, si es así, muestra un cuadro de diálogo preguntando a los usuarios si quieren reproducir el medio de nuevo.

> [!Note]  
> Todos los métodos del modelo de objetos de Windows Media Player son asíncronos. Si llama a dos métodos en el mismo procedimiento, el segundo método no puede confiar en el primer método que ha completado su acción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




