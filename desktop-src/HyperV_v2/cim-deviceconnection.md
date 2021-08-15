---
description: Una relación que indica que dos o más dispositivos están conectados juntos.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection (administración de Hyper-V)
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
ms.openlocfilehash: 81ec2826339e27d956750360b280fcafd7b55e6264a6bcab83ebc1cb41a1ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812849"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>CIM_DeviceConnection (administración de Hyper-V)

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

La **clase \_ DeviceConnection** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceConnection** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un dispositivo

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un segundo dispositivo que está conectado al otro dispositivo.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Asociación de puertos de bus DMTF \| \| 001.3"), **PUnit** ("bit")
</dt> </dl>

Cuando son posibles varios anchos de datos de bus y conexión, la propiedad NegotiatedDataWidth define el que está en uso entre los dispositivos. El ancho de datos se especifica en bits. Si no se negocia el ancho de datos o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| Bus Port Association \| 001.2"), **PUnit** ("bit/second")
</dt> </dl>

Cuando son posibles varias velocidades de conexión y bus, esta propiedad define la velocidad que se usa entre los dispositivos, en bits por segundo. Si no se negocian las velocidades de conexión o bus, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en "0".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

