---
description: Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a las especificaciones de la serie IEEE 802.11.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort clase
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
ms.openlocfilehash: a03b1fa986bbd03dd786678c57bd8896ec927ab707205d56e0889d9f2dc2be48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427645"
---
# <a name="cim_wifiport-class"></a>Cim \_ WiFiPort (clase)

Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a las especificaciones de la serie IEEE 802.11.

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

La **clase \_ Cim WiFiPort** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim WiFiPort** tiene estas propiedades.

<dl> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")
</dt> </dl>

Ancho de banda máximo admitido, en bits por segundo, según el modo de funcionamiento especificado en la **propiedad PortType.** Por ejemplo, **MaxSpeed** es "11000000" si **PortType** contiene "71" (802,11b).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")
</dt> </dl>

Matriz que contiene las direcciones MAC IEEE 802 EUI-48. La dirección MAC tiene el formato de doce dígitos hexadecimales, y cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")
</dt> </dl>

Dirección MAC IEEE 802 EUI-48 del puerto. La dirección MAC tiene el formato de doce dígitos hexadecimales, y cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")
</dt> </dl>

Modo operativo 802.11 habilitado en el puerto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

**802.11a** (70)


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

**802.11b** (71)


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

**802.11g** (72)


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

**802.11n** (73)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (16000).


</dt> <dd></dd> </dl>

</dd> <dt>

**Velocidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Velocidad")
</dt> </dl>

Velocidad de datos a la que se recibió la unidad de datos del protocolo PPDU (PLCP (Protocolo de convergencia de capas físicas) actual, en bits por segundo. Este valor se codifica en los primeros 4 bits del encabezado PLCP en cada fotograma de PLCP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ NetworkPort**](cim-networkport.md)
</dt> </dl>

 

