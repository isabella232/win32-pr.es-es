---
description: Asocia un conmutador Ethernet virtual a las extensiones enlazadas actualmente a él.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Msvm_HostedEthernetSwitchExtension clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dda28d4d5893f05ef067016da771b8dc510ba5588dd4f25ed89dfe7c4a8aa2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522985"
---
# <a name="msvm_hostedethernetswitchextension-class"></a>Clase \_ HostedEthernetSwitchExtension de Msvm

Asocia un conmutador Ethernet virtual a las extensiones enlazadas actualmente a él.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedEthernetSwitchExtension de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedEthernetSwitchExtension de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a una instancia de la clase [**\_ VirtualEthernetSwitch de Msvm**](msvm-virtualethernetswitch.md) que representa el conmutador virtual.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**\_ EthernetSwitchExtension de Msvm**](msvm-ethernetswitchextension.md) que representa la instancia de extensión switch enlazada al conmutador virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

