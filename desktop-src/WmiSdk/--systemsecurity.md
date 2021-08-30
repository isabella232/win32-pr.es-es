---
description: Contiene métodos que permiten acceder y modificar la configuración de seguridad de un espacio de nombres.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 141e659c0ddf15c0369323e5d18d6251c3334a47
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468532"
---
# <a name="__systemsecurity-class"></a>\_\_Clase SystemSecurity

La clase del sistema **\_ \_ SystemSecurity** contiene métodos que permiten acceder a la configuración de seguridad de un espacio de nombres y modificarla. La **\_ \_ clase SystemSecurity** es una clase singleton en cada espacio de nombres.

> [!Note]  
> Para obtener más información, vea [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase SystemSecurity** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **\_ \_ clase SystemSecurity** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a> | Obtiene una lista de usuarios a los que se permite el acceso remoto.<br /><blockquote>[!Note]<br />Este método no funciona en versiones admitidas de Windows. Use <a href="--systemsecurity-getsd.md"><strong>GetSD en</strong></a> su lugar.</blockquote><br /> | 
| <a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a> | Devuelve una máscara con cada bit que corresponde a un derecho de acceso.<br /> | 
| <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> | Obtiene el <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> del espacio de nombres al que está conectado el usuario.<br /> | 
| <a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a> | Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI asociado a la instancia <strong>de __SystemSecurity</strong>. El descriptor de seguridad se devuelve como una instancia<a href="--securitydescriptor.md"><strong>de __SecurityDescriptor</strong></a>.<br /> | 
| <a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a> | Establece una lista de usuarios a los que se permite el acceso remoto.<br /><blockquote>[!Note]<br />Este método no funciona en versiones admitidas de Windows. Use <a href="--systemsecurity-setsd.md"><strong>SetSD en</strong></a> su lugar.</blockquote><br /> | 
| <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> | Establece el descriptor de seguridad del espacio de nombres al que está conectado el usuario.<br /> | 
| <a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a> | Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora. El descriptor de seguridad se representa mediante una instancia <a href="--securitydescriptor.md"><strong>de __SecurityDescriptor</strong></a>.<br /> | 




 

## <a name="remarks"></a>Comentarios

Puede requerir que los scripts de cliente y las aplicaciones usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo .mof que crea el espacio de nombres . También puede modificar un espacio de nombres existente agregando este atributo y compilando el archivo .mof de nuevo. Para obtener más información sobre cómo usar **RequiresEncryption**, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Constantes de seguridad WMI](wmi-security-constants.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[Access Control listas de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**Descriptor de \_ seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

