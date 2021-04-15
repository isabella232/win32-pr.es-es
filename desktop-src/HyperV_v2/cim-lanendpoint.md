---
description: Un punto de conexión de comunicación que se puede conectar a una LAN para enviar y recibir tramas de datos. Los puntos de conexión de LAN incluyen Ethernet, token ring e interfaces FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670038"
---
# <a name="cim_lanendpoint-class"></a>\_Clase LANEndpoint de CIM

Un punto de conexión de comunicación que se puede conectar a una LAN para enviar y recibir tramas de datos. Los puntos de conexión de LAN incluyen Ethernet, token ring e interfaces FDDI.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ LANEndpoint** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ LANEndpoint** tiene estas propiedades.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión de LAN.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene las direcciones de multidifusión a las que el punto de conexión LAN realiza escuchas.

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LANID, CIM \_ LANSegment. LANID")
</dt> </dl>

Etiqueta o identificador del segmento de LAN al que está conectado el extremo. Si el extremo no está conectado actualmente o si no se conoce esta información, **LANID** es NULL.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el [**\_ ProtocolEndpoint de CIM**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")
</dt> </dl>

> [!Note]  
> Descripción en desuso: el tipo de tecnología que se usa en la LAN.

 

Esta propiedad está desusada. En su lugar, se recomienda usar la propiedad **protocolType** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Mac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Dirección de unidifusión principal usada por el extremo de LAN.

La dirección MAC se debe formatear con las siguientes características:

-   La dirección consta de doce dígitos hexadecimales.
-   Cada par de dígitos representa uno de los seis octetos de la dirección MAC.
-   Cada par de dígitos debe estar en orden de bits canónico según RFC 2469.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Tamaño máximo, en bytes, de los campos de datos enviados o recibidos por el punto de conexión de LAN.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el [**\_ ProtocolEndpoint de CIM**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Descripción en desuso: el tipo de tecnología que se usa en la LAN cuando la propiedad **LANType** se establece en "1" (otro).

 

Esta propiedad está desusada. En su lugar, se recomienda usar la propiedad **OtherTypeDescription** .

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

[**ProtocolEndpoint de CIM \_**](cim-protocolendpoint.md)
</dt> </dl>

 

