---
title: Crear un archivo de definición de máscara
description: Crear un archivo de definición de máscara
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, crear
- crear máscaras, acerca de
- crear máscaras,Reproductor de Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341605"
---
# <a name="creating-a-skin-definition-file"></a>Crear un archivo de definición de máscara

Un archivo de definición de máscara es un archivo de texto que define una máscara y todas sus partes compuestas. La extensión de nombre de archivo debe ser .skn.

Cada archivo de definición de máscara debe comenzar con la línea siguiente, que especifica el número de versión del archivo de máscara. En la tabla siguiente se Reproductor de Windows Media y la línea de código que se debe usar para identificar cada una de ellas en un archivo de definición de máscara. Aunque algunos de los números de las líneas de código no son los esperados, son correctos, como se muestra en la tabla siguiente.



| Reproductor de Windows Media versión | Primera línea del archivo de definición de máscara |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Archivo de máscara de WMP de pocket v1.0\]      |
| 1.2                          | \[Archivo de máscara de WMP de pocket v1.2\]      |
| 7,0                          | \[Archivo de máscara de WMP de pocket v2.0\]      |
| 7.1                          | \[Archivo de máscara de WMP de pocket v8.0\]      |
| Serie 9                     | \[Archivo de máscara de WMP de pocket v9.0.1\]    |
| 10 Mobile                    | \[Archivo de máscara de WMP de pocket v9.0.1\]    |
| 10.1 Mobile                  | \[Archivo de máscara de WMP de pocket v9.0.1\]    |



 

El número de versión 9.0.1 es para máscaras creadas específicamente para Reproductor de Windows Media serie 9 o posterior. Las máscaras con un número de versión anterior se abren Reproductor de Windows Media serie 9 o posterior como modo vertical, máscaras de 96 puntos por pulgada (PPP).

El archivo de definición de máscara consta de varias secciones. Cada sección define un área concreta de la máscara. Las secciones deben colocarse en el orden siguiente:

1.  Descripción
2.  Mapas de bits
3.  Vídeo
4.  Botones
5.  Estado
6.  Texto
7.  Marquesina
8.  Barras de seguimiento

Cada sección comienza por el nombre de la sección entre corchetes, por ejemplo:


```C++
[ Bitmaps ]

```



> [!Note]  
> El archivo de definición de máscara no se analizará correctamente a menos que incluya espacios entre los corchetes y el nombre de la sección.

 

A continuación, una o varias líneas definen imágenes individuales, botones, etc. Por ejemplo, una sección Mapas de bits podría incluir lo siguiente:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



No es necesario hacer una alineación de los valores de las columnas, pero ayudará a que el código sea más legible. Para obtener más detalles sobre cada sección del archivo de definición de máscara, vea la [referencia de máscara](skin-reference.md).

> [!Note]  
> No use tabulaciones en ningún lugar del archivo; use espacios adicionales en su lugar. Esto es muy importante, ya que al presionar la tecla TAB al escribir o editar el archivo de definición de máscara, se producirá un error en toda la máscara. Cada línea debe estar completa y no puede continuar en una segunda línea. Además, los valores Región y Super están en desuso para las máscaras usadas con Reproductor de Windows Media 10 Mobile o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivo de definición de máscara**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





