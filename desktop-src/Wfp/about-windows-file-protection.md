---
description: Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Acerca de Protección de recursos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706992"
---
# <a name="about-windows-resource-protection"></a>Acerca de Protección de recursos de Windows

Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo. Estuvo disponible a partir de Windows Server 2008 y Windows Vista. El permiso para el acceso completo para modificar los recursos protegidos por WRP está restringido a TrustedInstaller. Los recursos protegidos por WRP solo pueden cambiarse mediante los [mecanismos de sustitución de recursos admitidos](supported-file-replacement-mechanisms.md) con el servicio de instalador de módulos de Windows. La protección de estos recursos evita errores en la aplicación y en el sistema operativo.

Las aplicaciones no deben intentar modificar los recursos protegidos por WRP porque Windows y otras aplicaciones las utilizan. Si una aplicación intenta modificar un recurso protegido por WRP, puede tener los siguientes resultados.

-   Es posible que los instaladores de aplicaciones que intenten reemplazar, modificar o eliminar claves de registro o archivos críticos de Windows no puedan instalar la aplicación y reciban un mensaje de error que indica que se denegó el acceso al recurso.
-   Las aplicaciones que intentan agregar o quitar las subclaves o cambiar los valores de las claves del registro protegidas pueden producir un error y recibirán un mensaje de error que indica que se denegó el acceso al recurso.
-   Se puede producir un error en las aplicaciones que se basan en la escritura de información en claves, carpetas o archivos protegidos del registro.

WRP es el nuevo nombre de protección de archivos de Windows (WFP). WRP protege las claves del registro y las carpetas, así como los archivos esenciales del sistema. WFP estaba disponible en Microsoft Windows Server 2003 y Windows XP. WRP reemplaza WFP en Windows Server 2008 y Windows Vista.

En los temas siguientes se describe WRP:

-   [Lista de recursos protegidos](protected-file-list.md)
-   [Detección de reemplazo de recursos](detecting-file-replacement.md)
-   [Mecanismos de sustitución de recursos admitidos](supported-file-replacement-mechanisms.md)
-   [Comprobador de archivos de sistema](system-file-checker.md)
-   [Consideraciones de administración remota](remote-administration-considerations.md)

 

 



