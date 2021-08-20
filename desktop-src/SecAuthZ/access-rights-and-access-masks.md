---
description: Un derecho de acceso es una marca de bits que corresponde a un conjunto determinado de operaciones que un subproceso puede realizar en un objeto protegible.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Derechos de acceso y máscaras de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1238766e2e4c8629b6c3a508b30d1e8832314d2e8ddd5ffdf4a1b93085f3c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914362"
---
# <a name="access-rights-and-access-masks"></a>Derechos de acceso y máscaras de acceso

Un *derecho de* acceso es una marca de bits que corresponde a un conjunto determinado de operaciones que un subproceso puede realizar en un objeto protegible. Por ejemplo, una clave del Registro tiene el derecho de acceso KEY SET VALUE, que corresponde a la capacidad de un subproceso de establecer un \_ \_ valor bajo la clave. Si un subproceso intenta realizar una operación en un objeto, pero no tiene el derecho de acceso necesario al objeto , el sistema no lleva a cabo la operación.

Una [*máscara de*](/windows/desktop/SecGloss/a-gly) acceso es un valor de 32 bits cuyos bits corresponden a los derechos de acceso admitidos por un objeto . Todos Windows objetos protegibles usan un formato de máscara de [acceso](access-mask-format.md) que incluye bits para los siguientes tipos de derechos de acceso:

-   [Derechos de acceso genéricos](generic-access-rights.md)
-   [Derechos de acceso estándar](standard-access-rights.md)
-   [Derecho de acceso sacl](sacl-access-right.md)
-   [Derechos de acceso de servicios de directorio](directory-services-access-rights.md)

Cuando un subproceso intenta abrir un identificador en un objeto , el subproceso normalmente especifica una máscara de acceso para [solicitar un conjunto de derechos de acceso](requesting-access-rights-to-an-object.md). Por ejemplo, una aplicación que necesita establecer y consultar los valores de una clave del Registro puede abrir la clave mediante una máscara de acceso para solicitar los derechos de acceso KEY SET VALUE y \_ \_ KEY QUERY \_ \_ VALUE.

En la tabla siguiente se muestran las funciones que manipulan la información de seguridad para cada tipo de objeto protegible.



| Tipo de objeto                                                                                                                                           | Funciones descriptoras de seguridad                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Archivos o directorios](/windows/desktop/FileIO/file-security-and-access-rights) en un sistema de archivos NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Canalizaciones con nombre](/windows/desktop/ipc/named-pipe-security-and-access-rights)[Canalizaciones anónimas](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Búferes de pantalla de la consola                                                                                                                                | No compatible.                                                                                                                                                                                     |
| [Subprocesos de](/windows/desktop/ProcThread/process-security-and-access-rights)[procesos](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objetos de asignación de archivos](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Tokens de acceso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objetos de administración de ventanas[(estaciones de ventana](/windows/desktop/winstation/window-station-security-and-access-rights) [y escritorios)](/windows/desktop/winstation/desktop-security-and-access-rights) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Claves del Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Servicios de Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Impresoras locales o remotas                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Recursos compartidos de red                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de sincronización entre procesos](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventos, exclusiones mutuas, semáforos y temporizadores que se pueden esperar)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de trabajo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

