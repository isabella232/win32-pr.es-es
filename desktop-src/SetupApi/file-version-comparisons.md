---
description: Si se especifica la marca SP COPY NEWER durante una operación de copia de archivos, las funciones de instalación comprueban si hay una copia existente del archivo \_ en el directorio de \_ destino.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Comparaciones de versiones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a017549899aa43340f744b1176e7d14ce17d44d60c52b18cfbed9eae3474e99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683185"
---
# <a name="file-version-comparisons"></a>Comparaciones de versiones de archivo

Si se especifica la marca SP COPY NEWER durante una operación de copia de archivos, las funciones de instalación comprueban si hay una copia existente del archivo \_ en el directorio de \_ destino. Si se encuentra una copia existente, las funciones comparan las versiones del archivo de origen y de destino para determinar cuál es más reciente.

La información de versión del archivo utilizada durante las comprobaciones de versión es la especificada en los miembros **dwFileVersionMS** y **dwFileVersionLS** de una estructura [**\_ FIXEDFILEINFO de VS,**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) utilizada por las funciones de versión. Si uno de los archivos no tiene especificados recursos de versión o si tienen la misma información de versión, el archivo de origen se trata como el archivo más reciente.

 

 
