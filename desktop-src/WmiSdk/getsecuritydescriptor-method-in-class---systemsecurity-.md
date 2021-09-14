---
description: Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se devuelve como una instancia de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la __SystemSecurity clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965283"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método GetSecurityDescriptor de la \_ \_ clase SystemSecurity

El **método GetSecurityDescriptor** obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se devuelve como una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ out\]
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

## <a name="remarks"></a>Observaciones

La [**instancia \_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos [**SECURITY DESCRIPTOR \_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). Para obtener más información, [vea Access Control enumeraciones](/windows/desktop/SecAuthZ/access-control-lists).

Si no se concede o se habilita **SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**Constantes de privilegios**](privilege-constants.md) y [Ejecución de operaciones con privilegios.](executing-privileged-operations.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

