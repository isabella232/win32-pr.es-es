---
description: Al crear un archivo INF para una aplicación de instalación, también debe consultar el formato de archivo INF que se documenta en las secciones instrucciones generales para archivos INF y las secciones y directivas de archivos INF del kit de desarrollo de controladores de Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Creación de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666430"
---
# <a name="authoring-an-inf-file"></a>Creación de un archivo INF

Al crear un archivo INF para una aplicación de instalación, también debe consultar el formato de archivo INF que se documenta en las secciones *instrucciones generales para archivos INF* y las *secciones y directivas de archivos* inf del kit de desarrollo de controladores de Microsoft Windows 2000.

Al crear archivos INF para una aplicación de instalación, debe cumplir las siguientes reglas.

-   Se requiere una sección de **versión** en cada archivo INF.
-   Las secciones deben comenzar con el nombre de sección entre corchetes ( \[ \] ).
-   Los nombres de las secciones **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** y **version** deben ser idénticos al tipo de sección. Por ejemplo, use \[ DestinationDirs \] . Los autores pueden especificar los nombres de otros tipos de secciones.
-   Los nombres de las secciones **SourceDisksNames** y **SourceDisksFiles** se pueden anexar con un sufijo específico de la plataforma. Por ejemplo, para mostrar una sección **SourceDisksNames** específica de Intel, use \[ SourceDisksNames. x86 \] . Si las funciones de instalación buscan secciones **SourceDisksNames** y **SourceDisksFiles** específicas de la plataforma que coincidan con la plataforma del usuario, las funciones usan las secciones específicas de la plataforma. De lo contrario, las funciones de instalación usan las secciones **SourceDisksNames** y **SourceDisksFiles** sin sufijo. Las funciones de configuración pueden determinar mediante programación el sistema del usuario. Vea el [ejemplo de secciones SourceDisksNames y SourceDisksFiles de INF](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Los valores se pueden expresar como cadenas reemplazables con la forma%*strkey*%. Para usar un carácter% en la cadena, use%%. Strkey debe definirse en una sección **Strings** del archivo INF.

 

 



