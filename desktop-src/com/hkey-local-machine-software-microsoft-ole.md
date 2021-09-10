---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Los valores del Registro asociados con la clave Ole de Microsoft HKEY LOCAL MACHINE SOFTWARE controlan la configuración predeterminada de los permisos de inicio y acceso y las funcionalidades de seguridad de nivel de llamada para las aplicaciones basadas en COM que no llaman a \_ \_ \\ \\ \\ CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369611"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole

Los valores del Registro asociados con la clave Ole de **\_ Microsoft HKEY LOCAL MACHINE \_ \\ SOFTWARE \\ \\** controlan la configuración predeterminada de los permisos de inicio y acceso y las funcionalidades de seguridad de nivel de llamada para las aplicaciones basadas en COM que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Solo los administradores, el creador de objetos y el sistema tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura.



| Valor del Registro                                                                         | Descripción                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error para el inicio y la activación de componentes.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Controla el comportamiento de las llamadas desde el Administrador de control de servicios DCOM (DCOMSCM) local a un DCOMSCM remoto.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Define la lista de permisos de acceso predeterminado para el equipo.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Define la ACL de inicio predeterminada para el equipo.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Establece la directiva de activación global del equipo.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Establece el nivel de detalle de las entradas del registro de eventos sobre descriptores de seguridad no válidos para los permisos de inicio y acceso de componentes.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Establece el nivel de autenticación predeterminado.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Establece el nivel de suplantación predeterminado.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Determina el nivel de seguridad de **las invocaciones** / **addRef Release.**                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Establece la directiva de restricción de todo el equipo para el acceso a componentes.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Establece la directiva de restricción de todo el equipo para el inicio y la activación de componentes.                                                                                                |
| [**Noredista**](nonredist.md)                                                         | Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para su instalación en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Determina si se usan niveles de confianza de directiva de restricción de software (SRP) durante las activaciones de ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Determina si los intentos de conectarse a objetos en ejecución se han proyectado para los niveles de confianza de la directiva de restricción de software (SRP) compatible.                                         |



 

 

 




