---
title: Crear un archivo de definición de máscara
description: Crear un archivo de definición de máscara
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Máscaras móviles de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, crear
- crear máscaras, acerca de
- crear máscaras, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777257"
---
# <a name="creating-a-skin-definition-file"></a>Crear un archivo de definición de máscara

Un archivo de definición de máscara es un archivo de texto que define una máscara y todas sus partes compuestas. La extensión de nombre de archivo debe ser. SKN.

Cada archivo de definición de máscara debe comenzar con la línea siguiente, que especifica el número de versión del archivo de máscara. En la tabla siguiente se muestran las versiones de Windows Media Player y la línea de código que se debe usar para identificar cada una de ellas en un archivo de definición de máscara. Aunque algunos de los números de las líneas de código no son los que cabría esperar, son correctos como se muestra en la tabla siguiente.



| Versión de Windows Media Player | Primera línea del archivo de definición de máscara |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Archivo de máscara de Pocket WMP v 1.0\]      |
| 1.2                          | \[Archivo de máscara de Pocket WMP v 1.2\]      |
| 7.0                          | \[Archivo de máscara de Pocket WMP v 2.0\]      |
| 7.1                          | \[Archivo de máscara de Pocket WMP v 8.0\]      |
| Series 9                     | \[Archivo de máscara de Pocket WMP v 9.0.1\]    |
| 10 Mobile                    | \[Archivo de máscara de Pocket WMP v 9.0.1\]    |
| móvil 10,1                  | \[Archivo de máscara de Pocket WMP v 9.0.1\]    |



 

El número de versión 9.0.1 es para las máscaras creadas específicamente para Windows Media Player 9 series o posterior. Las máscaras que tienen un número de versión anterior se abren con Windows Media Player 9 series o posterior como modo vertical, con máscaras de 96 puntos por pulgada (PPP).

El archivo de definición de máscara consta de varias secciones. Cada sección define un área determinada de la máscara. Las secciones se deben colocar en el orden siguiente:

1.  Descripción
2.  Mapas de bits
3.  Vídeo
4.  Botones
5.  Status
6.  Texto
7.  Marquesina
8.  Trackbars

Cada sección comienza con el nombre de la sección entre corchetes, por ejemplo:


```C++
[ Bitmaps ]

```



> [!Note]  
> El archivo de definición de máscara no se analizará correctamente a menos que incluya espacios entre los corchetes y el nombre de la sección.

 

A continuación, una o más líneas definen imágenes individuales, botones, etc. Por ejemplo, una sección de mapas de bits podría incluir lo siguiente:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



No es necesario alinear los valores de las columnas, pero ayudará a que el código sea más legible. Para obtener más información sobre cada sección del archivo de definición de máscara, vea la referencia de la [máscara](skin-reference.md).

> [!Note]  
> No use pestañas en ningún lugar del archivo; en su lugar, use espacios adicionales. Esto es muy importante, ya que si se presiona la tecla TAB mientras se escribe o edita el archivo de definición de máscara, se producirá un error en toda la máscara. Cada línea debe estar completa y no puede continuar en una segunda línea. Además, la región y los súper valores están desusados para las máscaras usadas con Windows Media Player 10 Mobile o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivo de definición de máscara**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





