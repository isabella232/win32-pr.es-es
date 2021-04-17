---
description: Una relación que indica que dos o más dispositivos están conectados juntos.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687041"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>CIM_DeviceConnection (clase, administración de Hyper-V)

Una relación que indica que dos o más dispositivos están conectados juntos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a>Miembros

La **clase \_ de CIM de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceConnection de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un dispositivo

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un segundo dispositivo que está conectado al otro dispositivo.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Asociación de puerto de bus DMTF \| 001,3 "), **punitivo** (" bit ")
</dt> </dl>

Cuando se pueden usar varios buses y anchos de datos de conexión, la propiedad NegotiatedDataWidth define el que está en uso entre los dispositivos. El ancho de los datos se especifica en bits. Si no se negocia el ancho de los datos, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Asociación de puerto de bus DMTF \| 001,2 "), **punitivo** (" bit por segundo ")
</dt> </dl>

Cuando se pueden realizar varias velocidades de conexión y bus, esta propiedad define la velocidad que se utiliza entre los dispositivos, en bits por segundo. Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en "0".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

