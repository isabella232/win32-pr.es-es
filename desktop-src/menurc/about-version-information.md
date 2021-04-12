---
title: Información sobre la versión
description: En este tema se describen las funciones de información de versión.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- recursos, información de versión
- información de versión
- agregar información de versión
- conflictos de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420609"
---
# <a name="about-version-information"></a>Información sobre la versión

Puede utilizar las funciones de información de versión para determinar dónde debe instalarse un archivo e identificar conflictos con los archivos instalados actualmente. Estas funciones permiten evitar los problemas siguientes:

-   instalar versiones anteriores de componentes en versiones más recientes
-   cambiar el idioma en un sistema de lenguaje mixto sin notificación
-   instalación de varias copias de una biblioteca en directorios diferentes
-   copiar archivos en directorios de red compartidos por varios usuarios

Las funciones de información de versión permiten a las aplicaciones consultar un recurso de versión en busca de información de archivos y presentar la información en un formato sin cifrar. Esta información incluye el propósito del archivo, el autor, el número de versión, etc.

Puede agregar información de versión a cualquier archivo que pueda tener recursos de Windows, como archivos dll, archivos ejecutables o archivos de fuentes. fon. Para agregar la información, cree un [recurso versionInfo](/windows/desktop/menurc/versioninfo-resource) y use el compilador de recursos para compilar el recurso.

 

 