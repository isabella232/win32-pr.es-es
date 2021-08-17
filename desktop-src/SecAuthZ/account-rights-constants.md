---
description: Los derechos de cuenta determinan el tipo de inicio de sesión que puede realizar una cuenta de usuario. Un administrador asigna derechos de cuenta a cuentas de usuario y grupo. Los derechos de cuenta de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Constantes de derechos de cuenta (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4285561761908308f67585544bef6c87d2f0ebbaa25de9989f53fcab051b79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785376"
---
# <a name="account-rights-constants"></a>Constantes de derechos de cuenta

Los derechos de cuenta determinan el tipo de inicio de sesión que puede realizar una cuenta de usuario. Un administrador asigna derechos de cuenta a cuentas de usuario y grupo. Los derechos de cuenta de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

Un administrador del sistema puede usar las [*funciones de*](/windows/desktop/SecGloss/l-gly) autoridad de seguridad local (LSA) para trabajar con derechos de cuenta. Las [**funciones LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) y [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) agregan o quitan derechos de cuenta de una cuenta. La [**función LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera los derechos de cuenta que mantiene una cuenta especificada. La [**función LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera las cuentas que tienen un derecho de cuenta especificado.

Las siguientes constantes de derecho de cuenta se usan para controlar la capacidad de inicio de sesión de una cuenta. Las [**funciones LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) o [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) producirán un error si la cuenta que está iniciando sesión no tiene los derechos de cuenta necesarios para el tipo de inicio de sesión que se está realizando.



| Constante o valor                                                                                                                                                                                                                                                                                                                           | Descripción                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**SE \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeBatchLogonRight")</dt> </dl>                                                                         | Se requiere para que una cuenta inicie sesión con el tipo de inicio de sesión por lotes.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**SE \_ DENY \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyBatchLogonRight")</dt> </dl>                                                     | Deniega explícitamente a una cuenta el derecho de iniciar sesión con el tipo de inicio de sesión por lotes.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**SE \_ DENY \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyInteractiveLogonRight")</dt> </dl>                             | Deniega explícitamente a una cuenta el derecho de iniciar sesión con el tipo de inicio de sesión interactivo.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**SE \_ DENY \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyNetworkLogonRight")</dt> </dl>                                             | Deniega explícitamente a una cuenta el derecho de iniciar sesión con el tipo de inicio de sesión de red.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**SE \_ DENY \_ REMOTE INTERACTIVE LOGON \_ \_ \_ NAME**</dt> <dt>TEXT("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Deniega explícitamente a una cuenta el derecho de iniciar sesión de forma remota mediante el tipo de inicio de sesión interactivo.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**SE \_ DENY \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyServiceLogonRight")</dt> </dl>                                             | Deniega explícitamente a una cuenta el derecho de iniciar sesión con el tipo de inicio de sesión del servicio.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**SE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeInteractiveLogonRight")</dt> </dl>                                                 | Se requiere para que una cuenta inicie sesión con el tipo de inicio de sesión interactivo.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**SE \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeNetworkLogonRight")</dt> </dl>                                                                 | Se requiere para que una cuenta inicie sesión con el tipo de inicio de sesión de red.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**SE \_ REMOTE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Se requiere para que una cuenta inicie sesión de forma remota mediante el tipo de inicio de sesión interactivo.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**SE \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeServiceLogonRight")</dt> </dl>                                                                 | Se requiere para que una cuenta inicie sesión con el tipo de inicio de sesión del servicio.<br/>                             |



## <a name="remarks"></a>Comentarios

Los SE \_ deny invalidan los derechos de cuenta correspondientes. Un administrador puede asignar un SE deny a una cuenta para invalidar los derechos de inicio de sesión que una cuenta pueda tener como resultado de \_ una pertenencia a un grupo. Por ejemplo, podría asignar el derecho nombre de inicio de sesión de SE NETWORK a Todos, pero asignar el derecho SE DENEGAR NOMBRE DE INICIO DE SESIÓN DE RED a los administradores para evitar la administración remota de \_ \_ \_ \_ \_ \_ \_ equipos.

Todas las funciones de LSA mencionadas en la introducción anterior admiten derechos de cuenta [y privilegios](privilege-constants.md). Sin embargo, a diferencia de los privilegios, las funciones [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) y [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) no admiten los derechos de cuenta. La [**función GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) obtendrá información sobre los derechos de cuenta si Se especifica TokenGroups y no TokenPrivileges como valor del *parámetro TokenInformationClass.*

Las constantes de derecho de cuenta anteriores se definen como cadenas en Ntsecapi.h. Por ejemplo, la SE \_ INTERACTIVE LOGON NAME se define como \_ \_ "SeInteractiveLogonRight".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



 

