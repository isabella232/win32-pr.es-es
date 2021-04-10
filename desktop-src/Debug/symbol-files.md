---
description: Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Archivos de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152847"
---
# <a name="symbol-files"></a>Archivos de símbolos

Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable. La implementación de esta información de depuración ha cambiado a lo largo de los años y en la siguiente documentación se proporcionan instrucciones sobre estas distintas implementaciones.

## <a name="pdb-files"></a>PDB (archivos)

Todas las versiones modernas de los compiladores de Microsoft almacenan información de depuración sobre un ejecutable compilado en un archivo de *base de datos de programa* (. pdb) independiente. Este archivo se conoce comúnmente como *PDB*. Los datos se almacenan en un archivo independiente del ejecutable para limitar el tamaño del archivo ejecutable, lo que ahorra espacio de almacenamiento en disco y reduce el tiempo necesario para cargar los datos. Esta metodología también permite que el ejecutable se distribuya sin revelar esta información importante, lo que podría facilitar el uso del programa de ingeniería inversa.

Para crear un PDB, compile el archivo ejecutable con la información de depuración de acuerdo con las instrucciones de las herramientas de compilación.

La API de DbgHelp puede usar archivos PDB para obtener la información siguiente.

-   públicos y exportaciones
-   símbolos globales
-   símbolos locales
-   datos de tipo
-   archivos de código fuente
-   números de línea

## <a name="dbg-files-and-embedded-debug-information"></a>Archivos DBG e información de depuración incrustada

Las versiones anteriores del conjunto de herramientas de Microsoft usaban para incrustar la información de depuración en el archivo ejecutable, pero normalmente se eliminarían en un archivo independiente con la extensión. dbg. Esto se conoce comúnmente como archivo *dbg* . Los archivos DBG usan el mismo formato de archivo PE que los ejecutables.

La compatibilidad con la API de DbgHelp para DBGs y la información de depuración incrustada es limitada e incluye lo siguiente.

-   públicos y exportaciones
-   símbolos globales

 

 



