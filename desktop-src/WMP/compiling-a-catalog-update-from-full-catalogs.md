---
title: Compilar una actualización del catálogo desde catálogos completos
description: Compilar una actualización del catálogo desde catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player tiendas en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- Escriba 1 tiendas en línea, compilando catálogos
- Windows Media Player tiendas en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tipo 1 almacenes en línea, actualizaciones del catálogo
- Windows Media Player tiendas en línea, catálogos completos
- tiendas en línea, catálogos completos
- tipo 1 tiendas en línea, catálogos completos
- compilar catálogos
- actualizaciones del catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358666"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilar una actualización del catálogo desde catálogos completos

Una actualización de catálogo que contenga los cambios entre dos versiones de un catálogo compilado se puede crear con la siguiente sintaxis, donde *ruta1* es el directorio que contiene el primer catálogo, *ruta2* es el directorio que contiene el segundo catálogo y, opcionalmente, se puede incluir la depuración para mostrar información de error detallada en la pantalla. Los archivos de catálogo deben estar en un formato sin comprimir; el nombre de archivo del catálogo compilado sería Catalog. wmdb, en lugar de Catalog. wmdb. LZ.


```C++
catcomp diff <path1> <path2> [debug]
```



Por ejemplo, si el directorio C: \\ Catalog210 \\ contiene la versión 210 de un catálogo compilado completo y C: \\ Catalog211 contiene la \\ versión 211, el siguiente comando crea un archivo de diferencias que contiene los cambios entre las dos versiones:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Para mostrar información detallada del error, puede Agregar el parámetro de depuración opcional de la siguiente manera:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Si la compilación se realiza correctamente, catcomp.exe crea los archivos de salida que se enumeran a continuación y los guarda en el directorio que contiene el primer catálogo.



| Nombre de archivo             | Descripción                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. diff          | Archivo de diferencias compiladas sin comprimir.                                                                                                                                                           |
| Catalog. diff. LZ       | Versión comprimida del archivo de actualización de catálogo. El complemento puede proporcionar la ubicación de este archivo a Windows Media Player en [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| Catalog. wmdb. Delta    | Archivo de salida intermedio. No lo utiliza Windows Media Player                                                                                                                                       |
| Catalog. wmdb. Modified | Archivo de salida intermedio. No lo utiliza Windows Media Player                                                                                                                                       |



 

 

 




