---
description: Representa la configuración de descarga del conmutador.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Msvm_EthernetSwitchHardwareOffloadSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 751e5f3256da82d2b7cae2da17a8b9dfb54bc5331ebf2679e745bc67c0b4d3b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524554"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a>Clase Msvm \_ EthernetSwitchHardwareOffloadSettingData

Representa la configuración de descarga del conmutador.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchHardwareOffloadSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchHardwareOffloadSettingData** tiene estas propiedades.

<dl> <dt>

**DefaultQueueVmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica la configuración de VMMQ para la cola predeterminada del vswitch.

</dd> <dt>

**DefaultQueueVmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el número de colas para la cola predeterminada.

</dd> <dt>

**DefaultQueueVrssEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica la configuración de las VRs para la cola predeterminada del vswitch.

</dd> <dt>

**DefaultQueueVrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica si la CPU de VMQ principal se excluye de la tabla de direccionamiento indirecto de VRSS/VMMQ.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**DefaultQueueVrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica si se debe realizar siempre la propagación de VRSS para la cola predeterminada, independientemente del estado RSS del vPort externo.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**DefaultQueueVrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica el número mínimo de colas usadas para VRSS/VMMQ.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**DefaultQueueVrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica cómo las colas VRSS/VMMQ se dirige a distintos procesadores de host.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




