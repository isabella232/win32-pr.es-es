---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Los valores del registro asociados al \_ software del \_ equipo local HKEY \\ \\ Microsoft \\ OLE Key controlan la configuración predeterminada de los permisos de inicio y de acceso, y las capacidades de seguridad de nivel de llamada para las aplicaciones basadas en com que no llaman a CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076284"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE

Los valores del registro asociados al **\_ software del \_ equipo local HKEY \\ \\ Microsoft \\ OLE** Key controlan la configuración predeterminada de los permisos de inicio y de acceso, y las capacidades de seguridad de nivel de llamada para las aplicaciones basadas en com que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Solo los administradores, el creador de objetos y el sistema tienen acceso total a esta parte del registro. El resto de usuarios tienen acceso de solo lectura.



| Valor del Registro                                                                         | Descripción                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error de inicio y activación de componentes.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Controla el comportamiento de las llamadas desde el administrador de control de servicios (DCOMSCM) DCOM local a un DCOMSCM remoto.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Define la lista de permisos de acceso predeterminada para el equipo.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Define la ACL de inicio predeterminada para el equipo.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Establece la Directiva de activación global para el equipo.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Establece el nivel de detalle de las entradas del registro de eventos acerca de los descriptores de seguridad no válidos para el inicio y los permisos de acceso de los componentes.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Establece el nivel de autenticación predeterminado.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Establece el nivel de suplantación predeterminado.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Determina el nivel de seguridad de las invocaciones de liberación de **AddRef** /  .                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Establece la Directiva de restricción para todo el equipo para el acceso a componentes.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Establece la Directiva de restricción para todo el equipo para el inicio y activación de componentes.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para instalarse en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Determina si los niveles de confianza de la Directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Determina si los intentos de conexión a objetos en ejecución se filtran para los niveles de confianza de la Directiva de restricción de software (SRP) compatible.                                         |



 

 

 




