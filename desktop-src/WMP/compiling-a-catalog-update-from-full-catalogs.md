---
title: Compilar una actualización de catálogo a partir de catálogos completos
description: Compilar una actualización de catálogo a partir de catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Reproductor de Windows Media en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- tiendas en línea de tipo 1, compilar catálogos
- Reproductor de Windows Media en línea, actualizaciones de catálogo
- tiendas en línea, actualizaciones de catálogo
- tiendas en línea de tipo 1, actualizaciones de catálogo
- Reproductor de Windows Media en línea, catálogos completos
- tiendas en línea, catálogos completos
- tiendas en línea de tipo 1, catálogos completos
- compilar catálogos
- actualizaciones del catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306412d98f315a6a63aa40974b03a51a388b6db5c9e09c8d5b8907ef2cc15704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763955"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilar una actualización de catálogo a partir de catálogos completos

Se puede crear una actualización de catálogo que contenga los cambios entre dos versiones de un catálogo compilado mediante la sintaxis siguiente, donde *path1* es el directorio que contiene el primer catálogo, *path2* es el directorio que contiene el segundo catálogo y la depuración se puede incluir opcionalmente para mostrar información detallada del error en la pantalla. Los archivos de catálogo deben estar en formato sin comprimir: el nombre de archivo del catálogo compilado sería catalog.wmdb, en lugar de catalog.wmdb.lz.


```C++
catcomp diff <path1> <path2> [debug]
```



Por ejemplo, si el directorio C: Catalog210 contiene la versión 210 de un catálogo compilado completo y \\ \\ C: \\ Catalog211 contiene la versión 211, el siguiente comando crea un archivo de diferencia que contiene los cambios entre las dos \\ versiones:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Para mostrar información detallada del error, puede agregar el parámetro de depuración opcional como se muestra a continuación:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Si la compilación es correcta, catcomp.exe los archivos de salida enumerados a continuación y los guarda en el directorio que contiene el primer catálogo.



| Nombre de archivo             | Descripción                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.diff          | Archivo de diferencia compilado sin comprimir.                                                                                                                                                           |
| catalog.diff.lz       | Versión comprimida del archivo de actualización del catálogo. El complemento puede proporcionar la ubicación de este archivo Reproductor de Windows Media en [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| catalog.wmdb.delta    | Archivo de salida intermedio. No lo usa Reproductor de Windows Media                                                                                                                                       |
| catalog.wmdb.modified | Archivo de salida intermedio. No lo usa Reproductor de Windows Media                                                                                                                                       |



 

 

 




