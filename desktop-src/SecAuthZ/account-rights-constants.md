---
description: Los derechos de cuenta determinan el tipo de inicio de sesión que puede realizar una cuenta de usuario. Un administrador asigna derechos de cuenta a cuentas de usuario y de grupo. Los derechos de cada cuenta de usuario incluyen aquellos concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Constantes de derechos de cuenta (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b16b75af89773df969ec78b771986b0a73dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276499"
---
# <a name="account-rights-constants"></a>Constantes de derechos de cuenta

Los derechos de cuenta determinan el tipo de inicio de sesión que puede realizar una cuenta de usuario. Un administrador asigna derechos de cuenta a cuentas de usuario y de grupo. Los derechos de cuenta de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

Un administrador del sistema puede usar las funciones de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) para trabajar con derechos de cuenta. Las funciones [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) y [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) agregan o quitan derechos de cuenta de una cuenta. La función [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera los derechos de cuenta que mantiene una cuenta especificada. La función [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera las cuentas que contienen un derecho de cuenta especificado.

Las siguientes constantes de derecha de cuenta se utilizan para controlar la capacidad de inicio de sesión de una cuenta. Las funciones [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) o [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) producen un error si la cuenta que ha iniciado sesión no tiene los derechos de cuenta necesarios para el tipo de inicio de sesión que se está realizando.



| Constante o valor                                                                                                                                                                                                                                                                                                                           | Descripción                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**Se \_ Texto \_ del \_ nombre de inicio de sesión por lotes**</dt> <dt>("SeBatchLogonRight")</dt> </dl>                                                                         | Necesario para que una cuenta inicie sesión con el tipo de inicio de sesión por lotes.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**Se \_ Denegar el texto de \_ \_ \_ nombre de inicio de sesión por lotes**</dt> <dt>("SeDenyBatchLogonRight")</dt> </dl>                                                     | Deniega explícitamente a una cuenta el derecho a iniciar sesión con el tipo de inicio de sesión por lotes.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**Se \_ Denegar texto de \_ \_ \_ nombre de inicio de sesión interactivo**</dt> <dt>("SeDenyInteractiveLogonRight")</dt> </dl>                             | Deniega explícitamente a una cuenta el derecho a iniciar sesión con el tipo de inicio de sesión interactivo.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**Se \_ Denegar texto de \_ \_ \_ nombre de inicio de sesión de red**</dt> <dt>("SeDenyNetworkLogonRight")</dt> </dl>                                             | Deniega explícitamente a una cuenta el derecho a iniciar sesión con el tipo de inicio de sesión de red.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**Se \_ Denegar texto de \_ \_ nombre de inicio de \_ sesión \_ interactivo remoto**</dt> <dt>("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Deniega explícitamente a una cuenta el derecho de iniciar sesión de forma remota mediante el tipo de inicio de sesión interactivo.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**Se \_ Denegar \_ \_ \_ el nombre de inicio de sesión del servicio**</dt> <dt>("SeDenyServiceLogonRight")</dt> </dl>                                             | Deniega explícitamente a una cuenta el derecho a iniciar sesión con el tipo de inicio de sesión del servicio.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**Se \_ Texto \_ del \_ nombre de inicio de sesión interactivo**</dt> <dt>("SeInteractiveLogonRight")</dt> </dl>                                                 | Necesario para que una cuenta inicie sesión con el tipo de inicio de sesión interactivo.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**Se \_ Texto \_ de \_ nombre de inicio de sesión de red**</dt> <dt>("SeNetworkLogonRight")</dt> </dl>                                                                 | Necesario para que una cuenta inicie sesión con el tipo de inicio de sesión de red.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**Se \_ Texto \_ del \_ \_ nombre de inicio de sesión interactivo remoto**</dt> <dt>("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Necesario para que una cuenta inicie sesión de forma remota con el tipo de inicio de sesión interactivo.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**Se \_ Texto \_ del \_ nombre de inicio de sesión del servicio**</dt> <dt>("SeServiceLogonRight")</dt> </dl>                                                                 | Necesario para que una cuenta inicie sesión con el tipo de inicio de sesión del servicio.<br/>                             |



## <a name="remarks"></a>Observaciones

Los \_ derechos de denegación de se reemplazan a los derechos de cuenta correspondientes. Un administrador puede asignar un \_ derecho denegar a una cuenta para invalidar los derechos de inicio de sesión que puede tener una cuenta como resultado de la pertenencia a un grupo. Por ejemplo, puede asignar el nombre de \_ Inicio de sesión de red se \_ \_ a todos los usuarios, pero debe asignar el \_ derecho de \_ \_ Inicio de sesión de red se deniega \_ a los administradores para evitar la administración remota de equipos.

Todas las funciones de LSA mencionadas en la introducción anterior admiten los derechos de cuenta y los [privilegios](privilege-constants.md). Sin embargo, a diferencia de los privilegios, las funciones [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) y [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) no admiten los derechos de cuenta. La función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) obtendrá información sobre los derechos de cuenta si TokenGroups, y no TokenPrivileges, se especifica como el valor del parámetro *TokenInformationClass* .

Las constantes de derecha de la cuenta anterior se definen como cadenas en Ntsecapi. h. Por ejemplo, la \_ constante de \_ nombre de inicio de sesión interactivo \_ se define como "SeInteractiveLogonRight".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

