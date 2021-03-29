---
title: Copia de seguridad y restauración de un servidor Active Directory
description: Active Directory Domain Services proporcionan funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, uso, copia de seguridad y restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789639"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Copia de seguridad y restauración de un servidor Active Directory

Active Directory Domain Services proporcionan funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio. En esta sección se describe cómo [realizar una copia de seguridad](backing-up-an-active-directory-server.md) y [restaurar](restoring-an-active-directory-server.md) un servidor de Active Directory. Para obtener más información acerca de la copia de seguridad de un servidor de Active Directory con las utilidades proporcionadas en los sistemas operativos Windows 2000 y Windows Server 2003, consulte el kit de recursos aplicable, disponible en el sitio web de Microsoft TechNet.

La copia de seguridad de un servidor de Active Directory debe realizarse en línea y debe realizarse cuando se instale el Active Directory Domain Services. Active Directory Domain Services se basan en una base de datos Especial y exportan un conjunto de funciones de copia de seguridad que proporcionan la interfaz de copia de seguridad mediante programación. La copia de seguridad no admite copias de seguridad incrementales. Una aplicación de copia de seguridad se enlaza a un archivo DLL del lado cliente local con puntos de entrada definidos en Ntdsbcli. h.

La restauración de un servidor de Active Directory siempre se realiza sin conexión.

Aunque en los temas de esta sección solo se describe cómo realizar copias de seguridad y restaurar un servidor de Active Directory, tenga en cuenta que los sistemas operativos Windows 2000 y Windows Server 2003 tienen varios componentes de "estado del sistema" que se deben copiar y restaurar juntos. Estos componentes de estado del sistema constan de:

-   Archivos de arranque como NTLDR, Ntdetect, todos los archivos protegidos por SFP y configuración del contador de rendimiento
-   El controlador de Dominio de Active Directory
-   SysVol (solo controlador de dominio)
-   Servidor de certificados (solo CA)
-   Base de datos de clúster (solo nodo de clúster)
-   Registro
-   Base de datos de registro de clase COM+

Se puede realizar una copia de seguridad del estado del sistema en cualquier orden, pero la restauración del estado del sistema debe realizarse en el orden siguiente:

1.  Restaure los archivos de arranque.
2.  Restaure SysVol, servidor de certificados, base de datos de clúster y base de datos de registro de clase COM+, según corresponda.
3.  Restaure el servidor de Active Directory.
4.  Restaure el registro.

Para obtener más información sobre la copia de seguridad y restauración de servicios de Certificate Server, vea [usar las funciones de copia de seguridad y restauración de servicios de certificados](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Para obtener más información acerca de la copia de seguridad y la restauración de Active Directory Domain Services, consulte:

-   [Consideraciones sobre la copia de seguridad de Active Directory Domain Services](considerations-for-active-directory-domain-services-backup.md)
-   [Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
-   [Restauración de un servidor de Active Directory](restoring-an-active-directory-server.md)
-   [Funciones de copia de seguridad de directorios](directory-backup-functions.md)

 

 