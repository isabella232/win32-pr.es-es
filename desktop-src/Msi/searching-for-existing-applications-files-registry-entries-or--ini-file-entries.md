---
description: Windows El instalador puede buscar un archivo o directorio específico durante una instalación. Las búsquedas de archivos o directorios se usan para determinar si un usuario ya ha instalado una versión de una aplicación.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Buscar aplicaciones, archivos, entradas del Registro o entradas de .ini existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9cf4b39f8a46ccd16e83c96ee6ca808b3a1bee32094da480d0226d8bdf283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041055"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Buscar aplicaciones, archivos, entradas del Registro o entradas de .ini existentes

Windows El instalador puede buscar un archivo o directorio específico durante una instalación. Las búsquedas de archivos o directorios se usan para determinar si un usuario ya ha instalado una versión de una aplicación.

[Acción de AppSearch](appsearch-action.md) busca en un sistema de usuario firmas de archivo que se especifican en la [tabla de AppSearch](appsearch-table.md). Si la acción AppSearch encuentra un archivo o directorio instalado con la firma especificada, establece una propiedad correspondiente, también especificada en la tabla AppSearch, en la ubicación del archivo o directorio. Al buscar un archivo, la firma de archivo también debe aparecer en la tabla [de firma](signature-table.md). Si una firma de archivo aparece en la tabla AppSearch y no aparece en la tabla de firmas, la búsqueda busca un directorio, una entrada del Registro o una .ini archivo.

Para acelerar la búsqueda de un equipo de usuario, el instalador consulta las siguientes tablas de base de datos de localizador en el orden indicado para una ubicación de búsqueda sugerida:

-   Si la firma de archivo aparece en la tabla [CompLocator](complocator-table.md), la ubicación de búsqueda sugerida es la ruta de acceso clave de un componente. Si la firma no aparece en esta tabla o no está instalada en la ubicación sugerida, el instalador consulta la tabla [RegLocator](reglocator-table.md) para obtener una ubicación sugerida.
-   Si la firma de archivo aparece en la [tabla RegLocator](reglocator-table.md), la ubicación de búsqueda sugerida es una ruta de acceso de clave escrita en el registro de usuario. Si la firma no aparece en esta tabla o no está instalada en la ubicación sugerida, el instalador consulta la tabla [IniLocator](inilocator-table.md) para obtener una ubicación sugerida.
-   Si la firma de archivo aparece en la tabla [IniLocator](inilocator-table.md), la ubicación de búsqueda sugerida es una ruta de acceso clave escrita en un archivo .ini presente en el directorio Windows predeterminado de un sistema de usuario. Si la firma no aparece en esta tabla o no está instalada en la ubicación sugerida, el instalador consulta la [tabla DrLocator](drlocator-table.md) para obtener una ubicación sugerida.
-   Si la firma de archivo aparece en la [tabla DrLocator](drlocator-table.md), la ubicación de búsqueda sugerida es una ruta de acceso en el árbol de directorios de usuario. La profundidad de los niveles de subdirectorio para buscar debajo de esta ubicación también se especifica en esta tabla.

La primera vez que el instalador encuentra la firma de archivo en una ubicación sugerida, deja de buscar este archivo o directorio y establece la propiedad correspondiente en la [tabla de AppSearch](appsearch-table.md). Para obtener más información, vea lo siguiente:

-   [Buscar un archivo en todas las unidades fijas](searching-all-fixed-drives-for-a-file.md)
-   [Buscar un directorio y un archivo en el directorio](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Buscar un archivo y crear una propiedad que mantiene la ruta de acceso del archivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Buscar un archivo en una ubicación específica](searching-for-a-file-in-a-specific-location.md)
-   [Buscar una entrada del Registro y crear una propiedad que mantiene el valor del Registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



