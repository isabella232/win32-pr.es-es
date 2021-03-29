---
description: Un archivo de texto para una base de datos de Windows Installer incluye una extensión de nombre de archivo. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de archivo de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909089"
---
# <a name="archive-file-format"></a>Formato de archivo de almacenamiento

Un [archivo de texto](text-archive-files.md) para una base de datos de Windows Installer incluye una extensión de nombre de archivo. IDT. Cuando se exporta una base de datos completa a archivos de almacenamiento, cada tabla de la base de datos tiene un archivo. IDT independiente. Si una tabla contiene una columna de secuencia, cada secuencia de la tabla se representa mediante un archivo con la extensión de nombre de archivo. ibd. Los archivos. ibd se almacenan en una carpeta con el mismo nombre que la tabla.

## <a name="idt-file-format"></a>Formato de archivo. IDT

El archivo. IDT de una tabla de base de datos exportada que solo contiene caracteres ASCII tiene el formato básico siguiente.

-   La primera fila contiene los nombres de columna de la tabla separados por tabulaciones.
-   La segunda fila contiene las definiciones de columna separadas por tabulaciones.
-   Si el archivo solo contiene datos ASCII, la tercera fila es el nombre de la tabla y los nombres de columna de clave principal separados por tabulaciones.
-   Las filas restantes del archivo representan las filas de la tabla, con las columnas separadas por tabulaciones.

> [!Note]  
> Si el archivo contiene datos que no son ASCII, la tercera fila es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por tabulaciones. Un archivo. IDT que contiene información no ASCII se debe guardar en formato ASCII. Por ejemplo, un archivo de almacenamiento de texto puede contener los nombres de tabla y columna codificados como UTF-8, pero el propio archivo de almacenamiento debe ser ASCII. Vea la sección [datos ASCII en archivos de almacenamiento de texto](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> Los archivos especiales [ \_ ForceCodepage](-forcecodepage.md) y [ \_ SummaryInformation](-summaryinformation.md) . IDT usan formatos extendidos. Vea las \_ secciones ForceCodepage y \_ SummaryInformation para obtener descripciones de sus formatos.

 

## <a name="column-definitions"></a>Definiciones de columna

Las definiciones de columna se indican mediante caracteres.

-   El primer carácter indica el tipo de columna. Una letra minúscula indica una columna que no admite valores NULL y una letra mayúscula indica que la columna puede contener valores NULL.

    | Carácter | Significado                   |
    |-----------|---------------------------|
    | s, S      | Columna de cadena             |
    | l, L      | Columna de cadena localizable |
    | v, V      | Columna binaria             |
    | i, I      | Columna de enteros            |

    

     

-   El segundo carácter indica el tamaño de los datos de la columna.

    > [!Note]  
    > El Windows Installer no utiliza realmente el tamaño de columna especificado para limitar el tamaño de la cadena que se puede escribir en un campo de columna de cadena. Sin embargo, algunas herramientas de creación usan el tamaño de columna especificado para limitar el tamaño de una cadena válida. Se recomienda que las cadenas especificadas en cualquier columna cumplan el requisito de tamaño especificado.

     

    

    | Definición de columna | Significado                                    |
    |-------------------|--------------------------------------------|
    | s255              | Columna de cadena que no acepta valores NULL 255 Long        |
    | L50               | Columna de cadena localizable que acepta valores NULL 50 Long |
    | I2, I2            | Columna de entero corto                       |
    | I4, I4            | Columna de entero largo                        |

    

     

## <a name="control-character-translation"></a>Traducción de caracteres de control

Exportar una tabla a un archivo de almacenamiento de texto traduce los caracteres de control para evitar conflictos con delimitadores de archivos. Al escribir en el archivo. IDT, los caracteres de control se convierten como se indica a continuación.



| Carácter de control | Traducción en. IDT | Significado         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Espacio de retroceso      |
| HT                | 16                  | Pestaña             |
| LF                | 25                  | avance de línea       |
| FF                | 24                  | Avance de formulario       |
| CR                | 17                  | Retorno de carro |



 

 

 



