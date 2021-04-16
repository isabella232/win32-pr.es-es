---
title: Clasificaciones
description: Clasificaciones
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Aspectos de Windows Media Player Mobile, clasificaciones
- máscaras, clasificaciones
- referencia para máscaras, clasificaciones
- clasificaciones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714217"
---
# <a name="ratings"></a>Clasificaciones

Al crear una máscara para Windows Media Player 10,1 Mobile, puede mostrar la clasificación asociada al contenido basado en Windows Media Audio que se está reproduciendo actualmente. La clasificación se muestra en forma de estrella con un número. La estrella se numerará de una a cinco, lo que indica la clasificación actual del contenido. Si no se clasifica el contenido, la estrella se numerará como cero.

La sección clasificaciones del archivo de definición de máscara comienza con esta línea:


```C++
[ Ratings ]

```



A continuación, debe agregar una línea que contenga información sobre el tamaño y la ubicación del icono de clasificación en la máscara.


```C++
147, 3, 22, 21       ratings96S.gif

```



Puede usar la siguiente plantilla para la sección clasificaciones del archivo de definición de máscara:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



También puede asignar un valor de clasificación a un elemento multimedia a través de la interfaz de usuario en Windows Media Player 10,1 Mobile y la próxima vez que el dispositivo se sincronice con el equipo, el nuevo valor de clasificación se propagará a ese elemento multimedia si reside en la biblioteca de Windows Media Player 10.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




