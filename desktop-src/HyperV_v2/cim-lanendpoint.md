---
description: Un punto de conexión de comunicación que puede conectarse a una LAN para enviar y recibir tramas de datos. Los puntos de conexión LAN incluyen interfaces Ethernet, Token Ring y FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint clase
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
ms.openlocfilehash: 5e42f5edcc7010b9a84fdaaf3686208c9f82def03493c4c423aa3815b1d0758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046815"
---
# <a name="cim_lanendpoint-class"></a>CIM \_ LANEndpoint (clase)

Un punto de conexión de comunicación que puede conectarse a una LAN para enviar y recibir tramas de datos. Los puntos de conexión LAN incluyen interfaces Ethernet, Token Ring y FDDI.

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

La **clase CIM \_ LANEndpoint** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ LANEndpoint** tiene estas propiedades.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión DE LAN.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene las direcciones de multidifusión en las que escucha el punto de conexión de LAN.

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.LANID, CIM \_ LANSegment.LANID")
</dt> </dl>

Etiqueta o identificador del segmento LAN al que está conectado el punto de conexión. Si el punto de conexión no está conectado actualmente o si se desconoce esta información, **LANID** es NULL.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Cim \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.ConnectivityType, CIM \_ LANSegment.LANType")
</dt> </dl>

> [!Note]  
> Descripción en desuso: el tipo de tecnología usada en la LAN.

 

Esta propiedad está desusada. En su lugar, se recomienda usar la **propiedad ProtocolType.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


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

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Dirección de unidifusión principal utilizada por el punto de conexión de LAN.

La dirección MAC debe tener el formato siguiente:

-   La dirección consta de doce dígitos hexadecimales.
-   Cada par de dígitos representa uno de los seis octetos de la dirección MAC.
-   Cada par de dígitos debe estar en orden de bits canónico según RFC 2469.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Tamaño máximo, en bytes, de los campos de datos enviados o recibidos por el punto de conexión de LAN.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Cim \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.OtherTypeDescription", "**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Descripción en desuso: el tipo de tecnología que se usa en la LAN cuando la propiedad **LANType** está establecida en "1" (Otros).

 

Esta propiedad está desusada. En su lugar, se recomienda usar la **propiedad OtherTypeDescription.**

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

[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

