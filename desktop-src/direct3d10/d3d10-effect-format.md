---
description: Un efecto (que a menudo se almacena en un archivo con una extensión de archivo .fx) declara el estado de canalización establecido por un efecto .
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato de efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c9511304a3c24784381092017659fb1a6c593808253383443c8e9f6917c2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852835"
---
# <a name="effect-format-direct3d-10"></a>Formato de efecto (Direct3D 10)

Un efecto (que a menudo se almacena en un archivo con una extensión de archivo .fx) declara el estado de canalización establecido por un efecto . El estado del efecto se puede dividir aproximadamente en tres categorías:

-   [Variables](d3d10-effect-variable-syntax.md), que normalmente se declaran en la parte superior de un efecto.
-   [Funciones](d3d10-effect-function-syntax.md), que implementan código de sombreador, o que otras funciones usan como funciones auxiliares.
-   [Técnica ,](d3d10-effect-technique-syntax.md)que implementa secuencias de representación mediante uno o varios pases de efecto. Cada paso establece uno o varios grupos [de estados y](d3d10-effect-states.md) llama a las funciones del sombreador.

![diagrama de las categorías de estado de efecto](images/d3d10-effect-intro.png)

En el diagrama anterior se muestran las categorías de estado de efecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efecto](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



