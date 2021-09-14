---
description: La estructura STATIONSTATS proporciona estadísticas sobre una estación específica descrita por la captura actual.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Estructura STATIONSTATS (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245157"
---
# <a name="stationstats-structure"></a>STATIONSTATS (estructura)

La **estructura STATIONSTATS** proporciona estadísticas sobre una estación [*específica*](s.md) descrita por la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NextStationStats**
</dt> <dd>

Índice de la siguiente estación registrada en la matriz **de estructura STATIONSTATS.**

</dd> <dt>

**SessionPartnerList**
</dt> <dd>

Índice de la lista de asociados de estación.

</dd> <dt>

**Marcas**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**StationAddress**
</dt> <dd>

Dirección MAC de la estación.

</dd> <dt>

**Pad**
</dt> <dd>

**Alineación DWORD.**

</dd> <dt>

**TotalPacketsReceived**
</dt> <dd>

Número total de paquetes enviados a la estación.

</dd> <dt>

**TotalDirectedPacketsSent**
</dt> <dd>

Número total de paquetes dirigidos enviados por la estación.

</dd> <dt>

**TotalBroadcastPacketsSent**
</dt> <dd>

Número total de paquetes dirigidos a difusión (dirección MAC FF FF FF FF FF FF) enviados por la estación.

</dd> <dt>

**TotalMulticastPacketsSent**
</dt> <dd>

Número total de paquetes de multidifusión (conjunto de bits de grupo en la dirección de destino) enviados por la estación.

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

Número total de bytes enviados a la estación.

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

Número total de bytes enviados por la estación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Monitor de red almacena la información de la sesión y la estación en dos matrices asociadas. cuyos elementos [son estructuras SESSIONSTATS](sessionstats.md) **y STATIONSTATS** respectivamente. Los miembros de estas estructuras se pueden usar para navegar entre ellas. Por ejemplo, para pasar a la estación siguiente, use **NextStationStats**. Para saltar a la lista de asociados de sesión de la matriz SESSIONSTATS, use el índice proporcionado **en SessionPartnerList**.

> [!Note]  
> La **matriz STATIONSTATS** contiene un elemento para cada estación usada durante la captura actual. El algoritmo Monitor de red utiliza para agregar elementos a esta matriz se basa en la manera más eficaz de registrar información mientras la captura está en curso. Por lo tanto, la siguiente estación no siempre es el siguiente elemento de la matriz.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




