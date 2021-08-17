---
title: Errores de copia de seguridad en Active Directory Domain Services
description: En este tema se enumeran los valores devueltos de errores de copia de seguridad para las funciones Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Active Directory de copia de seguridad
- Dominio de Active Directory de copia de seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5038b1d3a7a1f24c2e3b8dbf137aa2722073650b878e1d6a1dfdec8cac399a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024142"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Errores de copia de seguridad en Active Directory Domain Services

En este tema se enumeran los valores devueltos de errores de copia de seguridad para las funciones Active Directory Domain Services.



| Value                                      | Descripción                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hr Rr.**<br/>                       | La función no se implementa.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Parámetro no válido.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Se ha producido un error interno.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | El identificador no es válido.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | El proceso de restauración está en curso.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | El archivo especificado está abierto.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Los destinatarios no son válidos. <br/>                                                                                                                                                    |
| **hrConnectldNotConnect**<br/>           | No se puede realizar la copia de seguridad. No se detectó una conexión con el servidor de copia de seguridad especificado o el servicio del que está intentando realizar una copia de seguridad no se está ejecutando.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Existe una asignación de restauración para el componente especificado. Se puede especificar un mapa de restauración al realizar una restauración completa.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Otra aplicación ha modificado la base de datos Windows NT/Windows 2000 Directory Service especificada, de forma que se producirá un error en las copias de seguridad posteriores. Para corregirlo, realice una copia de seguridad completa.<br/> |
| **hrLogFileNotFound**<br/>           | No se puede realizar una copia de seguridad incremental porque no se encontró Windows archivo de registro de base de datos nt/Windows servicio de directorio 2000.<br/>                                        |
| **hrCircularLogging**<br/>           | El Windows nt/Windows de servicio de directorio 2000 especificado está configurado para usar registros de base de datos circulares. No se puede realizar una copia de seguridad incrementalmente. Realice una copia de seguridad completa.<br/>       |
| **hrNoFullRestore**<br/>             | Las bases de datos no se han restaurado en este equipo. No puede restaurar una copia de seguridad incremental hasta que se haya restaurado una copia de seguridad completa.<br/>                                            |
| **hrCommunicationError**<br/>        | Error de comunicaciones al intentar realizar una copia de seguridad local.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Debe realizar una copia de seguridad completa para poder realizar una copia de seguridad incremental.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Falta el token de expiración. No se puede restaurar sin los datos de expiración.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | El token de expiración está en un formato irreconocible.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | El contenido de DS de la copia de seguridad no está actualizado. Restaure con una copia reciente.<br/>                                                                                                            |



 

## <a name="see-also"></a>Consulte también

[Correcto,](success.md) [Errores del sistema en Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), Errores del Administrador de directorios, Errores de registro y recuperación en funciones de [Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), Valores devueltos para funciones [en Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md) [](directory-manager-errors.md)


 

 





