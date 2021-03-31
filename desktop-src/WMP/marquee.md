---
title: Marquesina
description: Marquesina
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418934"
---
# <a name="marquee"></a>Marquesina

Una marquesina es un cuadro de texto de desplazamiento que muestra información de uno o varios cuadros de presentación de texto. No es necesario agregar una marquesina, pero puede ser muy útil cuando se tiene información detallada que se desea mostrar al usuario en un espacio limitado.

El texto de la marquesina solo se desplazará si se cumplen las dos condiciones siguientes:

-   Tiene más texto que mostrar en la marquesina que el ancho del cuadro de visualización de marquesina.
-   El elemento multimedia está detenido o en pausa.

La sección de marquesina del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Marquee ]

```



> [!Note]  
> Para mantener la compatibilidad con versiones de Windows Media Player Mobile anteriores a Windows Media Player 10 Mobile, el uso de "Marquis" en un archivo de definición de máscara todavía se considera válido.

 

A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los cuadros de visualización de marquesina de la máscara.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



Puede usar la siguiente plantilla para la sección marquesina del archivo de definición de máscara:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



Debe usar el orden siguiente para obtener información en cada línea de la sección marquesina (se requiere cada parte de la línea):

1.  [Ubicación de marquesina](marquee-location.md)
2.  [Fuente de marquesina](marquee-font.md)
3.  [Color de marquesina](marquee-color.md)
4.  [Combinaciones de texto](text-combinations.md)

Para obtener un ejemplo de código de marquesina, vea [sección marquesina de ejemplo](sample-marquee-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




