---
description: Asociación genérica que se usa para establecer parte de las relaciones entre una instancia de CIM VirtualSystemSettingData y una o varias instancias de \_ \_ RESOURCEAllocationSettingData de CIM.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 485ac065f91a83479081a3cddd89cbae5b6eaa95bc3a30733371075226f58cdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083155"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>Clase Msvm \_ VirtualSystemSettingDataComponent

Asociación genérica que se usa para establecer relaciones de "parte de" entre una instancia de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) y una o varias instancias de [**\_ RESOURCEAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)de CIM.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualSystemSettingDataComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemSettingDataComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Override**, **Min** (1), **Max** (1)
</dt> </dl>

Elemento primario de la asociación. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingDataComponent.**](/previous-versions//cc150674(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento secundario de la asociación. Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingDataComponent.**](/previous-versions//cc150674(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase Msvm \_ VirtualSystemSettingDataComponent** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ VirtualSystemSettingDataComponent**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

