---
title: Enlazar al punto inicial de búsqueda
description: El punto de inicio de una búsqueda es un contenedor que contiene directa o indirectamente los objetos buscados.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, enlazar a un punto de inicio de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486546"
---
# <a name="binding-to-the-search-start-point"></a>Enlazar al punto inicial de búsqueda

El punto de inicio de una búsqueda es un contenedor que contiene directa o indirectamente los objetos buscados. La búsqueda no se realizará en contenedores por encima del punto de inicio de la búsqueda. Por ejemplo, tome la siguiente estructura de directorios hipotética:

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Si se realiza una búsqueda para todos los objetos y el punto de inicio de la búsqueda es "contenedor 2", solo se recuperarán "Object 3" y "Object 4". Si se realizó la misma búsqueda con el punto de inicio de búsqueda en "contenedor 1", se recuperaría el "objeto 1" y el "objeto 2".

Para enlazar con el punto inicial de búsqueda, enlace al ADsPath del contenedor que será el punto de inicio de la búsqueda.

 

 




