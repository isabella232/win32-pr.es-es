---
description: Establece el parámetro rights como un mapa de bits con cada bit correspondiente a un derecho de acceso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Método GetCallerAccessRights de la __SystemSecurity clase
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
ms.openlocfilehash: 770a4a51a6a0ea9e38e8c5bd6fed944b473a41373933cee497e98fd8f9952422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110030"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Método GetCallerAccessRights de la \_ \_ clase SystemSecurity

El **\_ \_ método SystemSecurity::GetCallerAccessRights** establece el parámetro *rights* como un mapa de bits con cada bit correspondiente a un derecho de acceso. Cualquier cliente puede llamar a esto para determinar qué derechos tiene el cliente. Este método es útil para los clientes que habilitan o deshabilitan características. Por ejemplo, una aplicación guia podría deshabilitar un botón si el usuario que ha iniciado sesión actualmente no tiene derechos de ejecución de métodos.

Cualquier cliente habilitado tiene derecho a llamar a **GetCallerAccessRights,** incluso si ese cliente no tiene derechos generales de ejecución de métodos.

## <a name="syntax"></a>Sintaxis


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*derechos* \[ out\]
</dt> <dd>

Derechos de acceso del cliente. Para obtener más información, [**\_ \_ vea SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE** (1 (0x1))


</dt> <dd>

Habilita la cuenta y concede al usuario permisos de lectura. Este es el derecho de acceso predeterminado para todos los usuarios.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ METHOD \_ EXECUTE** (2 (0x2))


</dt> <dd>

Permite la ejecución de métodos.

> [!Note]  
> Los proveedores pueden realizar comprobaciones de acceso adicionales.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ REP \_ DE \_ ESCRITURA COMPLETA** (4 (0x4))


</dt> <dd>

Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban en clases e instancias, excepto en las clases del sistema.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ PARTIAL \_ WRITE \_ REP** (8 (0x8))


</dt> <dd>

Permite al autor de la llamada, al contexto de seguridad o al usuario escribir instancias de proveedor, pero no clases estáticas ni instancias estáticas en el repositorio.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ PROVEEDOR \_ DE** ESCRITURA (16 (0x10))


</dt> <dd>

Permite que el autor de la llamada, el contexto de seguridad o el usuario escriban clases e instancias en proveedores.

> [!Note]  
> La suplantación de proveedores puede realizar comprobaciones de acceso adicionales.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ ACCESO \_ REMOTO** (32 (0x20))


</dt> <dd>

Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos establecidos por otros bits.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**READ \_ CONTROL** (131072 (0x20000))


</dt> <dd>

Permite el acceso de lectura a los descriptores de seguridad.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCRITURA \_ DAC** (262144 (0x40000))


</dt> <dd>

Permite el acceso de escritura a listas de control de acceso discrecional (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **HRESULT** que indica el estado de la llamada al método. En la lista siguiente se enumeran los valores devueltos que son significativos [**para Set9XUserList**](--systemsecurity-set9xuserlist.md). Para el scripting Visual Basic aplicaciones, el resultado se puede obtener de [OutParameters.ReturnValue](parsing-outparameters-objects.md). Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**MÉTODO WBEM \_ E \_ \_ DESHABILITADO**
</dt> <dd>

Este método no se admite en las versiones admitidas de Windows.

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

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[Constantes de seguridad WMI](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

Constantes de seguridad WMI
</dt> </dl>

 

