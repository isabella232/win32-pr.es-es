---
title: Diferencias entre los modelos de objetos
description: Diferencias entre los modelos de objetos
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Reproductor de Windows Media,modelo de objetos
- Reproductor de Windows Media modelo de objetos, diferencias de versión
- modelo de objetos, diferencias de versión
- Reproductor de Windows Media ActiveX control, diferencias de versión
- ActiveX control de versiones, diferencias de versión
- Reproductor de Windows Media Control de ActiveX móviles, diferencias de versión
- Reproductor de Windows Media Móvil, modelo de objetos
- guía de migración, diferencias de versión
- versiones de Reproductor de Windows Media,object model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068464"
---
# <a name="differences-between-the-object-models"></a>Diferencias entre los modelos de objetos

Hay dos diferencias principales entre el modelo de objetos Reproductor de Windows Media 6.4 y el modelo de objetos Reproductor de Windows Media 7 o posterior.

-   **CLSID** El Reproductor de Windows Media de objetos 7 o posterior es una salida completa del modelo de objetos de la versión 6.4. La especificación del modelo de objetos componentes (COM) requiere que todas las interfaces existentes sigan funcionando en las nuevas versiones de un componente COM. Esto significa que se pueden agregar nuevas interfaces a un componente COM, pero las interfaces existentes nunca se deben modificar, lo que garantiza que el código de cliente anterior siempre funcionará con el componente concreto que se diseñó para usar. Por lo tanto, Reproductor de Windows Media control ActiveX 7 o posterior tiene un nuevo identificador de clase: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Si desea aprovechar la nueva funcionalidad del control para esta versión, debe cambiar el CLSID.
-   **Modelo jerárquico de objetos** Si ha estado usando el control ActiveX de Reproductor de Windows Media 6.4, es posible que haya observado que se tiene acceso a todas las propiedades, métodos y eventos a través del mismo objeto: el objeto **Player.** Por el contrario, Reproductor de Windows Media modelo de objetos 7 o posterior se organiza como una jerarquía de objetos. El **objeto Player** sigue siendo el objeto raíz, pero ahora se accede a las funciones a través de una variedad de objetos secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración de modelos de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




