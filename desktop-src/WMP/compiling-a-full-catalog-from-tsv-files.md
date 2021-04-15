---
title: Compilación de un catálogo completo a partir de archivos TSV
description: Compilación de un catálogo completo a partir de archivos TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player tiendas en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- Escriba 1 tiendas en línea, compilando catálogos
- Windows Media Player tiendas en línea, archivos TSV
- tiendas en línea, archivos TSV
- tipo 1 tiendas en línea, archivos TSV
- Windows Media Player tiendas en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- Escriba 1 tiendas en línea, catcomp.exe
- catcomp.exe
- compilar catálogos
- archivos de valores separados por tabulaciones (TSV)
- Archivos TSV (con valores separados por tabuladores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695530"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilación de un catálogo completo a partir de archivos TSV

Los nuevos catálogos se crean a partir de un conjunto de archivos de valores separados por tabulaciones (TSV). Los archivos deben estar en formato Unicode. Coloque los archivos TSV necesarios que se enumeran a continuación en una carpeta (el argumento de ruta de acceso de entrada para catcomp.exe) y llame a catcomp.exe con la siguiente sintaxis:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Si no se proporciona un número de versión, el número de versión se establecerá en 0. Si no se proporciona ningún identificador de configuración regional, se utiliza la configuración regional del sistema. Si solo se proporciona un argumento opcional numérico, se supone que es el número de versión. Si se especifica debug, la salida en la pantalla proporcionará información de diagnóstico más detallada.

Por ejemplo, a continuación se compilará un catálogo a partir de los archivos de C: \\ CatalogData \\ 210 y se asignará al catálogo un número de versión de 210:


```C++
catcomp C:\CatalogData\210 210
```



Para mostrar mensajes de error más detallados, se puede Agregar el argumento opcional debug, como se indica a continuación:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Archivos TSV necesarios

Cada uno de los siguientes archivos debe estar presente, pero se puede usar un archivo vacío si no hay datos para un archivo. Por ejemplo, si el catálogo no contiene ningún canal de radio, radio.csv puede estar vacío. Los archivos se deben denominar exactamente como se muestra.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Aunque los nombres de archivo deben tener extensiones. csv, los archivos no están en formato de valores separados por comas (CSV). Los archivos deben estar en formato de valores separados por tabulaciones (TSV).

 

Si la compilación se realiza correctamente, catcomp.exe crea tres archivos de salida.



| Nombre de archivo                   | Descripción                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. wmdb                | Catálogo compilado no comprimido.                                                                                                                                                      |
| Catalog. wmdb. LZ             | Catalogar en formato comprimido. El complemento puede proporcionar la ubicación de este archivo a Windows Media Player en [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| \_words.txt únicos compilados \_ | Un archivo de salida intermedio. No lo usa Windows Media Player.                                                                                                                      |



 

 

 




