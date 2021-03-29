---
description: Enumera las funciones de compatibilidad proporcionadas por el conjunto de herramientas de configuración de seguridad.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Funciones de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912257"
---
# <a name="security-management-functions"></a>Funciones de administración de seguridad

Esta sección contiene temas para los siguientes grupos de funciones:

-   [Funciones de devolución de llamada Attachment](#attachment-callback-functions)
-   [Funciones del motor de datos adjuntos](#attachment-engine-functions)
-   [Funciones de directiva de LSA](#lsa-policy-functions)
    -   [Funciones de Directiva](#lsa-policy-functions)
    -   [Funciones de cuenta](#account-functions)
    -   [Funciones de dominio de confianza](#trusted-domain-functions)
    -   [Funciones de datos privadas](#private-data-functions)
    -   [Funciones varias](#miscellaneous-functions)
-   [Funciones de cuenta de servicio administrada](#managed-service-account-functions)
-   [Funciones de filtro de contraseñas](#password-filter-functions)
-   [Funciones más seguras](#safer-functions)

## <a name="attachment-callback-functions"></a>Funciones de devolución de llamada Attachment

Las siguientes funciones de soporte se proporcionan mediante el conjunto de herramientas de configuración de seguridad y los motores de datos adjuntos y los complementos de extensión pueden utilizarla para leer y escribir datos de configuración.



| Función de devolución de llamada                                         | Descripción                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_información gratuita de PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Se usa para liberar memoria asignada por estas funciones de soporte.<br/>                        |
| [**\_información de registro de PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Se utiliza para registrar el mensaje en el archivo de registro de configuración o de análisis.<br/>          |
| [**\_información de consulta de PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Se utiliza para consultar la información de configuración y análisis de un servicio específico.<br/> |
| [**PFSCE \_ establecer \_ información**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Se usa para establecer la información de configuración y análisis para un servicio específico.<br/>       |



 

## <a name="attachment-engine-functions"></a>Funciones del motor de datos adjuntos



| Función                                                              | Descripción                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Implementado por el archivo DLL del motor de datos adjuntos. El motor de configuración de seguridad llama a esta función cuando se analiza el sistema.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Implementado por el archivo DLL del motor de datos adjuntos. El motor de configuración de seguridad llama a esta función cuando el sistema está configurado.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Implementado por el archivo DLL del motor de datos adjuntos. El motor de configuración de seguridad llama a esta función cuando recibe una solicitud de actualización de la configuración de la extensión del complemento de datos adjuntos.<br/> |



 

## <a name="lsa-policy-functions"></a>Funciones de directiva de LSA

En los temas siguientes se proporciona información de referencia para las funciones de directiva de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA).



| Tema                               | Descripción                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funciones de Directiva<br/>         | Funciones de detalles que se usan para abrir el objeto de [**Directiva**](policy-object.md) local y para establecer o recuperar información global de la Directiva.<br/>                                                  |
| Funciones de cuenta<br/>        | Funciones de detalles que se usan para administrar los permisos de cuenta y para crear y eliminar cuentas de usuario.<br/>                                                                                       |
| Funciones de dominio de confianza<br/> | Funciones de detalles utilizadas para crear y eliminar relaciones de dominio de confianza, así como para establecer y recuperar información acerca de los dominios de confianza.<br/>                                          |
| Funciones de datos privadas<br/>   | No utilice las funciones de datos privadas de LSA. En su lugar, use las funciones [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .<br/> |
| Funciones varias<br/>  | Funciones de detalles no descritas en ningún otro lugar.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Funciones de Directiva

Las funciones siguientes enumeran las cuentas de usuario y los dominios de confianza, reciben notificaciones de cambio de directiva y nombres de cuenta de búsqueda y SID.



| Función                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Enumera todas las cuentas que tienen un permiso de usuario especificado.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Enumera los dominios de confianza.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Asigna los nombres especificados a sus SID. Devuelve el SID como un par de SID de dominio o RID.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Asigna los nombres especificados a sus SID. Devuelve el SID como un único elemento.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Recupera el [*identificador local único*](/windows/desktop/SecGloss/l-gly) (LUID) usado por la autoridad de [*seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) para representar el nombre de privilegio especificado.<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Asigna los nombres de cuenta especificados a sus SID.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registra un objeto de evento para recibir notificaciones cuando cambia la información de la directiva local.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Anula el registro de un objeto de evento que recibe notificaciones de cambio de directiva.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Funciones de cuenta

Las siguientes funciones agregan, enumeran y eliminan permisos para una cuenta.



| Función                                                                  | Descripción                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Agregar permisos a una cuenta. Si la cuenta aún no existe, se crea.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Enumerar los permisos concedidos a una cuenta.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Quitar permisos de una cuenta. Cuando se quitan todos los permisos, la cuenta se elimina.<br/> |



 

### <a name="trusted-domain-functions"></a>Funciones de dominio de confianza

Las siguientes funciones crean, enumeran y eliminan dominios de confianza y establecen y recuperan información de dominio de confianza.



| Función                                                                                                                                                    | Descripción                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Crea un nuevo objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Quita un objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Enumera los dominios en los que confía actualmente el sistema local.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Abre un identificador de un objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Recupera información sobre un dominio de confianza. El dominio se especifica mediante SID.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Recupera información sobre un dominio de confianza. El dominio se especifica mediante el nombre.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Establece la información de un dominio de confianza. El dominio se especifica mediante el nombre.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Establece la información de un dominio de confianza. El dominio se especifica mediante SID.<br/>         |



 

### <a name="private-data-functions"></a>Funciones de datos privadas

No utilice las funciones de datos privadas de LSA. En su lugar, use las funciones [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .



| Función                                                            | Descripción                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Recupera y descifra una cadena.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Cifra y almacena una cadena.<br/>    |



 

### <a name="miscellaneous-functions"></a>Funciones varias

La API de directiva de LSA tiene las tres funciones siguientes que no caben en ninguna de las otras categorías de funciones de directiva de LSA.



| Función                                                          | Descripción                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Cierra un identificador de un objeto de [**Directiva**](policy-object.md) o un objeto [**TrustedDomain**](trusteddomain-object.md) .<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Libera un búfer asignado por una función LSA.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Convierte un valor de **NTSTATUS** en un código de error de Windows.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Funciones de cuenta de servicio administrada

Las siguientes funciones se usan para crear, enumerar, buscar y eliminar cuentas de servicio administradas.



| Función                                                                      | Descripción                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Crea una cuenta de servicio administrada.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Enumera las cuentas de servidor en el servidor especificado.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Comprueba si la cuenta de servicio especificada existe en el almacén Netlogon en el servidor especificado.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Elimina la cuenta de servicio especificada de la base de datos [Active Directory](/windows/desktop/AD/active-directory-domain-services) .<br/> |



 

## <a name="password-filter-functions"></a>Funciones de filtro de contraseñas

Las siguientes funciones de [*filtro de contraseña*](/windows/desktop/SecGloss/p-gly) se implementan mediante archivos dll de filtro de contraseña personalizados para proporcionar el filtrado de contraseña y la notificación de cambio de contraseña.



| Función                                                            | Descripción                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Indica que se ha inicializado un archivo DLL de filtro de contraseña.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Indica que se ha cambiado una contraseña.<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Valida una nueva contraseña basada en la Directiva de contraseñas.<br/>   |



 

## <a name="safer-functions"></a>Funciones más seguras

Se pueden usar las siguientes funciones más seguras para comprobar el nivel más seguro de cualquier archivo ejecutable y registrar los eventos.



| Función                                                         | Descripción                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Cierra un identificador de \_ nivel más seguro \_ abierto mediante la función [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) o la función [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) .<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Restringe un token mediante el uso de las restricciones especificadas por un controlador de nivel más seguro \_ \_ .<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Abre un controlador de nivel más seguro \_ \_ .<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Recupera información sobre un nivel de directiva.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Recupera información sobre una directiva.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Recupera información sobre un nivel.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Determina si un archivo especificado es un archivo ejecutable.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Envía un mensaje al registro de eventos.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Establece la información sobre un nivel de directiva.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Establece los controles de directiva global.<br/>                                                                                                                                          |



 

 

