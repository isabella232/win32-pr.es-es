---
description: Un objeto protegible es un objeto que puede tener un descriptor de seguridad.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Objetos protegibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867a40e781d9d7f97302ed6e592a7fc26d61b939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810712"
---
# <a name="securable-objects"></a>Objetos protegibles

Un objeto protegible es un objeto que puede tener un [descriptor de seguridad](security-descriptors.md). Todos los objetos de Windows con nombre son protegibles. Algunos objetos sin nombre, como los objetos de [*proceso*](/windows/desktop/SecGloss/p-gly) y de subprocesos, también pueden tener descriptores de seguridad. Para la mayoría de los objetos protegibles, puede especificar el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) de un objeto en la llamada de función que crea el objeto. Por ejemplo, puede especificar un descriptor de seguridad en las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Además, las funciones de seguridad de Windows permiten obtener y establecer la información de seguridad para los objetos protegibles creados en sistemas operativos distintos de Windows. Las funciones de seguridad de Windows también proporcionan compatibilidad para el uso de descriptores de seguridad con objetos privados definidos por la aplicación. Para obtener más información acerca de los objetos protegibles privados, vea [Access Control cliente/servidor](client-server-access-control.md).

Cada tipo de objeto protegible define su propio conjunto de [derechos de acceso](access-rights-and-access-masks.md) específicos y su propia [asignación de derechos de acceso genéricos](generic-access-rights.md). Para obtener información sobre los derechos de acceso específicos y genéricos para cada tipo de objeto protegible, vea la información general de ese tipo de objeto.

En la tabla siguiente se muestran las funciones que se usan para manipular la información de seguridad de algunos objetos protegibles comunes.



| Tipo de objeto                                                                                                                                           | Funciones de descriptor de seguridad                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Archivos o directorios](/windows/desktop/FileIO/file-security-and-access-rights) en un sistema de archivos NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Canalizaciones con nombre](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Canalizaciones anónimas](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Procesos](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Subprocesos](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objetos de asignación de archivos](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Tokens de acceso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objetos de administración de Windows ([estaciones de ventana](/windows/desktop/winstation/window-station-security-and-access-rights) y equipos de [escritorio](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Claves del Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Servicios de Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Impresoras locales o remotas                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Recursos compartidos de red                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de sincronización entre procesos](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventos, exclusiones mutuas, semáforos y temporizadores que esperan)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objetos de trabajo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Objetos del servicio de directorio                                                                                                                             | Los objetos Active Directory controlan estos objetos. Para obtener más información, vea [Active Directory interfaces de servicio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 

