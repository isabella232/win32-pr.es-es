---
description: El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159134"
---
# <a name="anypath"></a>AnyPath

El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa. Al especificar una ruta de acceso relativa, puede incluir un nombre de archivo largo con el nombre de archivo corto separando los nombres cortos y largos con una barra vertical ( \| ). Tenga en cuenta que no puede especificar varios niveles de un directorio o rutas de acceso completas de esta manera. La ruta de acceso puede contener propiedades entre corchetes ( \[ \] ).

Ejemplos de datos AnyPath válidos:

-   \\\\server \\ share \\ temp
-   c: \\ temp
-   \\Temp
-   projec~1 \| Project estado

Ejemplos de datos AnyPath no válidos:

-   c: \\ temp \\ projec~1 \| c: temp one Project \\ \\ Status
-   \\temp \\ projec~1 \| \\ temp one Project \\ Status

 

 



