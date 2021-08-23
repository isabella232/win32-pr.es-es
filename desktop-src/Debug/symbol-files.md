---
description: Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Archivos de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642185"
---
# <a name="symbol-files"></a>Archivos de símbolos

Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable. La implementación de esta información de depuración ha cambiado a lo largo de los años y la siguiente documentación proporcionará instrucciones sobre estas diversas implementaciones.

## <a name="pdb-files"></a>PDB (archivos)

Todas las versiones modernas de los compiladores de Microsoft almacenan información de depuración sobre un ejecutable compilado en un archivo de base de datos de *programa* independiente (.pdb). Este archivo se conoce normalmente como *PDB.* Los datos se almacenan en un archivo independiente del ejecutable para ayudar a limitar el tamaño del ejecutable, lo que ahorra espacio de almacenamiento en disco y reduce el tiempo necesario para cargar los datos. Esta metodología también permite distribuir el archivo ejecutable sin revelar esta información significativa, lo que podría facilitar la ingeniería inversa del programa.

Para crear una PDB, compile el archivo ejecutable con información de depuración según las instrucciones de las herramientas de compilación.

DbgHelp API puede usar archivos PDU para obtener la siguiente información.

-   publics y exports
-   símbolos globales
-   símbolos locales
-   datos de tipo
-   archivos de código fuente
-   números de línea

## <a name="dbg-files-and-embedded-debug-information"></a>Archivos DBG e información de depuración insertadas

Las versiones anteriores del conjunto de herramientas de Microsoft se usaban para insertar la información de depuración en el ejecutable, pero normalmente se quitaban en un archivo independiente con una extensión .dbg. Esto se conoce normalmente como un *archivo DBG.* Los archivos DBG usan el mismo formato de archivo PE que los ejecutables.

La compatibilidad de la API de DbgHelp con los DBG y la información de depuración incrustada es limitada e incluye lo siguiente.

-   publics y exports
-   símbolos globales

 

 



