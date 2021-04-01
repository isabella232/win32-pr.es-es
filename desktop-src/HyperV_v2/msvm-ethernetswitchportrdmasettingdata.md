---
description: Representa los datos de configuración de la característica RDMA de puerto.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Msvm_EthernetSwitchPortRdmaSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913890"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a>MSVM \_ EthernetSwitchPortRdmaSettingData (clase)

Representa los datos de configuración de la característica RDMA de puerto.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ EthernetSwitchPortRdmaSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ EthernetSwitchPortRdmaSettingData** tiene estas propiedades.

<dl> <dt>

**RdmaOffloadWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

El peso asignado a este puerto para el RDMA invitado. El peso es la importancia relativa al asignar recursos RDMA. Al establecer la propiedad **RdmaOffloadWeight** en 0, se deshabilita RDMA en el puerto. El valor predeterminado es 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




