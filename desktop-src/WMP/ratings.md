---
title: Clasificaciones
description: Clasificaciones
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Reproductor de Windows Media Máscaras móviles, clasificaciones
- máscaras, clasificaciones
- referencia de máscaras, clasificaciones
- clasificaciones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465523"
---
# <a name="ratings"></a>Clasificaciones

Al crear una máscara para Reproductor de Windows Media 10.1 Mobile, puede mostrar la clasificación asociada con el contenido basado en Windows Media Audio que se está reproduciendo actualmente. La clasificación se muestra como una estrella con un número. La estrella se numerará de uno a cinco, lo que indica la clasificación actual de ese contenido. Si el contenido no está clasificado, la estrella se numerará como cero.

La sección Clasificaciones del archivo de definición de máscara comienza con esta línea:


```C++
[ Ratings ]

```



A continuación, debe agregar una línea que contenga información sobre el tamaño y la ubicación del icono de clasificaciones en la máscara.


```C++
147, 3, 22, 21       ratings96S.gif

```



Puede usar la siguiente plantilla para la sección Clasificaciones del archivo de definición de máscara:


```C++
// <Location>           <Image>
// ---------------      --------------------
```



También puede asignar un valor de clasificación a un elemento multimedia a través de la interfaz de usuario en Reproductor de Windows Media 10.1 Mobile y la próxima vez que el dispositivo se sincronice con el equipo, el nuevo valor de clasificaciones se propagará a ese elemento multimedia si reside en la biblioteca Reproductor de Windows Media 10.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




