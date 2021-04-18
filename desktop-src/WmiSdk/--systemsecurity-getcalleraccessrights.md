---
description: Establece el parámetro Rights como un mapa de bits con cada bit correspondiente a un derecho de acceso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Método GetCallerAccessRights de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706845"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Método GetCallerAccessRights de la \_ \_ clase SystemSecurity

El método **\_ \_ SystemSecurity:: GetCallerAccessRights** establece el parámetro *Rights* como un mapa de bits con cada bit correspondiente a un derecho de acceso. Cualquier cliente puede llamar a este método para determinar qué derechos tiene el cliente. Este método es útil para los clientes que habilitan o deshabilitan características de. Por ejemplo, una aplicación GUI podría deshabilitar un botón si el usuario que ha iniciado sesión actualmente no tiene derechos de ejecución del método.

Cualquier cliente habilitado tiene derecho a llamar a **GetCallerAccessRights**, incluso si ese cliente no tiene derechos de ejecución de método general.

## <a name="syntax"></a>Sintaxis


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*derechos* \[ de enuncia\]
</dt> <dd>

Derechos de acceso del cliente. Para obtener más información, vea [**\_ \_ SystemSecurity**](--systemsecurity.md) y las [constantes de seguridad WMI](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ HABILITAR** (1 (0x1))


</dt> <dd>

Habilita la cuenta y concede al usuario permisos de lectura. Este es el derecho de acceso predeterminado para todos los usuarios.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTODO \_ Execute** (2 (0X2))


</dt> <dd>

Permite la ejecución de métodos.

> [!Note]  
> Los proveedores pueden realizar comprobaciones de acceso adicionales.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Rellenado completo de \_ escritura \_** (4 (0x4))


</dt> <dd>

Permite que el llamador, el contexto de seguridad o el usuario escriba en clases e instancias excepto en las clases del sistema.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Rep. de escritura parcial** (8 (0x8))


</dt> <dd>

Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban instancias de proveedor, pero no clases estáticas o instancias estáticas en el repositorio.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Proveedor de escritura** (16 (0x10))


</dt> <dd>

Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban clases e instancias en los proveedores.

> [!Note]  
> Los proveedores de suplantación pueden realizar comprobaciones de acceso adicionales.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Acceso remoto** (32 (0x20))


</dt> <dd>

Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos establecidos por otros bits.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))


</dt> <dd>

Permite el acceso de lectura a los descriptores de seguridad.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))


</dt> <dd>

Permite el acceso de escritura a las listas de control de acceso discrecional (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método. En la lista siguiente se muestran los valores devueltos que son significativos para [**Set9XUserList**](--systemsecurity-set9xuserlist.md). En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E \_ método \_ deshabilitado**
</dt> <dd>

Este método no se admite en las versiones compatibles de Windows.

</dd> </dl>

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

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: obtiene**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: establecido**](--systemsecurity-setsd.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> <dt>

Constantes de seguridad de WMI
</dt> </dl>

 

