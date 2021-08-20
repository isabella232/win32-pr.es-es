---
title: Copia de seguridad y restauración de un servidor Active Directory servidor
description: Active Directory Domain Services funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, mediante, realizar copias de seguridad y restaurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1955c70daed8cfaed0f5afe6c498a599aebb30f5d7b1846442d22cf84e9634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024162"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Copia de seguridad y restauración de un servidor Active Directory servidor

Active Directory Domain Services funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio. En esta sección se describe cómo hacer [una copia de seguridad](backing-up-an-active-directory-server.md) y restaurar [un](restoring-an-active-directory-server.md) Active Directory servidor. Para obtener más información sobre cómo hacer una copia de seguridad de un servidor de Active Directory mediante las utilidades proporcionadas en los sistemas operativos Windows 2000 y Windows Server 2003, consulte el Kit de recursos aplicable, disponible en el sitio web de Microsoft TechNet.

La copia de seguridad Active Directory servidor debe realizarse en línea y debe realizarse cuando se Active Directory Domain Services el servidor. Active Directory Domain Services se basa en una base de datos especial y exporta un conjunto de funciones de copia de seguridad que proporcionan la interfaz de copia de seguridad mediante programación. La copia de seguridad no admite copias de seguridad incrementales. Una aplicación de copia de seguridad se enlaza a un archivo DLL del lado cliente local con puntos de entrada definidos en Ntdsbcli.h.

La restauración de Active Directory servidor siempre se realiza sin conexión.

Aunque los temas de esta sección describen solo cómo realizar copias de seguridad y restaurar un servidor Active Directory, tenga en cuenta que Windows 2000 y los sistemas operativos Windows Server 2003 tienen varios componentes de "estado del sistema" de los que se deben realizar copias de seguridad y restaurarse juntos. Estos componentes de estado del sistema constan de:

-   Archivos de arranque como ntldr, ntdetect, todos los archivos protegidos por SFP y la configuración del contador de rendimiento
-   Controlador de Dominio de Active Directory de datos
-   SysVol (solo controlador de dominio)
-   Servidor de certificados (solo CA)
-   Base de datos de clúster (solo nodo de clúster)
-   Registro
-   Base de datos de registro de clases COM+

Se puede realizar una copia de seguridad del estado del sistema en cualquier orden, pero la restauración del estado del sistema debe realizarse en el orden siguiente:

1.  Restaure los archivos de arranque.
2.  Restaure SysVol, Servidor de certificados, Base de datos de clúster y Base de datos de registro de clases COM+, según corresponda.
3.  Restaure el Active Directory servidor.
4.  Restaure el registro.

Para obtener más información sobre la copia de seguridad y restauración de Servicios de certificados, vea Usar las funciones de copia de [seguridad y restauración de Servicios de certificados](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Para obtener más información sobre la copia de seguridad y la restauración Active Directory Domain Services, vea:

-   [Consideraciones para la copia Active Directory Domain Services copia de seguridad](considerations-for-active-directory-domain-services-backup.md)
-   [Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
-   [Restaurar un servidor Active Directory servidor](restoring-an-active-directory-server.md)
-   [Funciones de copia de seguridad de directorios](directory-backup-functions.md)

 

 