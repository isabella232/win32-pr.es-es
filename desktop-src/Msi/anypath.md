---
description: El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652618"
---
# <a name="anypath"></a>AnyPath

El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa. Al especificar una ruta de acceso relativa, puede incluir un nombre de archivo largo con el nombre de archivo corto separando los nombres corto y largo con una barra vertical ( \| ). Tenga en cuenta que no puede especificar varios niveles de un directorio o rutas de acceso completas de esta manera. La ruta de acceso puede contener propiedades entre corchetes ( \[ \] ).

Ejemplos de datos de AnyPath válidos:

-   \\\\\\recurso compartido de servidor \\ temporal
-   c: \\ Temp
-   \\temperatura
-   Project ~ 1 \| Estado del proyecto

Ejemplos de datos de AnyPath no válidos:

-   c: \\ temp \\ Project ~ 1 \| c: \\ temp un \\ Estado de proyecto
-   \\Temp \\ Project ~ 1 \| \\ temp un \\ Estado de proyecto

 

 



