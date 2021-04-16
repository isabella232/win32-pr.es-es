---
title: Diferencias entre los modelos de objetos
description: Diferencias entre los modelos de objetos
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, diferencias de versión
- modelo de objetos, diferencias de versión
- Control ActiveX de Windows Media Player, diferencias de versión
- Control ActiveX, diferencias de versión
- Control ActiveX móvil de Windows Media Player, diferencias de versión
- Windows Media Player Mobile, modelo de objetos
- Guía de migración, diferencias de versión
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695398"
---
# <a name="differences-between-the-object-models"></a>Diferencias entre los modelos de objetos

Hay dos diferencias principales entre el modelo de objetos de Windows Media Player 6,4 y el modelo de objetos de Windows Media Player 7 o posterior.

-   **CLSID** de El modelo de objetos de Windows Media Player 7 o posterior es una salida completa del modelo de objetos de la versión 6,4. La especificación del modelo de objetos componentes (COM) requiere que todas las interfaces existentes sigan funcionando en las nuevas versiones de un componente COM. Esto significa que se pueden agregar nuevas interfaces a un componente COM, pero las interfaces existentes no deben modificarse nunca, lo que garantiza que el código de cliente anterior funcionará siempre con el componente determinado que se diseñó para usar. Por lo tanto, el control ActiveX Windows Media Player 7 o versiones posteriores tiene un nuevo identificador de clase: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Si desea aprovechar las ventajas de la nueva funcionalidad del control para esta versión, debe cambiar el CLSID.
-   **Modelo de objetos jerárquicos** Si ha usado el control ActiveX de Windows Media Player 6,4, es posible que haya observado que se tiene acceso a todas las propiedades, métodos y eventos a través del mismo objeto: el objeto **Player** . Por el contrario, el modelo de objetos de Windows Media Player 7 o posterior se organiza como una jerarquía de objetos. El objeto **Player** sigue siendo el objeto raíz, pero ahora se tiene acceso a las funciones a través de diversos objetos secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




