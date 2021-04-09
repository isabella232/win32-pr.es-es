---
title: Código completo para la máscara simple
description: Código completo para la máscara simple
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- crear máscaras, ejemplos de código
- Aspectos de Windows Media Player, ejemplos de código
- máscaras, ejemplos de código
- archivos de definición de máscara, ejemplos de código
- crear máscaras, ejemplos
- Aspectos de Windows Media Player, ejemplos
- máscaras, ejemplos
- archivos de definición de máscara, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903623"
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



Ahora tiene todas las piezas colocadas.

Cree un archivo comprimido con la extensión de nombre de archivo. zip. Este archivo comprimido contiene el archivo de definición de máscara, los mapas de bits y los archivos multimedia digitales que desee incluir. Cambie el nombre del archivo para que tenga una extensión de nombre de archivo. WMZ. Después, al hacer doble clic en la máscara comprimida se iniciará la reproducción.

Puede ver una máscara sencilla funcional similar en la sección de ejemplos del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




