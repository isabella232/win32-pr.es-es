---
title: Compilador de catálogo para almacenes en línea de tipo 1
description: Compilador de catálogo para almacenes en línea de tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Reproductor de Windows Media en línea, compilador de catálogos
- online stores,catalog compiler
- tiendas en línea de tipo 1, compilador de catálogo
- Reproductor de Windows Media en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- tiendas en línea de tipo 1, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253280"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilador de catálogo para almacenes en línea de tipo 1

El compilador de catálogos (catcomp.exe) es una herramienta de línea de comandos que usan los almacenes en línea de tipo 1 para compilar el conjunto de archivos de valores separados por tabulaciones (TSV) que contienen los datos de catálogo del almacén en línea en un catálogo comprimido que puede descargar Reproductor de Windows Media. El compilador de catálogos también compila los archivos de actualización de catálogo que contienen solo la información del catálogo que ha cambiado desde la última actualización del catálogo.

Los archivos de catálogo comprimidos o los archivos de actualización del catálogo deben proporcionarse a Reproductor de Windows Media para su descarga en la implementación del complemento de la tienda en línea de [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tareas comunes

-   [Compilación de un catálogo completo a partir de archivos TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilación de una actualización de catálogo a partir de catálogos completos](compiling-a-catalog-update-from-full-catalogs.md)

Tareas de diagnóstico

-   [Mostrar ayuda](displaying-help.md)
-   [Recuperar información del catálogo](retrieving-catalog-information.md)
-   [Aplicar una actualización a un catálogo](applying-an-update-to-a-catalog.md)

 

 




