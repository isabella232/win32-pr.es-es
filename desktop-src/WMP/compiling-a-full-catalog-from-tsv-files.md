---
title: Compilación de un catálogo completo a partir de archivos TSV
description: Compilación de un catálogo completo a partir de archivos TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Reproductor de Windows Media en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- tiendas en línea de tipo 1, compilar catálogos
- Reproductor de Windows Media en línea, archivos TSV
- tiendas en línea, archivos TSV
- tipo 1 tiendas en línea, archivos TSV
- Reproductor de Windows Media en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- tiendas en línea de tipo 1, catcomp.exe
- catcomp.exe
- compilación de catálogos
- archivos de valores separados por tabulaciones (TSV)
- Archivos TSV (valores separados por tabulaciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243290"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilación de un catálogo completo a partir de archivos TSV

Los nuevos catálogos se crean a partir de un conjunto de archivos de valores separados por tabulaciones (TSV). Los archivos deben estar en formato Unicode. Coloque los archivos TSV necesarios que se enumeran a continuación en una carpeta (el argumento de ruta de acceso de entrada para catcomp.exe) y llame a catcomp.exe con la sintaxis siguiente:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Si no se proporciona un número de versión, el número de versión se establecerá en 0. Si no se proporciona ningún identificador de configuración regional, se usa la configuración regional del sistema. Si solo se proporciona un argumento opcional numérico, se supone que es el número de versión. Si se especifica debug, la salida a la pantalla proporcionará información de diagnóstico más detallada.

Por ejemplo, lo siguiente compilará un catálogo a partir de los archivos de C: CatalogData 210 y dará al catálogo un número de versión \\ \\ de 210:


```C++
catcomp C:\CatalogData\210 210
```



Para mostrar mensajes de error más detallados, se puede agregar el argumento de depuración opcional, como se muestra a continuación:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Archivos TSV necesarios

Cada uno de los siguientes archivos debe estar presente, pero se puede usar un archivo vacío si no hay datos para un archivo. Por ejemplo, si el catálogo no contiene canales de radio, radio.csv puede estar vacío. Los archivos se deben denominar exactamente como se enumeran.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Aunque los nombres de archivo deben tener .csv, los archivos no están en formato de valores separados por comas (CSV). Los archivos deben estar en formato de valores separados por tabulaciones (TSV).

 

Si la compilación se realiza correctamente, catcomp.exe tres archivos de salida.



| Nombre de archivo                   | Descripción                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.wmdb                | Catálogo compilado sin comprimir.                                                                                                                                                      |
| catalog.wmdb.lz             | Catálogo en formato comprimido. El complemento puede proporcionar la ubicación de este archivo Reproductor de Windows Media [en IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| compilación \_ única \_words.txt | Un archivo de salida intermedio. No lo usa Reproductor de Windows Media.                                                                                                                      |



 

 

 




