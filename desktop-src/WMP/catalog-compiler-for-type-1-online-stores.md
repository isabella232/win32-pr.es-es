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
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="52c64-111">Compilador de catálogo para las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="52c64-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="52c64-112">El compilador de catálogo (catcomp.exe) es una herramienta de línea de comandos que utilizan las tiendas en línea de tipo 1 para compilar el conjunto de archivos de valores separados por tabulaciones (TSV) que contienen los datos del catálogo de la tienda en línea en un catálogo comprimido que puede descargar Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="52c64-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="52c64-113">El compilador del catálogo también compila los archivos de actualización de catálogo que contienen solo la información del catálogo que ha cambiado desde la última actualización del catálogo.</span><span class="sxs-lookup"><span data-stu-id="52c64-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="52c64-114">Los archivos de catálogo comprimidos o los archivos de actualización de catálogo deben proporcionarse a Windows Media Player para su descarga en la implementación del complemento de la tienda en línea de [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="52c64-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="52c64-115">Tareas comunes</span><span class="sxs-lookup"><span data-stu-id="52c64-115">Common Tasks</span></span>

-   [<span data-ttu-id="52c64-116">Compilación de un catálogo completo a partir de archivos TSV</span><span class="sxs-lookup"><span data-stu-id="52c64-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="52c64-117">Compilar una actualización del catálogo desde catálogos completos</span><span class="sxs-lookup"><span data-stu-id="52c64-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="52c64-118">Tareas de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="52c64-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="52c64-119">Mostrar la ayuda</span><span class="sxs-lookup"><span data-stu-id="52c64-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="52c64-120">Recuperación de información del catálogo</span><span class="sxs-lookup"><span data-stu-id="52c64-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="52c64-121">Aplicar una actualización a un catálogo</span><span class="sxs-lookup"><span data-stu-id="52c64-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 




