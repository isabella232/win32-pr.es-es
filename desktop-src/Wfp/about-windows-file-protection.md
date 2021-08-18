---
description: Windows Resource Protection (WRP) impide la sustitución de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Acerca de Windows Resource Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134207"
---
# <a name="about-windows-resource-protection"></a>Acerca de Windows Resource Protection

Windows Resource Protection (WRP) impide la sustitución de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte del sistema operativo. Empezó a estar disponible a partir de Windows Server 2008 y Windows Vista. El permiso para el acceso completo para modificar recursos protegidos con WRP está restringido a TrustedInstaller. Los recursos protegidos con WRP solo se pueden cambiar mediante los mecanismos de reemplazo de recursos [admitidos](supported-file-replacement-mechanisms.md) con el Windows Instalador de módulos de almacenamiento. La protección de estos recursos evita errores en la aplicación y el sistema operativo.

Las aplicaciones no deben intentar modificar los recursos protegidos por WRP porque los usan Windows y otras aplicaciones. Si una aplicación intenta modificar un recurso protegido por WRP, puede tener los siguientes resultados.

-   Los instaladores de aplicaciones que intentan reemplazar, modificar o eliminar claves críticas de Windows o del Registro pueden no instalar la aplicación y recibirán un mensaje de error que indica que se denegó el acceso al recurso.
-   Las aplicaciones que intentan agregar o quitar subclave o cambiar los valores de las claves protegidas del Registro pueden producir un error y recibirán un mensaje de error que indica que se denegó el acceso al recurso.
-   Las aplicaciones que se basan en escribir información en claves, carpetas o archivos del Registro protegidos pueden producir un error.

WRP es el nuevo nombre de Windows File Protection (WFP). WRP protege las claves y carpetas del Registro, así como los archivos esenciales del sistema. WFP estaba disponible en Microsoft Windows Server 2003 y Windows XP. WRP reemplaza WFP en Windows Server 2008 y Windows Vista.

En los temas siguientes se describe WRP:

-   [Lista de recursos protegidos](protected-file-list.md)
-   [Detección de reemplazo de recursos](detecting-file-replacement.md)
-   [Mecanismos de reemplazo de recursos admitidos](supported-file-replacement-mechanisms.md)
-   [Comprobador de archivos de sistema](system-file-checker.md)
-   [Consideraciones de administración remota](remote-administration-considerations.md)

 

 



