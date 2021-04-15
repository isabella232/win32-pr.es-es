---
title: Compilador de catálogo para las tiendas en línea de tipo 1
description: Compilador de catálogo para las tiendas en línea de tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player tiendas en línea, compilador de catálogos
- tiendas en línea, compilador de catálogos
- tipo 1 almacenes en línea, compilador de catálogos
- Windows Media Player tiendas en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- Escriba 1 tiendas en línea, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695524"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilador de catálogo para las tiendas en línea de tipo 1

El compilador de catálogo (catcomp.exe) es una herramienta de línea de comandos que utilizan las tiendas en línea de tipo 1 para compilar el conjunto de archivos de valores separados por tabulaciones (TSV) que contienen los datos del catálogo de la tienda en línea en un catálogo comprimido que puede descargar Windows Media Player. El compilador del catálogo también compila los archivos de actualización de catálogo que contienen solo la información del catálogo que ha cambiado desde la última actualización del catálogo.

Los archivos de catálogo comprimidos o los archivos de actualización de catálogo deben proporcionarse a Windows Media Player para su descarga en la implementación del complemento de la tienda en línea de [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tareas comunes

-   [Compilación de un catálogo completo a partir de archivos TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilar una actualización del catálogo desde catálogos completos](compiling-a-catalog-update-from-full-catalogs.md)

Tareas de diagnóstico

-   [Mostrar la ayuda](displaying-help.md)
-   [Recuperación de información del catálogo](retrieving-catalog-information.md)
-   [Aplicar una actualización a un catálogo](applying-an-update-to-a-catalog.md)

 

 




