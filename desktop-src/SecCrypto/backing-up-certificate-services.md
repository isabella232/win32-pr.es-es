---
description: Cómo puede usar las funciones de copia de seguridad de Servicios de certificados para realizar una copia de seguridad de una base de datos de Servicios de certificados y sus archivos asociados.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Copia de seguridad de servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773091"
---
# <a name="backing-up-certificate-services"></a>Copia de seguridad de servicios de certificados

A continuación se muestra un escenario en el que se muestra cómo puede usar las funciones de copia de seguridad de Servicios de certificados para realizar una copia de seguridad de una base de datos de Servicios de certificados y sus archivos asociados.

1.  Cargue la biblioteca Certadm.dll en la memoria (mediante una llamada [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere la dirección de cada una de las funciones necesarias Certadm.dll (por medio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use estas direcciones al llamar a las funciones en los pasos restantes.
3.  Llame [**a CertSrvIsServerOnline para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) determinar si Servicios de certificados está en línea. Servicios de certificados debe estar en línea para que las operaciones de copia de seguridad se realicen correctamente.
4.  Llame a [**CertSrvBackupPrepare para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) iniciar una sesión de copia de seguridad. Muchas de las demás funciones de copia de seguridad usarán el identificador de contexto de copia de seguridad de Servicios de certificados resultante.
5.  Llame [**a CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) para determinar la asignación de restauración. El mapa de restauración contiene las rutas de acceso que se usarán al restaurar la copia de seguridad. Guarde la información recuperada por **CertSrvRestoreGetDatabaseLocations** en una ubicación específica de la aplicación.
6.  Llame [**a CertSrvBackupGetDatabaseNames para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) determinar los nombres de los archivos de base de datos de los que se va a realizar la copia de seguridad. Para cada uno de estos archivos, ejecute los pasos del 7 al 9.
7.  Llame [**a CertSrvBackupOpenFile para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) abrir el archivo de copia de seguridad.
8.  Llame a [**CertSrvBackupRead para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) leer una parte de bytes del archivo y, a continuación, llame a una rutina específica de la aplicación para almacenar los bytes en un medio de copia de seguridad. Repita este paso hasta que se hace una copia de seguridad de todos los bytes del archivo.
9.  Llame [**a CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) para cerrar el archivo.
10. Llame [**a CertSrvBackupGetBackupLogs para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) determinar los nombres de los archivos de registro de los que se va a realizar una copia de seguridad. Para cada uno de estos archivos, ejecute los pasos del 7 al 9.
11. Llame [**a CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) para truncar los archivos de registro de los que se ha creado una copia de seguridad en los pasos 6 y 10. Este paso es opcional; sin embargo, llame a **CertSrvBackupTruncateLogs** solo si se ha realizado una copia de seguridad de todos los archivos devueltos por [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) y [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) (de lo contrario, se producirá un error en la operación de restauración). Consulte la **página de referencia certSrvBackupTruncateLogs** para obtener más información.
12. Llame [**a CertSrvBackupGetDynamicFileList para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) determinar los nombres de los archivos que no son de base de datos que se va a realizar la copia de seguridad. Estos archivos solo se identifican mediante la función y se debe realizar una copia de seguridad por otros medios.
13. Realice una copia de seguridad de los archivos dinámicos identificados en el paso 12, mediante rutinas independientes de Certadm.dll.
14. Llame [**a CertSrvBackupEnd para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) finalizar la sesión de copia de seguridad.
15. Llame [**a CertSrvBackupFree según**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) sea necesario para liberar búferes asignados por determinadas funciones de copia de seguridad de Servicios de certificados. Las llamadas a [**CertSrvBackupGetBackupLogs,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)y [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) asignarán búferes que se pueden liberar mediante una llamada a **CertSrvBackupFree.**
16. Libere el Certadm.dll recursos mediante una [**llamada a FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Para obtener información sobre los privilegios necesarios para realizar una copia de seguridad de la base de datos de Servicios de certificados y los archivos [asociados,](setting-the-backup-and-restore-privileges.md)vea Establecer los privilegios de copia de seguridad y restauración .

 

 
