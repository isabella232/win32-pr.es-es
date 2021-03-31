---
description: Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a la serie de especificaciones de IEEE 802,11.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910397"
---
# <a name="cim_wifiport-class"></a>\_Clase WiFiPort de CIM

Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a la serie de especificaciones de IEEE 802,11.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ WiFiPort** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ WiFiPort** tiene estas propiedades.

<dl> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")
</dt> </dl>

El ancho de banda máximo admitido, en bits por segundo, basado en el modo de funcionamiento especificado en la propiedad **portType** . Por ejemplo, **MaxSpeed** es "11 millones" Si **PortType** contiene "71" (802.11 b).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")
</dt> </dl>

Una matriz que contiene las direcciones MAC de IEEE 802 EUI-48. La dirección MAC tiene el formato de doce dígitos hexadecimales, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")
</dt> </dl>

La dirección MAC de IEEE 802 EUI-48 del puerto. La dirección MAC tiene el formato de doce dígitos hexadecimales, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("portType")
</dt> </dl>

El modo de funcionamiento 802,11 que está habilitado en el puerto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

**802.11 a** (70)


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

**802.11 b** (71)


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

**802.11 g** (72)


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

**802.11 n** (73)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (16000...)


</dt> <dd></dd> </dl>

</dd> <dt>

**Velocidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("velocidad")
</dt> </dl>

La velocidad de datos a la que se recibió la unidad de datos del protocolo PPDU (PLCP (Protocolo de convergencia de capa física) actual, en bits por segundo. Este valor se codifica en los primeros 4 bits del encabezado PLCP en cada fotograma PLCP.

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

[**\_NETWORKPORT CIM**](cim-networkport.md)
</dt> </dl>

 

