---
description: Un servidor protegido puede usar las siguientes funciones para generar informes de auditoría en el registro de eventos de seguridad.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Auditoría del acceso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac3a38a9f0af292a77a539491e0cea5f1faf40b570f34a35371ad43a7abe757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784596"
---
# <a name="auditing-access-to-private-objects"></a>Auditoría del acceso a objetos privados

Un servidor protegido puede usar las siguientes funciones para generar informes de auditoría en el registro de eventos de seguridad.



| Función                                                                                                     | Descripción                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Igual que la [**función AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) salvo que puede generar mensajes de auditoría para intentos de acceso con error o correctos.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Igual que la [**función AccessCheckByType,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) salvo que puede generar mensajes de auditoría para intentos de acceso correctos o con error.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Igual que la [**función AccessCheckByTypeResultList,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) salvo que puede generar mensajes de auditoría para intentos de acceso con error o correctos.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Igual que [**la función AccessCheckByTypeResultListAndAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) salvo que permite que el subproceso que realiza la llamada realice la comprobación de acceso antes de suplantar al cliente. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Genera un mensaje de auditoría para indicar que un cliente intentó cerrar un objeto privado.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Genera un mensaje de auditoría para indicar que un cliente intentó eliminar un objeto privado.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Genera un mensaje de auditoría para indicar que un cliente intentó abrir o crear un objeto privado.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Genera un mensaje de auditoría para indicar que un cliente intentó usar un conjunto de privilegios especificado junto con un intento de acceder a un objeto privado.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Genera un mensaje de auditoría para indicar que un cliente intentó usar un conjunto de privilegios especificado.                                                                                                                        |



 

 

 
