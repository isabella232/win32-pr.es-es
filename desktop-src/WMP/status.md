---
title: Estado (Reproductor de Windows Media SDK)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Reproductor de Windows Media Máscaras móviles, visualización de estado
- máscaras, visualización de estado
- referencia de máscaras, visualización de estado
- mostrar el estado en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243098"
---
# <a name="status-windows-media-player-sdk"></a>Estado (Reproductor de Windows Media SDK)

Es posible que quiera usar una presentación de estado en la máscara. Si es así, el elemento status debe definirse en el archivo de definición de máscara. Como alternativa, también puede mostrar esta información mediante el atributo Status en el elemento Text.

La sección Estado del archivo de definición de máscara comienza con esta línea:


```C++
[ Status ]

```



A continuación, debe agregar una o varias líneas que contengan información sobre el estado que se muestra en la máscara.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Puede usar la siguiente plantilla para la sección Estado del archivo de definición de máscara:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Debe usar el orden que se muestra en la plantilla anterior para la información de visualización de estado de cada línea de la sección Estado. Se requiere cada parte de la línea. En las secciones siguientes se describe cada elemento:

-   [Elemento de estado](status-item.md)
-   [Ubicación de estado](status-location.md)
-   [Alineación de estado](status-alignment.md)
-   [Fuente de estado](status-font.md)
-   [Color de estado](status-color.md)

Para obtener un ejemplo de código de estado, vea [Sección de estado de ejemplo](sample-status-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




