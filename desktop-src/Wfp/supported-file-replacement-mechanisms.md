---
description: La sustitución de recursos protegidos se admite mediante los mecanismos siguientes.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de reemplazo de recursos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359856"
---
# <a name="supported-resource-replacement-mechanisms"></a>Mecanismos de reemplazo de recursos admitidos

La sustitución de recursos protegidos se admite mediante los mecanismos siguientes.

El permiso de acceso completo para modificar recursos protegidos con WRP en Windows Vista y Windows Server 2008 está restringido a TrustedInstaller con el servicio instalador de módulos de Windows mediante los mecanismos siguientes:

-   Windows Service Packs instalados por TrustedInstaller.
-   Revisiones instaladas por TrustedInstaller.
-   Actualizaciones del sistema operativo instaladas por TrustedInstaller.
-   Windows Actualización instalada por TrustedInstaller.

A las aplicaciones e instaladores que intentan reemplazar un recurso protegido por WRP por medios distintos de estos métodos especificados se les deniega el acceso para cambiar el recurso y generar un mensaje de error de acceso denegado.

En el caso de instaladores conocidos que intentan reemplazar recursos protegidos por WRP, se puede suprimir el mensaje de error y el error de acceso denegado. En este caso, la operación se devuelve correctamente, se suprimen el mensaje de error y el error, pero no se aplica ningún cambio al recurso protegido por WRP. El error se puede suprimir para un instalador conocido solo cuando se cumplen todos los criterios siguientes:

-   Se trata de una aplicación heredada. La aplicación no incluye un manifiesto con un requestedExecutionlevel que identifique la aplicación como diseñada para Windows Vista o Windows Server 2008.
-   El error de acceso denegado solo se debe al intento de modificar un recurso protegido por WRP.
-   Un administrador está instalando la aplicación.

Para obtener información sobre cómo usar Windows Installer con WRP, consulte Uso de Windows Installer y [Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) en el SDK Windows [Installer.](/windows/desktop/Msi/windows-installer-portal)

**Windows Server 2003 y Windows XP:** La sustitución de archivos del sistema protegidos por WFP solo se admite mediante los mecanismos siguientes:

-   Windows Instalación de Service Pack mediante Update.exe
-   Revisiones instaladas mediante Hotfix.exe
-   Actualizaciones del sistema operativo mediante Winnt32.exe
-   Windows Update

La sustitución de archivos protegidos por medios distintos de estos métodos especificados da lugar a que WFP restaure los archivos originales.

 

 
