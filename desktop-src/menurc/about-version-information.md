---
title: Acerca de la información de versión
description: En este tema se de abordan las funciones de información de versión.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- resources,version information
- información de versión
- agregar información de versión
- conflictos de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7b7916e77d29fa21aa6eb68e223d43a1415c36058fbe00e2d3abb9c4cae979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870721"
---
# <a name="about-version-information"></a>Acerca de la información de versión

Puede usar las funciones de información de versión para determinar dónde debe instalarse un archivo e identificar conflictos con los archivos instalados actualmente. Estas funciones le permiten evitar los siguientes problemas:

-   instalar versiones anteriores de componentes en versiones más recientes
-   cambiar el idioma en un sistema de lenguaje mixto sin notificación
-   instalar varias copias de una biblioteca en directorios diferentes
-   copiar archivos en directorios de red compartidos por varios usuarios

Las funciones de información de versión permiten a las aplicaciones consultar un recurso de versión para obtener información de archivo y presentar la información en un formato claro. Esta información incluye el propósito del archivo, el autor, el número de versión, y así sucesivamente.

Puede agregar información de versión a cualquier archivo que pueda tener Windows recursos, como archivos DLL, archivos ejecutables o archivos de fuente .fon. Para agregar la información, cree un [recurso VERSIONINFO y](/windows/desktop/menurc/versioninfo-resource) use el compilador de recursos para compilar el recurso.

 

 