---
description: Un derecho de acceso es una marca de bits que corresponde a un conjunto determinado de operaciones que un subproceso puede realizar en un objeto protegible.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Derechos de acceso y máscaras de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f06cdf447f9d91c1553ea5fb6b3b7d1f324dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423924"
---
# <a name="access-rights-and-access-masks"></a>Derechos de acceso y máscaras de acceso

Un *derecho de acceso* es una marca de bits que corresponde a un conjunto determinado de operaciones que un subproceso puede realizar en un objeto protegible. Por ejemplo, una clave del registro tiene el \_ derecho de acceso del valor del conjunto de claves \_ , que corresponde a la capacidad de un subproceso de establecer un valor bajo la clave. Si un subproceso intenta realizar una operación en un objeto, pero no tiene el derecho de acceso necesario al objeto, el sistema no realiza la operación.

Una [*máscara de acceso*](/windows/desktop/SecGloss/a-gly) es un valor de 32 bits cuyos bits corresponden a los derechos de acceso admitidos por un objeto. Todos los objetos protegibles de Windows utilizan un [formato de máscara de acceso](access-mask-format.md) que incluye bits para los siguientes tipos de derechos de acceso:

-   [Derechos de acceso genéricos](generic-access-rights.md)
-   [Derechos de acceso estándar](standard-access-rights.md)
-   [Derecho de acceso SACL](sacl-access-right.md)
-   [Derechos de acceso de servicios de directorio](directory-services-access-rights.md)

Cuando un subproceso intenta abrir un identificador de un objeto, el subproceso normalmente especifica una máscara de acceso para [solicitar un conjunto de derechos de acceso](requesting-access-rights-to-an-object.md). Por ejemplo, una aplicación que necesita establecer y consultar los valores de una clave del registro puede abrir la clave mediante una máscara de acceso para solicitar el \_ valor del conjunto \_ de claves y los derechos de acceso del valor de la consulta de clave \_ \_ .

En la tabla siguiente se muestran las funciones que manipulan la información de seguridad para cada tipo de objeto protegible.



| Tipo de objeto                                                                                                                                           | Funciones de descriptor de seguridad                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Archivos o directorios](/windows/desktop/FileIO/file-security-and-access-rights) en un sistema de archivos NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Canalizaciones[anónimas](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights) [con nombre](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Búferes de pantalla de la consola                                                                                                                                | No se admite.                                                                                                                                                                                     |
| [Procesa los](/windows/desktop/ProcThread/process-security-and-access-rights)[subprocesos](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objetos de asignación de archivos](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Tokens de acceso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objetos de administración de Windows ([estaciones de ventana](/windows/desktop/winstation/window-station-security-and-access-rights) y equipos de [escritorio](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Claves del Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Servicios de Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Impresoras locales o remotas                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Recursos compartidos de red                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de sincronización entre procesos](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventos, exclusiones mutuas, semáforos y temporizadores que esperan)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de trabajo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

