---
description: Conjunto de marcas de bits que califican el significado de un descriptor de seguridad o sus componentes.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da495f90337cd84b57c991c4c195d4d4ff971b8d15f012f724eeb1662e74a71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907405"
---
# <a name="security_descriptor_control"></a>CONTROL \_ DESCRIPTOR DE \_ SEGURIDAD

El **tipo de datos CONTROL DEL \_ \_ DESCRIPTOR** DE SEGURIDAD es un conjunto de marcas de bits que califican el significado de un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) o sus componentes. Cada descriptor de seguridad tiene un **miembro Control** que almacena los bits DE CONTROL DEL DESCRIPTOR **DE \_ \_ SEGURIDAD.**


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Comentarios

Para obtener los bits de control de un descriptor de seguridad, llame a la [**función GetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Para establecer los bits de control de un descriptor de seguridad, use las funciones para modificar descriptores de seguridad. Para obtener una lista de estas funciones, consulte la sección Consulte también.

Las aplicaciones pueden usar [**la función SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) para establecer los bits de control relacionados con la herencia automática de ace.

El valor de control recuperado por la función [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) puede incluir una combinación de las siguientes marcas de **bits DE CONTROL DEL \_ \_ DESCRIPTOR** DE SEGURIDAD.



| Value                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_SE DACL \_ AUTO \_ INHERIT \_ REQ<br/> 0x0100<br/> | Indica un [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad necesario en el que la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) está configurada para admitir la propagación automática de entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) heredables a objetos secundarios existentes.<br/> Para [*las listas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACL) que admiten la herencia automática, este bit siempre se establece. Los servidores protegidos pueden llamar a [**la función ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para convertir un descriptor de seguridad y establecer esta marca. <br/> |
| \_SE DACL \_ AUTO \_ INHERITED<br/> 0x0400<br/>    | Indica un descriptor de seguridad en el que se configura la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) para admitir la propagación automática de entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) heredables a objetos secundarios existentes.<br/> Para [*las listas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACL) que admiten la herencia automática, este bit siempre se establece. Los servidores protegidos pueden llamar a [**la función ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para convertir un descriptor de seguridad y establecer esta marca. <br/>                                                                                                  |
| \_SE DACL \_ PREDETERMINADO<br/> 0x0008<br/>          | Indica un descriptor de seguridad con una DACL predeterminada. Por ejemplo, si el creador de un objeto no especifica una DACL, el objeto recibe la DACL predeterminada del [*token*](/windows/desktop/SecGloss/a-gly) de acceso del creador. Esta marca puede afectar a cómo el sistema trata la DACL con respecto a la herencia ace. El sistema omite esta marca si no SE \_ marca DACL \_ PRESENT.<br/> Esta marca se usa para determinar cómo se va a calcular la DACL final del objeto y no se almacena físicamente en el control descriptor de seguridad del objeto protegible.<br/> Para establecer esta marca, use la [**función SetSecurityDescriptorDacl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)<br/>                                                                                                                                                                      |
| \_SE DACL \_ PRESENT<br/> 0x0004<br/>            | Indica un descriptor de seguridad que tiene una DACL. Si no se establece esta marca, o si esta marca está establecida y dacl es **NULL,** el descriptor de seguridad permite el acceso completo a todos los usuarios.<br/> Esta marca se usa para contener la información de seguridad especificada por un llamador hasta que el descriptor de seguridad está asociado a un objeto protegible. Una vez asociado el descriptor de seguridad a un objeto protegible, SE marca DACL PRESENT siempre se \_ establece en el control descriptor de \_ seguridad.<br/> Para establecer esta marca, use la [**función SetSecurityDescriptorDacl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)<br/>                                                                                                                                                                                                                                                                                                   |
| \_SE DACL \_ PROTECTED<br/> 0x1000<br/>          | Impide que las ACE heredables modifiquen la DACL del descriptor de seguridad. Para establecer esta marca, use la [**función SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_SE GROUP \_ DEFAULTED<br/> 0x0002<br/>         | Indica que el identificador [*de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del grupo de descriptores de seguridad se proporcionó mediante un mecanismo predeterminado. Un administrador de recursos puede usar esta marca para identificar objetos cuyo grupo de descriptores de seguridad se estableció mediante un mecanismo predeterminado. Para establecer esta marca, use la [**función SetSecurityDescriptorGroup.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_SE PROPIETARIO \_ PREDETERMINADO<br/> 0x0001<br/>         | Indica que el SID del propietario del descriptor de seguridad se proporcionó mediante un mecanismo predeterminado. Un administrador de recursos puede usar esta marca para identificar objetos cuyo propietario se estableció mediante un mecanismo predeterminado. Para establecer esta marca, use la [**función SetSecurityDescriptorOwner.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_SE \_RM CONTROL \_ VÁLIDO<br/> 0x4000<br/>       | Indica que el control de Resource Manager es válido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_SE SACL \_ AUTO \_ INHERIT \_ REQ<br/> 0x0200<br/> | Indica un descriptor de seguridad necesario en el que se configura la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL) para admitir la propagación automática de ACE heredables a objetos secundarios existentes.<br/> El sistema establece este bit cuando realiza el algoritmo de herencia automática para el objeto y sus objetos secundarios existentes. Para convertir un descriptor de seguridad y establecer esta marca, los servidores protegidos pueden llamar a la [**función ConvertToAutoInheritPrivateObjectSecurity.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)<br/>                                                                                                                                                                                                                                                                                   |
| \_SE SACL \_ AUTO \_ INHERITED<br/> 0x0800<br/>    | Indica un descriptor de seguridad en el que se configura la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL) para admitir la propagación automática de ACE heredables a objetos secundarios existentes.<br/> El sistema establece este bit cuando realiza el algoritmo de herencia automática para el objeto y sus objetos secundarios existentes. Para convertir un descriptor de seguridad y establecer esta marca, los servidores protegidos pueden llamar a la [**función ConvertToAutoInheritPrivateObjectSecurity.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) <br/>                                                                                                                                                                                                                                                                                           |
| \_SE SACL \_ PREDETERMINADO<br/> 0x0008<br/>          | Un mecanismo predeterminado, en lugar del [*proveedor*](/windows/desktop/SecGloss/p-gly) original del descriptor de seguridad, proporcionó la SACL. Esta marca puede afectar a cómo el sistema trata la SACL, con respecto a la herencia ace. El sistema omite esta marca si no se SE \_ la marca SACL \_ PRESENT. Para establecer esta marca, use la [**función SetSecurityDescriptorSacl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_SE SACL \_ PRESENT<br/> 0x0010<br/>            | Indica un descriptor de seguridad que tiene una SACL. Para establecer esta marca, use la [**función SetSecurityDescriptorSacl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_SE SACL \_ PROTECTED<br/> 0x2000<br/>          | Impide que las ACL heredables modifiquen la SACL del descriptor de seguridad. Para establecer esta marca, use la [**función SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_SE SELF \_ RELATIVE<br/> 0x8000<br/>           | Indica un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)auto relative . Si no se establece esta marca, el descriptor de seguridad está en formato absoluto. Para obtener más información, [vea Absolute and Self-Relative Security Descriptors](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Bajo nivel de Access Control](low-level-access-control.md)
</dt> <dt>

[Estructuras de Access Control básicas](authorization-structures.md)
</dt> <dt>

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 

