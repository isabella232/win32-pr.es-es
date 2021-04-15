---
title: Errores de copia de seguridad en Active Directory Domain Services
description: En este tema se enumeran los valores devueltos de error de copia de seguridad para funciones de Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Errores de copia de seguridad de Active Directory
- Errores de copia de seguridad del servicio Dominio de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9b38ba9f28e47fd95e69a923e953d59fdd4d37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486547"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Errores de copia de seguridad en Active Directory Domain Services

En este tema se enumeran los valores devueltos de error de copia de seguridad para funciones de Active Directory Domain Services.



| Value                                      | Descripción                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | La función no está implementada.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Parámetro no válido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Se ha producido un error interno.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | El identificador no es válido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | El proceso de restauración está en curso.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | El archivo especificado está abierto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Los destinatarios no son válidos. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | No se puede realizar la copia de seguridad. No se detectó una conexión con el servidor de copia de seguridad especificado o el servicio del que está intentando realizar la copia de seguridad no se está ejecutando.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Existe una asignación de restauración para el componente especificado. Se puede especificar una asignación de restauración al realizar una restauración completa.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Otra aplicación ha modificado la base de datos de servicio de directorio de Windows NT/Windows 2000 especificada de modo que se producirá un error en las copias de seguridad posteriores. Para solucionarlo, realice una copia de seguridad completa.<br/> |
| **hrLogFileNotFound**<br/>           | No se puede realizar una copia de seguridad incremental porque no se encontró un archivo de registro de base de datos del servicio de directorio de Windows NT/Windows 2000.<br/>                                        |
| **hrCircularLogging**<br/>           | El componente de servicio de directorio de Windows NT/Windows 2000 especificado está configurado para usar registros de base de datos circulares. No se puede realizar una copia de seguridad incremental. Realice una copia de seguridad completa.<br/>       |
| **hrNoFullRestore**<br/>             | Las bases de datos no se han restaurado en este equipo. No se puede restaurar una copia de seguridad incremental hasta que se haya restaurado una copia de seguridad completa.<br/>                                            |
| **hrCommunicationError**<br/>        | Error de comunicación al intentar realizar una copia de seguridad local.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Debe realizar una copia de seguridad completa antes de poder realizar una copia de seguridad incremental.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Falta el token de expiración. No se puede restaurar sin los datos de expiración.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | El token de expiración tiene un formato irreconocible.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | El contenido de DS de la copia de seguridad no está actualizado. Restaure con una copia reciente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Consulte también

[Correctos](success.md), [errores del sistema en Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), [errores del administrador de directorios](directory-manager-errors.md), [errores de registro y recuperación en funciones de Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [valores devueltos para las funciones de Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





