---
title: Empezar con el tema y la vista
description: Empezar con el tema y la vista
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- crear máscaras, elemento de tema
- Aspectos de Windows Media Player, elemento THEME
- máscaras, elemento de tema
- archivos de definición de máscara, elemento THEME
- Elemento THEME
- crear máscaras, elemento VIEW
- Aspectos de Windows Media Player, elemento VIEW
- aspectos, elemento de vista
- archivos de definición de máscara, elemento de vista
- Elemento de vista
- elementos, vista
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903815"
---
# <a name="start-with-theme-and-view"></a>Empezar con el tema y la vista

Cada máscara debe tener exactamente un elemento de **tema** y al menos un elemento de **vista** .

Con el editor de texto, cree el siguiente texto:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Deje algunas líneas en blanco antes de la etiqueta de **vista** de cierre porque agregará más código aquí más adelante.

Guarde el archivo con cualquier nombre de archivo que desee, pero asegúrese de que la extensión es. WMS. Por ejemplo, un nombre de archivo típico podría ser skinone. WMS.

Cada máscara debe empezar por <THEME> y terminar con </THEME>. Solo puede tener un elemento de **tema** en la máscara, pero debe tener uno.

También debe tener al menos un elemento de **vista** . Puede tener más de una **vista**, pero este ejemplo solo tiene una. Debe tener una apertura <VIEW> y un cierre <VIEW>. Tenga en cuenta que la etiqueta de apertura </VIEW> no cierra la etiqueta de inmediato, sino que incluye varios atributos antes del corchete angular de cierre (>). En este ejemplo se usan los siguientes atributos en el elemento **Theme** :

**clippingColor**

No siempre se necesita el atributo **clippingColor** si los bordes de la máscara son rectangulares. La máscara de este ejemplo tiene forma ovalada, por lo que necesita un color de recorte para las partes de la máscara en las que desea ver el escritorio; esencialmente, todas las partes fuera de la elipse. En esta máscara de ejemplo, usaremos un amarillo oscuro, que se especifica como " \# CCCC00" en formato web. Los motivos de esta opción se proporcionan al [crear el archivo de imagen principal](creating-the-primary-art-file.md). Esencialmente, este valor siempre será un número que se obtiene del programa de arte.

**backgroundImage**

Este es el nombre del archivo de imagen principal. Debe ser el nombre de archivo y la ruta de acceso exactos del archivo de imagen principal. Solo se admiten archivos BMP, JPG, GIF y PNG, y se recomienda usar BMP.

**titleBar**

Esta máscara no tiene una **TitleBar**, por lo que el valor será "false". Solo deseará una barra de título si desea que la máscara tenga un color de fondo y sea rectangular.

Asegúrese de colocar el corchete angular de cierre (>) después del valor de la **TitleBar** para indicar que ha terminado de definir la **vista**. Deje unas cuantas líneas en blanco antes de la **vista** de cierre y las etiquetas de **tema** . Necesitará las líneas para el código que agregará más adelante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




