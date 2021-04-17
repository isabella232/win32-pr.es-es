---
description: Asociación que conecta un servicio de conmutador virtual a un servicio de puente transparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666333"
---
# <a name="msvm_hostedswitchservice-class"></a>MSVM \_ HostedSwitchService (clase)

Asociación que conecta un servicio de conmutador virtual a un servicio de puente transparente.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ HostedSwitchService** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ HostedSwitchService** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa el servicio de puente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ HostedSwitchService** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HostedService de CIM \_**](cim-hostedservice.md)
</dt> <dt>

[**HostedService de CIM \_**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

