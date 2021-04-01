---
description: Contiene métodos que permiten obtener acceso y modificar la configuración de seguridad de un espacio de nombres.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity (clase)
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
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156929"
---
# <a name="__systemsecurity-class"></a>\_\_Clase SystemSecurity

La clase del sistema **\_ \_ SystemSecurity** contiene métodos que permiten obtener acceso a la configuración de seguridad de un espacio de nombres y modificarla. La clase **\_ \_ SystemSecurity** es una clase singleton en cada espacio de nombres.

> [!Note]  
> Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ SystemSecurity** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **\_ \_ SystemSecurity** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></td>
<td style="text-align: left;">Obtiene una lista de usuarios a los que se permite el acceso remoto.<br/>
<blockquote>
[!Note]<br />
Este método no funciona en las versiones compatibles de Windows. En su lugar, <a href="--systemsecurity-getsd.md"><strong>se usa.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></td>
<td style="text-align: left;">Devuelve una máscara con cada bit que corresponde a un derecho de acceso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-getsd.md"><strong>Se obtiene</strong></a></td>
<td style="text-align: left;">Obtiene el <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> del espacio de nombres al que está conectado el usuario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI asociado a la instancia de <strong>__SystemSecurity</strong>. El descriptor de seguridad se devuelve como una instancia de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></td>
<td style="text-align: left;">Establece una lista de usuarios a los que se permite el acceso remoto.<br/>
<blockquote>
[!Note]<br />
Este método no funciona en las versiones compatibles de Windows. En su lugar, use <a href="--systemsecurity-setsd.md"><strong>establecido</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-setsd.md"><strong>Establecido</strong></a></td>
<td style="text-align: left;">Establece el descriptor de seguridad para el espacio de nombres al que está conectado el usuario.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora. El descriptor de seguridad se representa mediante una instancia de <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Puede requerir que las aplicaciones y los scripts de cliente usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo. mof que crea el espacio de nombres. También puede modificar un espacio de nombres existente agregando este atributo y compilando de nuevo el archivo. mof. Para obtener más información sobre cómo usar **RequiresEncryption**, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[Listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**Descriptor de seguridad \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

