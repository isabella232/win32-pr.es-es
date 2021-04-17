---
description: El reemplazo de recursos protegidos se admite a través de los siguientes mecanismos.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de sustitución de recursos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706990"
---
# <a name="supported-resource-replacement-mechanisms"></a>Mecanismos de sustitución de recursos admitidos

El reemplazo de recursos protegidos se admite a través de los siguientes mecanismos.

El permiso para el acceso completo para modificar los recursos protegidos por WRP en Windows Vista y Windows Server 2008 está restringido a TrustedInstaller con el servicio de instalador de módulos de Windows mediante los siguientes mecanismos:

-   Los Service Pack de Windows instalados por TrustedInstaller.
-   Revisiones instaladas por TrustedInstaller.
-   Actualizaciones del sistema operativo instaladas por TrustedInstaller.
-   Windows Update instala por TrustedInstaller.

Las aplicaciones y los instaladores que intentan reemplazar un recurso protegido por WRP por medio de otros métodos especificados tienen denegado el acceso para cambiar el recurso y generar un mensaje de error de acceso denegado.

En el caso de los instaladores conocidos que intentan reemplazar recursos protegidos por WRP, se puede suprimir el error de acceso denegado y el mensaje de error. En este caso, la operación se devuelve correctamente, se suprime el error y el mensaje de error, pero no se aplica ningún cambio al recurso protegido por WRP. El error se puede suprimir para un instalador conocido solo cuando se cumplen todos los criterios siguientes:

-   Se trata de una aplicación heredada. La aplicación no incluye un manifiesto con un requestedExecutionlevel que identifique la aplicación tal y como se diseñó para Windows Vista o Windows Server 2008.
-   El error de acceso denegado se debe a que solo se intenta modificar un recurso protegido por WRP.
-   Un administrador está instalando la aplicación.

Para obtener información acerca del uso del Windows Installer con WRP, consulte [uso de Windows Installer y protección de recursos de Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) en el SDK de [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .

**Windows Server 2003 y Windows XP:** El reemplazo de archivos del sistema protegidos por WFP solo se admite a través de los siguientes mecanismos:

-   Instalación de Windows Service Pack mediante Update.exe
-   Revisiones instaladas mediante Hotfix.exe
-   Actualizaciones del sistema operativo con Winnt32.exe
-   Windows Update

Reemplazar archivos protegidos por medio de otros métodos especificados hace que WFP restaure los archivos originales.

 

 
