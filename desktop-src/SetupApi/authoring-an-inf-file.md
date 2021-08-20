---
description: Al crear un archivo INF para una aplicación de instalación, también debe hacer referencia al formato de archivo INF que se documenta en Directrices generales para archivos INF y secciones y directivas de archivo INF del Kit de desarrollo de controladores de Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Creación de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3745dc16a14f603de780b15d708fbb4542ea4503052aeb2b7edb3486c5b5fc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966373"
---
# <a name="authoring-an-inf-file"></a>Creación de un archivo INF

Al crear un archivo INF para una aplicación de instalación, también debe hacer referencia al formato de archivo INF que se documenta en Directrices generales para archivos *INF* y secciones y directivas de archivo *INF* del Kit de desarrollo de controladores de Microsoft Windows 2000.

Al crear archivos INF para una aplicación de instalación, cumpla las reglas siguientes.

-   Se **requiere una** sección Versión en cada archivo INF.
-   Las secciones deben comenzar con el nombre de sección entre corchetes ( \[ \] ).
-   Los nombres **de las secciones DestinationDirs,** **SourceDisksFiles,** **SourceDisksNames,** **Strings** y **Version** deben ser idénticos al tipo de sección. Por ejemplo, use \[ DestinationDirs \] . Los autores pueden especificar los nombres de otros tipos de secciones.
-   Los nombres **de las secciones SourceDisksNames** y **SourceDisksFiles** se pueden anexar con un sufijo específico de la plataforma. Por ejemplo, para mostrar una sección **SourceDisksNames** específica de Intel, use \[ SourceDisksNames.x86 \] . Si las funciones de instalación encuentran secciones **SourceDisksNames y** **SourceDisksFiles** específicas de la plataforma que coinciden con la plataforma del usuario, las funciones usan las secciones específicas de la plataforma. De lo contrario, las funciones de instalación usan las secciones **SourceDisksNames y** **SourceDisksFiles sin** sufijo. Las funciones de instalación pueden determinar mediante programación el sistema del usuario. Vea las [secciones INF SourceDisksNames y SourceDisksFiles Ejemplo](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Los valores se pueden expresar como cadenas reemplazables mediante el formato %*strkey*%. Para usar un carácter % en la cadena, use %%. La strkey debe definirse en una **sección Strings** del archivo INF.

 

 



