---
title: Código completo para la máscara simple
description: Código completo para la máscara simple
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- crear máscaras,ejemplos de código
- Reproductor de Windows Media máscaras,ejemplos de código
- máscaras, ejemplos de código
- archivos de definición de máscara, ejemplos de código
- crear máscaras, ejemplos
- Reproductor de Windows Media máscaras, ejemplos
- máscaras, ejemplos
- archivos de definición de máscara, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b4d4380c6d7fb44290e8faff26bf5cb84dae552d09fe13594402dbe434ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135798"
---
# <a name="complete-code-for-simple-skin"></a>Código completo para la máscara simple

Este es el código completo de la primera máscara de ejemplo:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



Ahora tiene todas las piezas juntas.

Cree un archivo comprimido con una extensión .zip nombre de archivo. Este archivo comprimido contiene el archivo de definición de máscara, los mapas de bits y los archivos multimedia digitales que quiera incluir. Cambie el nombre del archivo para que tenga una extensión de nombre de archivo .wmz. Después, al hacer doble clic en la máscara comprimida, se iniciará la reproducción.

Puede ver una máscara sencilla de trabajo similar en la sección de ejemplos del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




