---
description: Identifica la información de seguridad relacionada con objetos que se va a establecer o consultar.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eda92db81cc2325dcc2eb084c06aa5ac7ca92475cca92d8221e394af9704c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907205"
---
# <a name="security_information"></a>INFORMACIÓN DE \_ SEGURIDAD

El **tipo de datos SECURITY \_ INFORMATION** identifica la información de seguridad relacionada con objetos que se va a establecer o consultar. Esta información de seguridad incluye:

-   Propietario de un objeto
-   Grupo principal de un objeto
-   Lista [*de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto
-   Lista [*de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL) de un objeto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Comentarios

Algunos **miembros de SECURITY \_ INFORMATION** solo funcionan con [**la función SetNamedSecurityInfo.**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) Estos miembros no se devuelven en la estructura devuelta por otras funciones de seguridad como [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Cada elemento de información de seguridad se designa mediante una marca de bits. Cada marca de bits puede ser uno de los siguientes valores. Para obtener más información, vea las [**funciones SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) y [**QuerySecurityAccessMask.**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)



| Valor o derechos necesarios para consultar o establecer                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INFORMACIÓN DE \_ SEGURIDAD DE \_ ATRIBUTOS<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **WRITE \_ DAC**<br/>                                                                                     | Propiedades de recursos del objeto al que se hace referencia. Las propiedades del recurso se almacenan en tipos DE ACE DE ATRIBUTO DE RECURSO DEL \_ \_ SISTEMA en la \_ SACL del descriptor de seguridad.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                 |
| INFORMACIÓN DE \_ SEGURIDAD DE COPIA DE \_ SEGURIDAD<br/> Derecho necesario para consultar: **CONTROL \_ DE LECTURA** y SEGURIDAD DEL SISTEMA DE **\_ \_ ACCESO**<br/> Derecho necesario para establecer: **ESCRIBIR \_ DAC y** WRITE OWNER **\_ y** **ACCESS SYSTEM \_ \_ SECURITY**<br/> | Todas las partes del descriptor de seguridad. Esto es útil para el software de copia de seguridad y restauración que necesita conservar todo el descriptor de seguridad.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                                                  |
| INFORMACIÓN DE SEGURIDAD DE DACL \_ \_<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **WRITE \_ DAC**<br/>                                                                                          | Se hace referencia a la DACL del objeto .<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMACIÓN DE \_ SEGURIDAD \_ DE GRUPO<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **WRITE \_ OWNER** <br/>                                                                                      | Se hace referencia al identificador de grupo principal del objeto.<br/>                                                                                                                                                                                                                                                                                                    |
| INFORMACIÓN DE \_ SEGURIDAD DE \_ ETIQUETAS<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **WRITE \_ OWNER** <br/>                                                                                      | Se hace referencia a la etiqueta de integridad obligatoria.<br/> La etiqueta de integridad obligatoria es una ACE en la SACL del objeto .<br/> **Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                                                                                                                                    |
| INFORMACIÓN DE \_ SEGURIDAD DEL \_ PROPIETARIO<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **WRITE \_ OWNER** <br/>                                                                                      | Se hace referencia al identificador de propietario del objeto.<br/>                                                                                                                                                                                                                                                                                                            |
| INFORMACIÓN \_ DE SEGURIDAD DE DACL \_ \_ PROTEGIDA<br/> Derecho necesario para consultar: No disponible<br/> Derecho necesario para establecer: **WRITE \_ DAC**<br/>                                                                                   | La DACL no puede [*heredar las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE).<br/>                                                                                                                                                                                                                   |
| INFORMACIÓN \_ DE SEGURIDAD DE SACL \_ \_ PROTEGIDA<br/> Derecho necesario para consultar: No disponible<br/> Derecho necesario para establecer: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                     | La SACL no puede heredar las ACE.<br/>                                                                                                                                                                                                                                                                                                                                      |
| INFORMACIÓN DE \_ SEGURIDAD DE \_ SACL<br/> Derecho necesario para consultar: **ACCESS \_ SYSTEM \_ SECURITY**<br/> Derecho necesario para establecer: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                 | Se hace referencia a la SACL del objeto.<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMACIÓN DE \_ SEGURIDAD DEL \_ ÁMBITO<br/> Derecho necesario para consultar: **READ \_ CONTROL**<br/> Derecho necesario para establecer: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                           | Identificador de directiva de acceso central (CAP) aplicable al objeto al que se hace referencia. Cada identificador cap se almacena en un tipo ACE de id. de directiva con ámbito del sistema \_ \_ en la \_ \_ SACL de la SD.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/> |
| INFORMACIÓN DE SEGURIDAD \_ DE DACL \_ NO \_ PROTEGIDA<br/> Derecho necesario para consultar: No disponible<br/> Derecho necesario para establecer: **WRITE \_ DAC**<br/>                                                                                 | La DACL hereda las ACE del objeto primario.<br/>                                                                                                                                                                                                                                                                                                                     |
| INFORMACIÓN DE SEGURIDAD \_ DE SACL \_ NO \_ PROTEGIDA<br/> Derecho necesario para consultar: No disponible<br/> Derecho necesario para establecer: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                   | La SACL hereda las ACE del objeto primario.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de acceso](access-control.md)
</dt> <dt>

[Estructuras de Access Control básicas](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

