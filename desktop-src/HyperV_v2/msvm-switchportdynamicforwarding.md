---
description: Conecta un puerto de conmutador a una entrada de reenvío dinámico (dirección MAC aprendida).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d5deb326877e7af639c7bc18a73a8c968e75c26b64d690d4a4582085833fa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950075"
---
# <a name="msvm_switchportdynamicforwarding-class"></a>Clase \_ SwitchPortDynamicForwarding de Msvm

Conecta un puerto de conmutador a una entrada de reenvío dinámico (dirección MAC aprendida). Esto resulta útil para buscar todas las direcciones MAC aprendidas para un puerto especificado.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SwitchPortDynamicForwarding de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SwitchPortDynamicForwarding de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa el puerto del conmutador.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ DynamicForwardingEntry de Msvm**](msvm-dynamicforwardingentry.md) que representa la entrada de reenvío dinámico de la base de datos de reenvío.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ SwitchPortDynamicForwarding de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

Consulte [Consulta de objetos de red.](querying-networking-objects.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](cim-switchportdynamicforwarding.md)
</dt> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))
</dt> </dl>

 

