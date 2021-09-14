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
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268556"
---
# <a name="about-version-information"></a>Acerca de la información de versión

Puede usar las funciones de información de versión para determinar dónde se debe instalar un archivo e identificar conflictos con los archivos instalados actualmente. Estas funciones le permiten evitar los siguientes problemas:

-   instalar versiones anteriores de componentes en versiones más recientes
-   cambiar el idioma en un sistema de lenguaje mixto sin notificación
-   instalar varias copias de una biblioteca en directorios diferentes
-   copiar archivos en directorios de red compartidos por varios usuarios

Las funciones de información de versión permiten a las aplicaciones consultar un recurso de versión para obtener información de archivo y presentar la información en un formato claro. Esta información incluye el propósito del archivo, el autor, el número de versión, y así sucesivamente.

Puede agregar información de versión a cualquier archivo que pueda tener Windows recursos, como archivos DLL, archivos ejecutables o archivos de fuente .fon. Para agregar la información, cree un [recurso VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) y use el compilador de recursos para compilar el recurso.

 

 