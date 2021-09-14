---
description: Un archivo de archivo de texto para una base Windows instalador lleva una extensión de nombre de archivo .idt.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de archivo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159095"
---
# <a name="archive-file-format"></a>Formato de archivo de archivo

Un [archivo de archivo de texto](text-archive-files.md) para una base Windows instalador lleva una extensión de nombre de archivo .idt. Cuando se exporta una base de datos completa a archivos de archivo, cada tabla de la base de datos tiene un archivo .idt independiente. Si una tabla contiene una columna de secuencia, cada secuencia de la tabla se representa mediante un archivo con una extensión de nombre de archivo .ibd. Los archivos .ibd se almacenan en una carpeta con el mismo nombre que la tabla.

## <a name="idt-file-format"></a>Formato de archivo .idt

El archivo .idt de una tabla de base de datos exportada que contiene solo caracteres ASCII tiene el siguiente formato básico.

-   La primera fila contiene los nombres de columna de tabla separados por pestañas.
-   La segunda fila contiene las definiciones de columna separadas por pestañas.
-   Si el archivo solo contiene datos ASCII, la tercera fila es nombre de tabla y nombres de columna de clave principal separados por pestañas.
-   Las filas restantes del archivo representan las filas de la tabla, con columnas separadas por tabulaciones.

> [!Note]  
> Si el archivo contiene datos que no son ASCII, la tercera fila es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por tabulaciones. Un archivo .idt que contiene información no ASCII debe guardarse en formato ASCII. Por ejemplo, un archivo de archivo de texto puede contener los nombres de columna y tabla codificados como UTF-8, pero el propio archivo de archivo debe ser ASCII. Consulte la sección [Datos ASCII en archivos de archivo de texto.](ascii-data-in-text-archive-files.md)

 

> [!Note]  
> Los archivos [ \_ especial ForceCodepage](-forcecodepage.md) y [ \_ SummaryInformation](-summaryinformation.md) .idt usan formatos extendidos. Consulte las \_ secciones ForceCodepage \_ y SummaryInformation para obtener descripciones de sus formatos.

 

## <a name="column-definitions"></a>Definiciones de columna

Las definiciones de columna se indican mediante caracteres.

-   El primer carácter indica el tipo de columna. Una letra minúscula indica una columna que no acepta valores NULL y una letra mayúscula indica que la columna puede contener valores NULL.

    | Carácter | Significado                   |
    |-----------|---------------------------|
    | s, S      | Columna de cadena             |
    | l, L      | Columna de cadena localizable |
    | v, V      | Columna binaria             |
    | i, I      | Columna de enteros            |

    

     

-   El segundo carácter indica el tamaño de los datos de la columna.

    > [!Note]  
    > El Windows instalador no usa realmente el tamaño de columna especificado para limitar el tamaño de la cadena que se puede especificar en un campo de columna de cadena. Sin embargo, algunas herramientas de creación usan el tamaño de columna especificado para limitar el tamaño de una cadena válida. Se recomienda que las cadenas especificadas en cualquier columna cumplan el requisito de tamaño especificado.

     

    

    | Definición de columna | Significado                                    |
    |-------------------|--------------------------------------------|
    | s255              | Columna de cadena que no acepta valores NULL 255 long        |
    | L50               | Columna de cadena localizable que acepta valores NULL 50 long |
    | i2, I2            | Columna de entero corto                       |
    | i4, I4            | Columna de entero largo                        |

    

     

## <a name="control-character-translation"></a>Traducción de caracteres de control

Al exportar una tabla a un archivo de archivo de texto, se traducen los caracteres de control para evitar conflictos con delimitadores de archivo. Al escribir en el archivo .idt, los caracteres de control se traducen como se muestra a continuación.



| Carácter de control | Traducción en .idt | Significado         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Espacio atrás      |
| HT                | 16                  | Pestaña             |
| SI                | 25                  | avance de línea       |
| FF                | 24                  | Avance de página       |
| CR                | 17                  | Retorno de carro |



 

 

 



