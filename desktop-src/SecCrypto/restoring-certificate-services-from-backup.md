---
description: Muestra cómo se pueden usar las funciones de copia de seguridad de Servicios de certificados para restaurar y recuperar una base de datos de Servicios de certificados y sus archivos asociados.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Restauración de servicios de certificados a partir de la copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f5adf46d802194909397a3b70483b3cf43bb409
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476363"
---
# <a name="restoring-certificate-services-from-backup"></a>Restauración de servicios de certificados a partir de la copia de seguridad

En el escenario siguiente se muestra cómo se pueden usar las funciones de copia de seguridad de Servicios de certificados para restaurar y recuperar una base de datos de Servicios de certificados y sus archivos asociados. El proceso de restauración implica escribir los archivos contenidos en un conjunto de copia de seguridad en el disco. Puede restaurar varios conjuntos de copia de seguridad (una copia de seguridad completa más cero o más copias de seguridad incrementales), pero todas las restauraciones deben completarse antes de comenzar el proceso de recuperación. El proceso de recuperación implica la reproducción de archivos de registro de Certificate Services para garantizar la coherencia de la base de datos y del archivo de registro, lo que garantiza la integridad de la base de datos. El escenario muestra las llamadas de función para restaurar los conjuntos de copia de seguridad e informar a Certificate Services de los parámetros de recuperación.

Debe existir una copia de seguridad completa existente de la base de datos de Servicios de certificados antes de implementar este escenario.

1.  Cargue la biblioteca Certadm.dll en la memoria (mediante una llamada [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recupere la dirección de cada una de las funciones necesarias Certadm.dll (por medio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Use estas direcciones al llamar a las funciones en los pasos restantes.
3.  Llame [**a CertSrvIsServerOnline para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) determinar si Certificate Services está en línea. Si Servicios de certificados se está ejecutando, cállelo antes de continuar. Servicios de certificados no debe estar en línea para que las operaciones de restauración sean correctas.
4.  Llame [**a CertSrvRestorePrepare para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) iniciar una sesión de restauración. Varias de las demás funciones usarán el identificador de contexto de copia de seguridad de Servicios de certificados resultante.
5.  Determine la ruta de acceso de la ubicación de la base de datos. Durante un escenario de copia de seguridad, este valor habría estado disponible en una llamada a [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw); este valor se debe haber almacenado como parte de la copia de seguridad.
6.  Cree un mapa de restauración que especifique el nombre de la base de datos restaurada. Se usa una estructura de mapa de restauración de base de datos de Servicios de certificados (CSEDB \_ RSTMAPW) para especificar una asignación de restauración. Establezca el miembro \_ **pwszDatabaseName** de CSEDB RSTMAPW y el miembro \_ **pwszNewDatabaseName** de CSEDB RSTMAPW en la ubicación de la base de datos determinada en el paso 5. Opcionalmente, si la base de datos restaurada debe tener un nombre diferente al de la base de datos de copia de seguridad, establezca el miembro \_ **pwszNewDatabaseName** de CSEDB RSTMAPW en el nuevo nombre de la base de datos.
7.  Si desea asegurarse de que las modificaciones realizadas en la base de datos después de realizar la copia de seguridad no se vuelvan a aplicar una vez completada la restauración de la base de datos (como parte de la recuperación de la base de datos realizada durante el siguiente inicio de Servicios de certificados), elimine los archivos de los directorios de registro y la base de datos activas del servidor de destino.
8.  Copie los archivos contenidos en la copia de seguridad completa en los directorios de registro y la base de datos activas del servidor de destino.
9.  Llame [**a CertSrvRestoreRegister para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) registrar una operación de restauración para la copia de seguridad completa. **CertSrvRestoreRegister** usa el mapa de restauración especificado en el paso 6. **CertSrvRestoreRegister también** especifica la ubicación de la base de datos de copia de seguridad y los registros. Llamar **a CertSrvRestoreRegister** obligará a Certificate Services a intentar una operación de restauración la próxima vez que se inicia. También impide que Servicios de certificados procese solicitudes de certificado hasta que se complete la restauración.
10. Llame [**a CertSrvRestoreRegisterComplete,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)finalizando así la actividad de registro que se inició en el paso 8. Tenga en cuenta que el registro de una operación de restauración es una instrucción que Certificate Services debe seguir cuando se inicia. la recuperación real tendrá lugar solo después de iniciar Servicios de certificado.
11. Para cada copia de seguridad incremental que se va a restaurar, copie los archivos contenidos en la copia de seguridad incremental en el directorio de registro activo del servidor de destino y, a continuación, llame a [**CertSrvRestoreRegister,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)seguido de una llamada a [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). El registro de las copias de seguridad incrementales para la restauración puede producirse en cualquier orden, pero solo el conjunto de archivos de una copia de seguridad incremental debe copiarse en el servidor antes de cada llamada a **CertSrvRestoreRegister**.
12. Copie los archivos dinámicos de Servicios de certificados en el servidor de destino. Los archivos dinámicos se habrían identificado durante la copia de seguridad cuando se llamó [**a CertSrvBackupGetDynamicFileList.**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) Puede que sea necesario detener el servicio de World Wide Web para permitir sobrescribir los archivos dinámicos.
13. Llame [**a CertSrvRestoreEnd para**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) finalizar la sesión de restauración.
14. Inicie la aplicación Servicios de certificados manualmente (o espere hasta el siguiente reinicio para que se inicie automáticamente). Cuando se inicia Certificate Services, determinará si se ha registrado una operación de restauración. Si se ha registrado una operación de restauración, Servicios de certificados iniciará la recuperación. Servicios de certificados no procesará ninguna solicitud de certificado hasta que se complete la operación de recuperación.

> [!Note]  
> Una vez completada la recuperación, es importante realizar una nueva copia de seguridad completa de la base de datos de Servicios de certificados. Esto es necesario para truncar los archivos de registro restaurados y establecer un conjunto de copia de seguridad base para futuras restauraciones. Las copias de seguridad realizadas después de una restauración no se pueden mezclar con copias de seguridad (completas o incrementales) realizadas antes de la restauración; Es decir, después de restaurar una base de datos de servicios de certificados y haber progresado a un estado posterior, no puede usar las copias de seguridad previas a la restauración para restaurar la base de datos a ese estado posterior.

 

 

 
