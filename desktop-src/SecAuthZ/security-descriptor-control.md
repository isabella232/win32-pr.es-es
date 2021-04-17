---
description: Conjunto de marcadores de bits que califican el significado de un descriptor de seguridad o sus componentes.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666659"
---
# <a name="security_descriptor_control"></a>\_control de descriptor de seguridad \_

El tipo de datos **\_ \_ control del descriptor de seguridad** es un conjunto de marcadores de bits que califican el significado de un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) o sus componentes. Cada descriptor de seguridad tiene un miembro de **control** que almacena los bits de **\_ \_ control del descriptor de seguridad** .


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Observaciones

Para obtener los bits de control de un descriptor de seguridad, llame a la función [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Para establecer los bits de control de un descriptor de seguridad, utilice las funciones para modificar los descriptores de seguridad. Para obtener una lista de estas funciones, consulte la sección Vea también.

Las aplicaciones pueden usar la función [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) para establecer los bits de control relacionados con la herencia automática de ACE.

El valor del control recuperado por la función [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) puede incluir una combinación de las siguientes marcas de bits de **\_ \_ control del descriptor de seguridad** .



| Value                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_solicitud de \_ \_ herencia automática de DACL \_ de se<br/> 0x0100<br/> | Indica un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) necesario en el que la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) está configurada para admitir la propagación automática de [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) heredadas a objetos secundarios existentes.<br/> En el caso de [*las listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) que admiten la herencia automática, este bit siempre se establece. Los servidores protegidos pueden llamar a la función [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para convertir un descriptor de seguridad y establecer esta marca. <br/> |
| SE \_ \_ heredó automáticamente la DACL de se \_<br/> 0x0400<br/>    | Indica un descriptor de seguridad en el que la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) se configura para admitir la propagación automática de [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) heredadas a objetos secundarios existentes.<br/> En el caso de [*las listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) que admiten la herencia automática, este bit siempre se establece. Los servidores protegidos pueden llamar a la función [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para convertir un descriptor de seguridad y establecer esta marca. <br/>                                                                                                  |
| \_valor predeterminado de DACL de se \_<br/> 0x0008<br/>          | Indica un descriptor de seguridad con una DACL predeterminada. Por ejemplo, si el creador de un objeto no especifica una DACL, el objeto recibe la DACL predeterminada del [*token de acceso*](/windows/desktop/SecGloss/a-gly) del creador. Esta marca puede afectar a la forma en que el sistema trata la DACL con respecto a la herencia de ACE. El sistema omite esta marca si \_ \_ no se ha establecido la marca de DACL de este.<br/> Esta marca se usa para determinar cómo se calculará la DACL final en el objeto y no se almacena físicamente en el control de descriptor de seguridad del objeto protegible.<br/> Para establecer esta marca, utilice la función [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| DACL de SE \_ \_ presente<br/> 0x0004<br/>            | Indica un descriptor de seguridad que tiene una DACL. Si no se establece esta marca, o si se establece esta marca y la DACL es **null**, el descriptor de seguridad permite el acceso completo a todos los usuarios.<br/> Esta marca se usa para contener la información de seguridad especificada por un llamador hasta que el descriptor de seguridad está asociado a un objeto protegible. Una vez que el descriptor de seguridad está asociado a un objeto protegible, la marca de DACL de SE encuentra \_ \_ siempre establecida en el control de descriptor de seguridad.<br/> Para establecer esta marca, utilice la función [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| DACL de SE \_ \_ protegió<br/> 0x1000<br/>          | Impide que las ACE heredables modifiquen la DACL del descriptor de seguridad. Para establecer esta marca, utilice la función [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_valor predeterminado del grupo se \_<br/> 0x0002<br/>         | Indica que un mecanismo predeterminado proporcionó el [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del grupo de descriptores de seguridad. Este marcador lo puede utilizar un administrador de recursos para identificar objetos cuyo grupo de descriptores de seguridad se ha establecido mediante un mecanismo predeterminado. Para establecer esta marca, utilice la función [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| propietario de la propiedad SE ha \_ \_ predeterminado<br/> 0x0001<br/>         | Indica que un mecanismo predeterminado proporcionó el SID del propietario del descriptor de seguridad. Este marcador lo puede utilizar un administrador de recursos para identificar objetos cuyo propietario fue establecido por un mecanismo predeterminado. Para establecer esta marca, utilice la función [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SE trata de un \_ \_ control RM \_ válido<br/> 0x4000<br/>       | Indica que el control del administrador de recursos es válido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_solicitud de \_ \_ herencia automática de SACL \_ de se<br/> 0x0200<br/> | Indica un descriptor de seguridad necesario en el que la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) está configurada para admitir la propagación automática de ACE heredables a objetos secundarios existentes.<br/> El sistema establece este bit cuando realiza el algoritmo de herencia automática para el objeto y sus objetos secundarios existentes. Para convertir un descriptor de seguridad y establecer esta marca, los servidores protegidos pueden llamar a la función [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) .<br/>                                                                                                                                                                                                                                                                                   |
| \_SACL automática de se \_ \_ heredó<br/> 0x0800<br/>    | Indica un descriptor de seguridad en el que la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) está configurada para admitir la propagación automática de ACE heredables a objetos secundarios existentes.<br/> El sistema establece este bit cuando realiza el algoritmo de herencia automática para el objeto y sus objetos secundarios existentes. Para convertir un descriptor de seguridad y establecer esta marca, los servidores protegidos pueden llamar a la función [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) . <br/>                                                                                                                                                                                                                                                                                           |
| \_ \_ valores predeterminados de SACL de se<br/> 0x0008<br/>          | Un mecanismo predeterminado, en lugar del [*proveedor*](/windows/desktop/SecGloss/p-gly) original del descriptor de seguridad, proporcionó la SACL. Esta marca puede afectar a la forma en que el sistema trata la SACL con respecto a la herencia de ACE. El sistema omite esta marca si \_ \_ no se ha establecido la marca de SACL de se presente. Para establecer esta marca, utilice la función [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| la \_ SACL de se \_ presente<br/> 0x0010<br/>            | Indica un descriptor de seguridad que tiene una SACL. Para establecer esta marca, utilice la función [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SE \_ \_ protegió SACL<br/> 0x2000<br/>          | Impide que las ACE heredables modifiquen la SACL del descriptor de seguridad. Para establecer esta marca, utilice la función [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ auto- \_ relación<br/> 0x8000<br/>           | Indica un [*descriptor de seguridad autorelativo*](/windows/desktop/SecGloss/s-gly). Si no se establece esta marca, el descriptor de seguridad está en un formato absoluto. Para obtener más información, vea [descriptores de seguridad absolutos y Self-Relative](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Access Control de bajo nivel](low-level-access-control.md)
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

 

