---
description: El modelo de seguridad de Microsoft Windows le permite controlar el acceso a los objetos de trabajo. Para obtener más información sobre la seguridad, vea modelo de Access-Control.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Derechos de acceso y seguridad de objetos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5207e459bab2ae444282355844401e0b82e9c
ms.sourcegitcommit: 18023a15a4312c653a8dcc0feef23e3413a7f5dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2021
ms.locfileid: "105678609"
---
# <a name="job-object-security-and-access-rights"></a>Derechos de acceso y seguridad de objetos de trabajo

El modelo de seguridad de Microsoft Windows le permite controlar el acceso a los objetos de trabajo. Para obtener más información sobre la seguridad, vea [modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un [descriptor de seguridad](../secauthz/security-descriptors.md) para un objeto de trabajo cuando llame a la función [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Si especifica NULL, el objeto de trabajo obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para un objeto de trabajo proceden del token principal o de suplantación del creador.

Para obtener o establecer el descriptor de seguridad de un objeto de trabajo, llame a la función [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Los derechos de acceso válidos para los objetos de trabajo incluyen los [derechos de acceso estándar](../secauthz/standard-access-rights.md) y algunos derechos de acceso específicos del trabajo. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Value                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eliminar** (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                           |
| **Leer \_ CONTROL** (0x00020000L) | Necesario para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho de acceso de **\_ \_ seguridad del sistema de acceso** . Para obtener más información, consulte [derechos de acceso de SACL](../secauthz/sacl-access-right.md). |
| **Sincronizar** (0x00100000L)   | Derecho a utilizar el objeto para la sincronización. Esto permite a un subproceso esperar hasta que el objeto se encuentra en el estado señalado.                                                                                                                                                                |
| **Escribir \_ DAC** (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad para el objeto.                                                                                                                                                                                                                   |
| **Escribir \_ PROPIETARIO** (0x00080000L)  | Necesario para cambiar el propietario del descriptor de seguridad para el objeto.                                                                                                                                                                                                                  |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del trabajo.



| Value                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Trabajo \_ de \_ \_ Acceso a objetos** (0x1F001F)             | Combina todos los derechos de acceso a objetos de trabajo válidos.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Trabajo \_ de \_ \_ Proceso de asignación de objetos** (0x0001)           | Necesario para llamar a la función [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) para asignar procesos al objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                |
| **Trabajo \_ de \_Consulta de objeto** (0x0004)                     | Necesario para recuperar cierta información sobre un objeto de trabajo, como atributos e información de cuentas (vea [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) y [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **Trabajo \_ de \_ \_ Atributos de conjunto de objetos** (0x0002)           | Necesario para llamar a la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) para establecer los atributos del objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                |
| **Trabajo \_ de \_Atributos de \_ seguridad \_ del conjunto de objetos** (0x0010) | Esta marca no se admite. Debe establecer limitaciones de seguridad individualmente para cada proceso asociado a un objeto de trabajo. **Windows Server 2003 y Windows XP:** Necesario para llamar a la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información **JobObjectSecurityLimitInformation** para establecer limitaciones de seguridad para los procesos asociados con el objeto de trabajo. Se ha quitado la compatibilidad con esta marca en Windows Vista y Windows Server 2008. <br/> |
| **Trabajo \_ de \_Finalización de objeto** (0x0008)                 | Necesario para llamar a la función [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) para finalizar todos los procesos del objeto de trabajo.                                                                                                                                                                                                                                                                                                                                                                     |



 

El identificador devuelto por [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) tiene el **objeto de trabajo \_ \_ todos los \_** accesos al objeto de trabajo. Cuando se llama a la función [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto. Si un objeto de trabajo está en una jerarquía de [trabajos anidados](nested-jobs.md), un llamador con acceso al objeto de trabajo tiene acceso implícito a todos sus trabajos secundarios en la jerarquía.

Puede solicitar el derecho de acceso de **\_ \_ seguridad del sistema de acceso** a un objeto de trabajo si desea leer o escribir la SACL del objeto. Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y [SACL](../secauthz/sacl-access-right.md).

Debe establecer limitaciones de seguridad individualmente para cada proceso asociado a un objeto de trabajo, en lugar de establecerlos para el propio objeto de trabajo. Para obtener información, consulte [seguridad de procesos y derechos de acceso](process-security-and-access-rights.md).

**Windows Server 2003 y Windows XP:** Puede usar la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) para establecer limitaciones de seguridad para el objeto de trabajo. Esta funcionalidad se ha quitado en Windows Vista y Windows Server 2008.

 

 
