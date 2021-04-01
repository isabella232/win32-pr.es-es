---
title: Texto (SDK de Windows Media Player)
description: Texto
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Aspectos de Windows Media Player Mobile, texto
- máscaras, texto
- referencia de máscaras, texto
- texto en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904964"
---
# <a name="text-windows-media-player-sdk"></a>Texto (SDK de Windows Media Player)

Puede que desee usar uno o varios cuadros de presentación de texto en la máscara. Cada cuadro de texto que use debe definirse en el archivo de definición de máscara. Si no define un cuadro de presentación de texto en esta sección, la máscara no podrá utilizarlo.

La sección de texto del archivo de definición de máscara comienza con esta línea:


```C++
[ Text ]

```



A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los cuadros de presentación de texto de la máscara.


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Puede usar la siguiente plantilla para la sección de texto del archivo de definición de máscara:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Debe usar el orden mostrado en la plantilla anterior para obtener información del cuadro de presentación de texto para cada línea de la sección de texto. Cada parte de la línea es obligatoria. En las secciones siguientes se describe cada elemento en detalle.

1.  [Tipo de texto](text-type.md)
2.  [Ubicación del texto](text-location.md)
3.  [Alineación del texto](text-alignment.md)
4.  [Fuente de texto](text-font.md)
5.  [Color del texto](text-color.md)

Para obtener un ejemplo de código de texto, consulte la [sección texto de ejemplo](sample-text-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




