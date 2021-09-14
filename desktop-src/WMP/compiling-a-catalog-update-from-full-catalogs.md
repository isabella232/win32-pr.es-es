---
title: Compilación de una actualización de catálogo a partir de catálogos completos
description: Compilación de una actualización de catálogo a partir de catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Reproductor de Windows Media en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- tiendas en línea de tipo 1, compilar catálogos
- Reproductor de Windows Media en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tiendas en línea de tipo 1, actualizaciones del catálogo
- Reproductor de Windows Media en línea, catálogos completos
- tiendas en línea, catálogos completos
- tiendas en línea de tipo 1, catálogos completos
- compilación de catálogos
- actualizaciones del catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068486"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilación de una actualización de catálogo a partir de catálogos completos

Se puede crear una actualización de catálogo que contenga los cambios entre dos versiones de un catálogo compilado mediante la sintaxis siguiente, donde *path1* es el directorio que contiene el primer catálogo, *path2* es el directorio que contiene el segundo catálogo y la depuración se puede incluir opcionalmente para mostrar información de error detallada en la pantalla. Los archivos de catálogo deben estar en formato sin comprimir: el nombre de archivo del catálogo compilado sería catalog.wmdb, en lugar de catalog.wmdb.lz.


```C++
catcomp diff <path1> <path2> [debug]
```



Por ejemplo, si el directorio C: Catalog210 contiene la versión 210 de un catálogo compilado completo y \\ \\ C: \\ Catalog211 contiene la versión 211, el comando siguiente crea un archivo de diferencias que contiene los cambios entre las dos \\ versiones:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Para mostrar información detallada del error, puede agregar el parámetro de depuración opcional de la siguiente manera:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Si la compilación es correcta, catcomp.exe los archivos de salida que se enumeran a continuación y los guarda en el directorio que contiene el primer catálogo.



| Nombre de archivo             | Descripción                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.diff          | Archivo de diferencias compiladas sin comprimir.                                                                                                                                                           |
| catalog.diff.lz       | Versión comprimida del archivo de actualización del catálogo. El complemento puede proporcionar la ubicación de este archivo Reproductor de Windows Media [en IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| catalog.wmdb.delta    | Archivo de salida intermedio. No lo usa Reproductor de Windows Media                                                                                                                                       |
| catalog.wmdb.modified | Archivo de salida intermedio. No lo usa Reproductor de Windows Media                                                                                                                                       |



 

 

 




