---
description: Si \_ se especifica la marca de copia de SP \_ más reciente durante una operación de copia de archivos, las funciones de instalación comprueban si hay una copia existente del archivo en el directorio de destino.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Comparaciones de versión de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668181"
---
# <a name="file-version-comparisons"></a>Comparaciones de versión de archivo

Si \_ se especifica la marca de copia de SP \_ más reciente durante una operación de copia de archivos, las funciones de instalación comprueban si hay una copia existente del archivo en el directorio de destino. Si se encuentra una copia existente, las funciones comparan las versiones del archivo de origen y de destino para determinar cuál es la más reciente.

La información de versión de archivo que se usa durante las comprobaciones de versión es que se especifica en los miembros **dwFileVersionMS** y **dwFileVersionLS** de una estructura de [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) , usada por las funciones de versión. Si uno de los archivos no tiene los recursos de versión especificados o si tienen la misma información de versión, el archivo de código fuente se trata como el archivo más reciente.

 

 
