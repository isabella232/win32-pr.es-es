---
description: Escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se representa mediante una instancia de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la __SystemSecurity clase
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
ms.openlocfilehash: d44322820514fc676c1b3ad304375f5f3ce8966a73217c6505f24659914f7853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315632"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método SetSecurityDescriptor de la \_ \_ clase SystemSecurity

El [**método SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) escribe una versión actualizada del descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se representa mediante una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ En\]
</dt> <dd>

Descriptor de seguridad asociado al espacio de nombres WMI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener más información, vea [Códigos de retorno wmi](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

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

El usuario no tiene los privilegios adecuados para ejecutar el método .

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado en la llamada al método no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**instancia \_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos [**CONTROL DE \_ \_ DESCRIPTOR**](/windows/desktop/SecAuthZ/security-descriptor-control) DE SEGURIDAD y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de Access Control sistema (SACL). [](/windows/desktop/SecGloss/a-gly) Para obtener más información, [vea Access Control .](/windows/desktop/SecAuthZ/access-control-lists)

Si no se concede o se habilita **SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**Constantes de privilegios**](privilege-constants.md) y [Ejecución de operaciones con privilegios.](executing-privileged-operations.md)

Puede actualizar la DACL y la SACL en la instancia [**\_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o solo la SACL.

Los valores siguientes de [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan dacl, sacl o ambos.

-   **\_SE DACL \_ PRESENT**

    Indica que se debe actualizar la DACL. Si no se establece, WMI conserva el valor original de la DACL.

-   **\_SE SACL \_ PRESENT**

    Indica que se debe actualizar la SACL. Si no se establece, WMI conserva el valor original de sacl. Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege.** Para el scripting, el nombre de privilegio **es SeSecurityPrivilege.** Para obtener más información, vea [**Constantes de privilegios**](privilege-constants.md).

Si las propiedades de administrador de grupo y administrador de propietarios no son **NULL,** se actualizan. De lo contrario, WMI conserva los valores originales. Para obtener más información, vea [Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md).

Cuando una sacl nueva es **NULL en** una llamada a este método, el descriptor de seguridad SACL del objeto protegible de destino se deja sin modificar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Establecer descriptores de seguridad de namepace](setting-namespace-security-descriptors.md)
</dt> </dl>

 

