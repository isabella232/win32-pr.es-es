---
title: Estado (SDK de Windows Media Player)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Aspectos de Windows Media Player Mobile, presentación de estado
- máscaras, presentación de estado
- referencia de máscaras, presentación de estado
- presentación de estado en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078693"
---
# <a name="status-windows-media-player-sdk"></a>Estado (SDK de Windows Media Player)

Puede que desee usar una pantalla de estado en la máscara. En ese caso, el elemento de estado se debe definir en el archivo de definición de máscara. Como alternativa, también puede mostrar esta información mediante el atributo status en el elemento de texto.

La sección de estado del archivo de definición de máscara comienza con esta línea:


```C++
[ Status ]

```



A continuación, debe agregar una o más líneas que contengan información sobre la presentación de estado en la máscara.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Puede usar la siguiente plantilla para la sección de estado del archivo de definición de máscara:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Debe usar el orden mostrado en la plantilla anterior para ver la información de visualización de estado de cada línea en la sección estado. Cada parte de la línea es obligatoria. En las secciones siguientes se describe cada elemento:

-   [Elemento de estado](status-item.md)
-   [Ubicación de estado](status-location.md)
-   [Alineación del estado](status-alignment.md)
-   [Fuente de estado](status-font.md)
-   [Color de estado](status-color.md)

Para obtener un ejemplo de código de estado, consulte la [sección estado de ejemplo](sample-status-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




