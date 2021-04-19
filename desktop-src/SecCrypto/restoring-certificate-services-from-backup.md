---
description: Muestra cómo se pueden usar las funciones de copia de seguridad de servicios de Certificate Server para restaurar y recuperar una base de datos de servicios de certificados y sus archivos asociados.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Restauración de servicios de Certificate Server desde la copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f5adf46d802194909397a3b70483b3cf43bb409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688421"
---
# <a name="restoring-certificate-services-from-backup"></a>Restauración de servicios de Certificate Server desde la copia de seguridad

En el escenario siguiente se muestra cómo se pueden usar las funciones de copia de seguridad de servicios de Certificate Server para restaurar y recuperar una base de datos de servicios de certificados y sus archivos asociados. El proceso de restauración implica escribir los archivos contenidos en un conjunto de copia de seguridad en disco. Puede restaurar varios conjuntos de copia de seguridad (una copia de seguridad completa más cero o más copias de seguridad incrementales), pero todas las restauraciones se deben completar antes de comenzar el proceso de recuperación. El proceso de recuperación implica que los servicios de Certificate Server reproduzcan los archivos de registro para garantizar la coherencia de los archivos de registro y la base de datos. El escenario muestra las llamadas de función para restaurar los conjuntos de copia de seguridad e informar a los servicios de Certificate Server de los parámetros de recuperación.

Debe existir una copia de seguridad completa existente de la base de datos de servicios de certificados antes de implementar este escenario.

1.  Cargue la biblioteca de Certadm.dll en la memoria (llamando a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere la dirección de cada una de las funciones necesarias en Certadm.dll (mediante [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use estas direcciones al llamar a las funciones en los pasos restantes.
3.  Llame a [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) para determinar si los servicios de Certificate Server están en línea. Si se está ejecutando servicios de Certificate Server, ciérrelo antes de continuar. Los servicios de Certificate Server no deben estar en línea para que las operaciones de restauración se realicen correctamente.
4.  Llame a [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) para iniciar una sesión de restauración. Varias de las demás funciones utilizarán el identificador de contexto de copia de seguridad de servicios de certificados resultante.
5.  Determine la ruta de acceso de la ubicación de la base de datos. Durante un escenario de copia de seguridad, este valor habría estado disponible en una llamada a [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw); Este valor se debe haber almacenado como parte de la copia de seguridad.
6.  Cree una asignación de restauración que especifique el nombre de la base de datos restaurada. Se usa una estructura de asignación de restauración de base de datos de servicios de certificados (CSEDB \_ RSTMAPW) para especificar una asignación de restauración. Establezca el \_ miembro **PWSZDATABASENAME** de CSEDB RSTMAPW y el \_ miembro **RSTMAPW** de CSEDB pwszNewDatabaseName en la ubicación de la base de datos determinada en el paso 5. Opcionalmente, si la base de datos restaurada tiene un nombre diferente al de la base de datos de copia de seguridad, establezca el \_ miembro **PWSZNEWDATABASENAME** de CSEDB RSTMAPW en el nombre de la nueva base de datos.
7.  Si desea asegurarse de que las modificaciones realizadas en la base de datos después de realizar la copia de seguridad no se vuelvan a aplicar una vez completada la restauración de la base de datos (como parte de la recuperación de la base de datos realizada durante el siguiente inicio de servicios de servidor de certificados), elimine los archivos de la base de datos activa y los directorios de registro
8.  Copie los archivos contenidos en la copia de seguridad completa en los directorios de registro y la base de datos activa del servidor de destino.
9.  Llame a [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) para registrar una operación de restauración de la copia de seguridad completa. **CertSrvRestoreRegister** usa la asignación de restauración especificada en el paso 6. **CertSrvRestoreRegister** también especifica la ubicación de la base de datos y los registros de copia de seguridad. La llamada a **CertSrvRestoreRegister** forzará a los servicios de Certificate Server a intentar una operación de restauración la próxima vez que se inicie. También impide que los servicios de Certificate Server procesen solicitudes de certificados hasta que se complete la restauración.
10. Llame a [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), con lo que finalizará la actividad de registro que comenzó en el paso 8. Tenga en cuenta que el registro de una operación de restauración es una instrucción para que los servicios de Certificate Server sigan al iniciarse; la recuperación real solo tendrá lugar después de que se inicie servicios de Certificate Server.
11. Para restaurar cada copia de seguridad incremental, copie los archivos contenidos en la copia de seguridad incremental en el directorio de registro activo del servidor de destino y, a continuación, llame a [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw), seguido de una llamada a [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). El registro de las copias de seguridad incrementales para la restauración puede realizarse en cualquier orden, pero solo el conjunto de archivos para una copia de seguridad incremental debe copiarse en el servidor antes de cada llamada a **CertSrvRestoreRegister**.
12. Copie los archivos dinámicos de servicios de servidor de certificados en el servidor de destino. Los archivos dinámicos se habrían identificado durante la copia de seguridad cuando se llamó a [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) . Puede que sea necesario detener el servicio de publicación de World Wide Web para permitir que se sobrescriban los archivos dinámicos.
13. Llame a [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) para finalizar la sesión de restauración.
14. Inicie la aplicación de servicios de certificados manualmente (o espere hasta el siguiente reinicio para que se inicie automáticamente). Cuando se inicia servicios de Certificate Server, determinará si se ha registrado una operación de restauración; Si se ha registrado una operación de restauración, los servicios de Certificate Server iniciarán la recuperación. Los servicios de Certificate Server no procesarán ninguna solicitud de certificado hasta que se complete la operación de recuperación.

> [!Note]  
> Una vez finalizada la recuperación, es importante que realice una nueva copia de seguridad completa de la base de datos de servicios de Certificate Server. Esto es necesario para truncar los archivos de registro restaurados y establecer un conjunto de copia de seguridad base para las restauraciones futuras. Las copias de seguridad realizadas después de una restauración no se pueden mezclar con las copias de seguridad (completas o incrementales) realizadas antes de la restauración. es decir, después de restaurar una base de datos de servicios de certificados y de haber progresado a un estado posterior, no puede usar las copias de seguridad previas a la restauración para restaurar la base de datos a ese estado posterior.

 

 

 
