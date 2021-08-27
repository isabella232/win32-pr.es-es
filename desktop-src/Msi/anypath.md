---
description: El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045785"
---
# <a name="anypath"></a>AnyPath

El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa. Al especificar una ruta de acceso relativa, puede incluir un nombre de archivo largo con el nombre de archivo corto separando los nombres cortos y largos con una barra vertical ( \| ). Tenga en cuenta que no puede especificar varios niveles de un directorio o rutas de acceso completas de esta manera. La ruta de acceso puede contener propiedades entre corchetes ( \[ \] ).

Ejemplos de datos AnyPath válidos:

-   \\\\server \\ share \\ temp
-   c: \\ temp
-   \\Temp
-   projec~1 \| Project status

Ejemplos de datos AnyPath no válidos:

-   c: \\ temp \\ projec~1 \| c: temp one Project \\ \\ Status
-   \\temp \\ projec~1 \| \\ temp one Project \\ Status

 

 



