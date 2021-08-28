---
title: Comience con THEME y VIEW.
description: Comience con THEME y VIEW.
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- crear máscaras,elemento THEME
- Reproductor de Windows Media máscaras, elemento THEME
- skins,THEME, elemento
- archivos de definición de máscara, elemento THEME
- ELEMENTO THEME
- crear máscaras,elemento VIEW
- Reproductor de Windows Media máscaras, elemento VIEW
- skins,VIEW, elemento
- archivos de definición de máscara, elemento VIEW
- ELEMENTO VIEW
- elements,VIEW
- elements,THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bcb18a9d56a8780e56d81d6de60ca269036c72
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883719"
---
# <a name="start-with-theme-and-view"></a>Comience con THEME y VIEW.

Cada máscara debe tener exactamente un **elemento THEME** y al menos un **elemento VIEW.**

Con el editor de texto, cree el texto siguiente:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Deje algunas líneas en blanco antes de la **etiqueta VIEW** de cierre, ya que más adelante agregará más código aquí.

Guarde el archivo con el nombre de archivo que desee, pero asegúrese de que la extensión es .wms. Por ejemplo, un nombre de archivo típico podría ser skinone.wms.

Cada máscara debe empezar por &lt; THEME y terminar con &gt; </THEME> . Solo puede tener un **elemento THEME** en la máscara, pero debe tener uno.

También debe tener al menos un **elemento VIEW.** Puede tener más de una **vista**, pero este ejemplo solo tiene uno. Debe tener una vista de &lt; apertura y una vista de &gt; &lt; &gt; cierre. Observe que la etiqueta /VIEW de apertura no cierra la etiqueta inmediatamente, pero incluye varios atributos antes del corchete angular de cierre &lt; &gt; (>). Los atributos siguientes se usan en el **elemento THEME** de este ejemplo:

**clippingColor**

No siempre necesitará el atributo **clippingColor** si los bordes de la máscara son rectangulares. La máscara de este ejemplo tiene forma ovalada, por lo que necesita un color de recorte para las partes de la máscara a las que desea ver el escritorio; básicamente todas las partes fuera del óvalo. En esta máscara de ejemplo, usaremos un amarillo oscuro, especificado como \# "PNGC00" en formato web. Los motivos de esta elección se explican en [Creación del archivo de arte principal.](creating-the-primary-art-file.md) Básicamente, este valor siempre será un número que obtenga del programa de arte.

**backgroundImage**

Este es el nombre del archivo de arte principal. Debe ser el nombre de archivo exacto y la ruta de acceso del archivo de arte principal. Solo se admiten archivos BMP, JPG, GIF y PNG, y se recomienda BMP.

**titleBar**

Esta máscara no tiene un **titleBar,** por lo que el valor será "false". Solo querrá una barra de título si quiere que la máscara tenga un color de fondo y sea rectangular.

Asegúrese de colocar el corchete angular de cierre (>) después del valor **titleBar** para indicar que ha terminado de definir **la vista**. Deje algunas líneas en blanco antes de cerrar las etiquetas **VIEW** **y THEME.** Necesitará las líneas para el código que agregará más adelante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




