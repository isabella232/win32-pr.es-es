---
title: RTM_IP_ROUTE estructura (Rtm.h)
description: La estructura RTM \_ IP ROUTE contiene información que describe una ruta propiedad de la familia de \_ protocolos IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE ras de estructura
- PRTM_IP_ROUTE puntero ras de estructura
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd854864dcc61397fa52df7af9419a38ac829a81382be6b6190e4cb3db41d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026735"
---
# <a name="rtm_ip_route-structure"></a>Estructura RTM \_ IP \_ ROUTE

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura RTM \_ IP \_ ROUTE** contiene información que describe una ruta propiedad de la familia de protocolos IP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**RR \_ TimeStamp**
</dt> <dd>

Especifica la hora a la que se creó o actualizó por última vez la entrada de ruta. El administrador de tablas de enrutamiento establece este miembro. La hora se expresa como una estructura FILETIME.

</dd> <dt>

**RR \_ RoutingProtocol**
</dt> <dd>

Especifica el protocolo de enrutamiento que agregó la ruta.

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

Especifica la interfaz a través de la que se obtuvo la ruta.

</dd> <dt>

**RR \_ ProtocolSpecificData**
</dt> <dd>

Especifica una estructura [**DE DATOS ESPECÍFICA DEL \_ \_ PROTOCOLO**](protocol-specific-data.md) que contiene memoria reservada para los datos específicos del protocolo de enrutamiento.

</dd> <dt>

**Red \_ RR**
</dt> <dd>

Especifica una estructura [**DE \_ RED IP**](ip-network.md) que contiene una dirección de red IP.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Especifica una estructura [**IP \_ NEXT HOP \_ \_ ADDRESS**](ip-next-hop-address.md) que contiene la dirección del enrutador del próximo salto.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Especifica una estructura [**DE \_ DATOS \_ ESPECÍFICOS DE**](ip-specific-data.md) IP que contiene datos específicos de la familia de protocolos IP.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de la estructura **\_ RTM IP \_ ROUTE** están alineados **con DWORD.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RED \_ IP**](ip-network.md)
</dt> <dt>

[**DIRECCIÓN IP \_ DEL \_ PRÓXIMO \_ SALTO**](ip-next-hop-address.md)
</dt> <dt>

[**DATOS \_ ESPECÍFICOS DE \_ IP**](ip-specific-data.md)
</dt> </dl>

 

 





