---
description: Identifica la información de seguridad relacionada con el objeto que se establece o se consulta.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275626"
---
# <a name="security_information"></a>información de seguridad \_

El tipo de datos de **\_ información de seguridad** identifica la información de seguridad relacionada con el objeto que se establece o se consulta. Esta información de seguridad incluye:

-   Propietario de un objeto.
-   Grupo principal de un objeto
-   La [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto
-   La [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) de un objeto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Observaciones

Algunos miembros de **\_ información de seguridad** solo funcionan con la función [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) . Estos miembros no se devuelven en la estructura devuelta por otras funciones de seguridad, como [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Cada elemento de información de seguridad se designa mediante una marca de bits. Cada marcador de bits puede ser uno de los valores siguientes. Para obtener más información, vea las funciones [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) y [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) .



| Valor/derechos necesarios para consultar o establecer                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_información de seguridad de atributos \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho obligatorio para establecer: **escribir \_ DAC**<br/>                                                                                     | Propiedades de recurso del objeto al que se hace referencia. Las propiedades de recurso se almacenan \_ en \_ tipos ACE de atributo de recurso del sistema \_ en la SACL del descriptor de seguridad.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                 |
| información de seguridad de copia de \_ seguridad \_<br/> Derecho necesario para consultar: **\_ control de lectura** y **acceso a la \_ \_ seguridad del sistema**<br/> Derecho necesario para establecer: **escribir \_ DAC** y **escribir el \_ propietario** y **acceder a la \_ \_ seguridad del sistema**<br/> | Todas las partes del descriptor de seguridad. Esto resulta útil para el software de copia de seguridad y restauración que necesita conservar todo el descriptor de seguridad.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                                                  |
| \_información de seguridad de DACL \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho obligatorio para establecer: **escribir \_ DAC**<br/>                                                                                          | La DACL del objeto al que se hace referencia.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_información de seguridad de grupo \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho obligatorio para establecer: **\_ propietario de escritura** <br/>                                                                                      | Se está haciendo referencia al identificador de grupo principal del objeto.<br/>                                                                                                                                                                                                                                                                                                    |
| \_información de seguridad de etiqueta \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho obligatorio para establecer: **\_ propietario de escritura** <br/>                                                                                      | Se está haciendo referencia a la etiqueta de integridad obligatoria.<br/> La etiqueta de integridad obligatoria es una ACE en la SACL del objeto.<br/> **Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/>                                                                                                                                    |
| \_información de seguridad del propietario \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho obligatorio para establecer: **\_ propietario de escritura** <br/>                                                                                      | Se está haciendo referencia al identificador del propietario del objeto.<br/>                                                                                                                                                                                                                                                                                                            |
| \_información de \_ seguridad de DACL protegida \_<br/> Derecho necesario para consultar: no disponible<br/> Derecho obligatorio para establecer: **escribir \_ DAC**<br/>                                                                                   | La DACL no puede heredar [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE).<br/>                                                                                                                                                                                                                   |
| \_información de \_ seguridad \_ SACL protegida<br/> Derecho necesario para consultar: no disponible<br/> Derecho necesario para establecer: **acceso a la \_ \_ seguridad del sistema**<br/>                                                                     | La SACL no puede heredar ACE.<br/>                                                                                                                                                                                                                                                                                                                                      |
| \_información de seguridad de SACL \_<br/> Derecho necesario para consultar: **acceso a la \_ \_ seguridad del sistema**<br/> Derecho necesario para establecer: **acceso a la \_ \_ seguridad del sistema**<br/>                                                                 | Se hace referencia a la SACL del objeto.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_información de seguridad del ámbito \_<br/> Derecho necesario para consultar: **\_ control de lectura**<br/> Derecho necesario para establecer: **acceso a la \_ \_ seguridad del sistema**<br/>                                                                           | El identificador de la Directiva de acceso central (CAP) aplicable en el objeto al que se hace referencia. Cada identificador de CAP se almacena en un tipo de ACE de identificador de directiva de ámbito del sistema \_ \_ \_ \_ en la SACL del SD.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca de bits no está disponible.<br/> <br/> |
| información de seguridad de DACL desprotegida \_ \_ \_<br/> Derecho necesario para consultar: no disponible<br/> Derecho obligatorio para establecer: **escribir \_ DAC**<br/>                                                                                 | La DACL hereda las ACE del objeto primario.<br/>                                                                                                                                                                                                                                                                                                                     |
| información de seguridad de SACL no protegida \_ \_ \_<br/> Derecho necesario para consultar: no disponible<br/> Derecho necesario para establecer: **acceso a la \_ \_ seguridad del sistema**<br/>                                                                   | La SACL hereda las ACE del objeto primario.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



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

 

