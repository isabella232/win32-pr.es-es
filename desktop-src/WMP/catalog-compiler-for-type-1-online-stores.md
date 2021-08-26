---
title: Compilador de catálogos para almacenes en línea de tipo 1
description: Compilador de catálogos para almacenes en línea de tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Reproductor de Windows Media en línea,compilador de catálogo
- tiendas en línea, compilador de catálogos
- tiendas en línea de tipo 1, compilador de catálogo
- Reproductor de Windows Media en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- tiendas en línea de tipo 1, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864215"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilador de catálogos para almacenes en línea de tipo 1

El compilador de catálogo (catcomp.exe) es una herramienta de línea de comandos que usan las tiendas en línea de tipo 1 para compilar el conjunto de archivos de valores separados por tabulaciones (TSV) que contienen los datos de catálogo del almacén en línea en un catálogo comprimido que puede descargar Reproductor de Windows Media. El compilador de catálogos también compila archivos de actualización de catálogo que contienen solo la información del catálogo que ha cambiado desde la última actualización del catálogo.

Los archivos de catálogo comprimidos o los archivos de actualización del catálogo deben proporcionarse a Reproductor de Windows Media para su descarga en la implementación del complemento de tienda en línea [de IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tareas comunes

-   [Compilar un catálogo completo a partir de archivos TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilar una actualización de catálogo a partir de catálogos completos](compiling-a-catalog-update-from-full-catalogs.md)

Tareas de diagnóstico

-   [Mostrar ayuda](displaying-help.md)
-   [Recuperar información del catálogo](retrieving-catalog-information.md)
-   [Aplicar una actualización a un catálogo](applying-an-update-to-a-catalog.md)

 

 




