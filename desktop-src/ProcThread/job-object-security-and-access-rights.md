---
description: El modelo Windows seguridad de Microsoft permite controlar el acceso a los objetos de trabajo. Para obtener más información sobre la seguridad, vea Access-Control modelo.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Derechos de acceso y seguridad de objetos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62111a630b5fd8ee4639505bedec192155f3775f4c284ff1455b8eea63d21d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978505"
---
# <a name="job-object-security-and-access-rights"></a>Derechos de acceso y seguridad de objetos de trabajo

El modelo Windows seguridad de Microsoft permite controlar el acceso a los objetos de trabajo. Para obtener más información sobre la seguridad, vea [Modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un [descriptor de seguridad para](../secauthz/security-descriptors.md) un objeto de trabajo al llamar a la función [**CreateJobObject.**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) Si especifica NULL, el objeto de trabajo obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para un objeto de trabajo proceden del token principal o de suplantación del creador.

Para obtener o establecer el descriptor de seguridad para un objeto de trabajo, llame a la función [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo)

Los derechos de acceso válidos para los objetos de trabajo incluyen [los derechos de acceso estándar](../secauthz/standard-access-rights.md) y algunos derechos de acceso específicos del trabajo. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Value                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DELETE** (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                           |
| **READ \_ CONTROL** (0x00020000L) | Necesario para leer información en el descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho **de acceso ACCESS SYSTEM \_ \_ SECURITY.** Para obtener más información, vea [SACL Access Right](../secauthz/sacl-access-right.md). |
| **SYNCHRONIZE** (0x00100000L)   | Derecho a utilizar el objeto para la sincronización. Esto permite que un subproceso espere hasta que el objeto esté en estado señalado.                                                                                                                                                                |
| **ESCRITURA \_ DAC** (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad del objeto .                                                                                                                                                                                                                   |
| **ESCRITURA \_ OWNER** (0x00080000L)  | Necesario para cambiar el propietario en el descriptor de seguridad del objeto.                                                                                                                                                                                                                  |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del trabajo.



| Value                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **JOB \_ OBJECT \_ ALL \_ ACCESS** (0x1F001F)             | Combina todos los derechos de acceso a objetos de trabajo válidos.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **JOB \_ PROCESO \_ DE \_ ASIGNACIÓN DE** OBJETOS (0x0001)           | Necesario para llamar a [**la función AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) para asignar procesos al objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                |
| **JOB \_ OBJECT \_ QUERY** (0x0004)                     | Necesario para recuperar cierta información sobre un objeto de trabajo, como atributos e información de contabilidad (vea [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) [**e IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **JOB \_ ATRIBUTOS \_ DE \_ CONJUNTO DE** OBJETOS (0x0002)           | Necesario para llamar a [**la función SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) para establecer los atributos del objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                |
| **JOB \_ ATRIBUTOS \_ DE SEGURIDAD DEL CONJUNTO \_ \_ DE** OBJETOS (0x0010) | Esta marca no se admite. Debe establecer las limitaciones de seguridad individualmente para cada proceso asociado a un objeto de trabajo. **Windows Server 2003 y Windows XP:** Se requiere para llamar a [**la función SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información **JobObjectSecurityLimitInformation** para establecer limitaciones de seguridad para los procesos asociados al objeto de trabajo. La compatibilidad con esta marca se quitó en Windows Vista y Windows Server 2008. <br/> |
| **JOB \_ OBJECT \_ TERMINATE** (0x0008)                 | Necesario para llamar a [**la función TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) para finalizar todos los procesos del objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                     |



 

El identificador devuelto por [**CreateJobObject tiene**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) **acceso JOB OBJECT ALL \_ \_ \_ ACCESS** al objeto de trabajo. Al llamar a la [**función OpenJobObject,**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto. Si un objeto de trabajo está en una jerarquía de trabajos anidados [,](nested-jobs.md)un llamador con acceso al objeto de trabajo tiene acceso implícitamente a todos sus trabajos secundarios en la jerarquía.

Puede solicitar el derecho **de acceso ACCESS SYSTEM \_ \_ SECURITY** a un objeto de trabajo si desea leer o escribir la SACL del objeto. Para obtener más información, vea [Listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y Derecho de acceso [sacl](../secauthz/sacl-access-right.md).

Debe establecer las limitaciones de seguridad individualmente para cada proceso asociado a un objeto de trabajo, en lugar de establecerlas para el propio objeto de trabajo. Para obtener información, vea [Derechos de acceso y seguridad de procesos.](process-security-and-access-rights.md)

**Windows Server 2003 y Windows XP:** Puede usar la función [**SetInformationJobObject para**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) establecer limitaciones de seguridad para el objeto de trabajo. Esta funcionalidad se quitó en Windows Vista y Windows Server 2008.

 

 
