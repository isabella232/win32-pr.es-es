---
title: Marquesina
description: Marquesina
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Reproductor de Windows Media Máscaras móviles, marques
- máscaras, marques
- referencia de máscaras, marques
- marquees en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967511"
---
# <a name="marquee"></a>Marquesina

Un marco es un cuadro de presentación de texto de desplazamiento que muestra información de uno o varios cuadros de presentación de texto. No es necesario agregar una marquesina, pero puede ser muy útil si tiene información detallada que desea mostrar al usuario en un espacio limitado.

El texto del marco solo se desplazará si se cumplen las dos condiciones siguientes:

-   Tiene más texto para mostrar en el marco que el ancho del cuadro de presentación de marquesina.
-   El elemento multimedia está detenido o en pausa.

La sección Marquee del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Marquee ]

```



> [!Note]  
> Para mantener la compatibilidad con las versiones de Reproductor de Windows Media Mobile anteriores a Reproductor de Windows Media 10 Mobile, el uso de "Ándes" en un archivo de definición de máscara todavía se considera válido.

 

A continuación, debe agregar una o varias líneas que contengan información sobre cada uno de los cuadros de presentación de marquesinas de la máscara.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



Puede usar la siguiente plantilla para la sección Marquee del archivo de definición de máscara:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



Debe usar el orden siguiente para obtener información en cada línea de la sección Marquee (se requiere cada parte de la línea):

1.  [Ubicación de marquesina](marquee-location.md)
2.  [Fuente marquesina](marquee-font.md)
3.  [Color de marquesina](marquee-color.md)
4.  [Combinaciones de texto](text-combinations.md)

Para obtener un ejemplo de código Marquee, vea [Sample Marquee Section](sample-marquee-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




