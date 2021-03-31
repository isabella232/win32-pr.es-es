---
description: Cómo puede usar las funciones de copia de seguridad de servicios de servidor de certificados para realizar una copia de seguridad de una base de datos de servicios de certificados y sus archivos asociados.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Copia de seguridad de servicios de Certificate Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1be929fcf3bd9b8b9655b48758a97d19af7abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913425"
---
# <a name="backing-up-certificate-services"></a>Copia de seguridad de servicios de Certificate Server

A continuación se muestra un escenario en el que se muestra cómo se pueden usar las funciones de copia de seguridad de servicios de servidor de certificados para realizar una copia de seguridad de una base de datos de servicios de certificados y

1.  Cargue la biblioteca de Certadm.dll en la memoria (llamando a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere la dirección de cada una de las funciones necesarias en Certadm.dll (mediante [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use estas direcciones al llamar a las funciones en los pasos restantes.
3.  Llame a [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) para determinar si los servicios de Certificate Server están en línea. Los servicios de Certificate Server deben estar en línea para que las operaciones de copia de seguridad se realicen correctamente.
4.  Llame a [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) para iniciar una sesión de copia de seguridad. Muchas de las otras funciones de copia de seguridad utilizarán el identificador de contexto de copia de seguridad de servicios de certificados resultante.
5.  Llame a [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) para determinar la asignación de restauración. La asignación de restauración contiene las rutas de acceso que se van a usar al restaurar la copia de seguridad. Guarde la información recuperada por **CertSrvRestoreGetDatabaseLocations** en una ubicación específica de la aplicación.
6.  Llame a [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) para determinar los nombres de los archivos de base de datos que se van a copiar. Para cada uno de estos archivos, ejecute los pasos del 7 al 9.
7.  Llame a [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) para abrir el archivo de copia de seguridad.
8.  Llame a [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) para leer una parte de los bytes del archivo y, a continuación, llame a una rutina específica de la aplicación para almacenar los bytes en un medio de copia de seguridad. Repita este paso hasta que se realice una copia de seguridad de todos los bytes del archivo.
9.  Llame a [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) para cerrar el archivo.
10. Llame a [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) para determinar los nombres de los archivos de registro en los que se va a realizar la copia de seguridad. Para cada uno de estos archivos, ejecute los pasos del 7 al 9.
11. Llame a [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) para truncar los archivos de registro de los que se realizó una copia de seguridad en los pasos 6 y 10. Este paso es opcional; sin embargo, llame a **CertSrvBackupTruncateLogs** solo si se ha realizado una copia de seguridad de todos los archivos devueltos por [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) y [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) (de lo contrario, se producirá un error en la operación de restauración). Consulte la página de referencia de **CertSrvBackupTruncateLogs** para obtener más información.
12. Llame a [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) para determinar los nombres de los archivos que no son de base de datos para realizar la copia de seguridad. Estos archivos solo se identifican mediante la función y se deben realizar copias de seguridad de otros medios.
13. Realice una copia de seguridad de los archivos dinámicos identificados en el paso 12, utilizando rutinas independientes de Certadm.dll.
14. Llame a [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) para finalizar la sesión de copia de seguridad.
15. Llame a [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) según sea necesario para liberar los búferes asignados por determinadas funciones de copia de seguridad de servicios de certificados. Las llamadas a [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw), [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)y [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) asignarán los búferes que se pueden liberar mediante una llamada a **CertSrvBackupFree**.
16. Libere los recursos de Certadm.dll llamando a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Para obtener información acerca de los privilegios necesarios para realizar una copia de seguridad de la base de datos de servicios de certificados y los archivos asociados, vea [establecer los privilegios de copia de seguridad y restauración](setting-the-backup-and-restore-privileges.md).

 

 
