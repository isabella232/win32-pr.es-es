---
title: Texto (Reproductor de Windows Media SDK)
description: Texto
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Reproductor de Windows Media Máscaras móviles, texto
- skins,text
- referencia de máscaras,texto
- text in skins,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264748"
---
# <a name="text-windows-media-player-sdk"></a>Texto (Reproductor de Windows Media SDK)

Es posible que quiera usar uno o varios cuadros de presentación de texto en la máscara. Cada cuadro de presentación de texto que use debe definirse en el archivo de definición de máscara. Si no define un cuadro de presentación de texto en esta sección, la máscara no podrá usarla.

La sección Texto del archivo de definición de máscara comienza con esta línea:


```C++
[ Text ]

```



A continuación, debe agregar una o varias líneas que contengan información sobre cada uno de los cuadros de presentación de texto de la máscara.


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Puede usar la siguiente plantilla para la sección Texto del archivo de definición de máscara:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Debe usar el orden que se muestra en la plantilla anterior para obtener información del cuadro de presentación de texto para cada línea de la sección Texto. Se requiere cada parte de la línea. En las secciones siguientes se describe cada elemento con detalle.

1.  [Tipo de texto](text-type.md)
2.  [Ubicación de texto](text-location.md)
3.  [Alineación de texto](text-alignment.md)
4.  [Fuente de texto](text-font.md)
5.  [Color de texto](text-color.md)

Para obtener un ejemplo de código de texto, vea [Sección de texto de ejemplo](sample-text-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




