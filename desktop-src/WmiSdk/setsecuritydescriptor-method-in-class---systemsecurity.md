---
description: Escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se representa mediante una instancia de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706653"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método SetSecurityDescriptor de la \_ \_ clase SystemSecurity

El método [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se representa mediante una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ de\]
</dt> <dd>

Descriptor de seguridad asociado al espacio de nombres WMI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener más información, vea [códigos de retorno de WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

Finalización correcta.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tiene acceso a la información solicitada.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido.

</dd> <dt>

**9**
</dt> <dd>

El usuario no tiene los privilegios adecuados para ejecutar el método.

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado en la llamada al método no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de Access Control del sistema*](/windows/desktop/SecGloss/a-gly) (SACL). Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).

Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**constantes de privilegios**](privilege-constants.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).

Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.

Los valores siguientes en [**el \_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan la DACL o la SACL, o ambas.

-   **DACL de SE \_ \_ presente**

    Indica que se debe actualizar la DACL. Si no se establece, WMI conserva el valor original de la DACL.

-   **la \_ SACL de se \_ presente**

    Indica que se debe actualizar la SACL. Si no se establece, WMI conserva el valor original de la SACL. Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** . En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**. Para obtener más información, vea [**constantes de privilegios**](privilege-constants.md).

Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan. De lo contrario, WMI conserva los valores originales. Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md).

Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> </dl>

 

