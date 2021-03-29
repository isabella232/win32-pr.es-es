---
description: Un servidor protegido puede utilizar las siguientes funciones para generar informes de auditoría en el registro de eventos de seguridad.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Auditar el acceso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003128"
---
# <a name="auditing-access-to-private-objects"></a>Auditar el acceso a objetos privados

Un servidor protegido puede utilizar las siguientes funciones para generar informes de auditoría en el registro de eventos de seguridad.



| Función                                                                                                     | Descripción                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Igual que la función [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , salvo que puede generar mensajes de auditoría para intentos de acceso correctos o con errores.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Igual que la función [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) , salvo que puede generar mensajes de auditoría para los intentos de acceso correctos o con errores.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Igual que la función [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , salvo que puede generar mensajes de auditoría para los intentos de acceso correctos o con errores.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Igual que la función [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) , excepto que permite que el subproceso que realiza la llamada realice la comprobación de acceso antes de suplantar al cliente. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Genera un mensaje de auditoría para indicar que un cliente ha intentado cerrar un objeto privado.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Genera un mensaje de auditoría para indicar que un cliente intentó eliminar un objeto privado.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Genera un mensaje de auditoría para indicar que un cliente intentó abrir o crear un objeto privado.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Genera un mensaje de auditoría para indicar que un cliente intentó utilizar un conjunto de privilegios especificado junto con un intento de obtener acceso a un objeto privado.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Genera un mensaje de auditoría para indicar que un cliente intentó utilizar un conjunto de privilegios especificado.                                                                                                                        |



 

 

 
