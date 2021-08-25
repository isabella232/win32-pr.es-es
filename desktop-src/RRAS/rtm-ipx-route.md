---
title: RTM_IPX_ROUTE estructura (Rtm.h)
description: La estructura \_ RTM IPX \_ ROUTE contiene información que describe una ruta para la familia de protocolos IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE ras de estructura
- PRTM_IPX_ROUTE puntero ras de estructura
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3d14de623fe8d0b3a85118b39d764baa00d2ca5930cfe711be21a91057b6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101835"
---
# <a name="rtm_ipx_route-structure"></a>Estructura \_ RTM IPX \_ ROUTE

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura \_ RTM IPX \_ ROUTE** contiene información que describe una ruta para la familia de protocolos IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
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

Especifica una estructura [**DE DATOS ESPECÍFICA DEL \_ \_ PROTOCOLO**](protocol-specific-data.md) que contiene memoria reservada para los datos específicos de los protocolos de enrutamiento.

</dd> <dt>

**Red \_ RR**
</dt> <dd>

Especifica una estructura [**DE RED IPX \_**](ipx-network.md) que contiene una dirección de red IP.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Especifica una estructura [**IPX \_ NEXT HOP \_ \_ ADDRESS**](ipx-next-hop-address.md) que contiene la dirección del enrutador del próximo salto.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Especifica una estructura [**DE DATOS \_ \_ ESPECÍFICOS de IPX**](ipx-specific-data.md) que contiene datos específicos de la familia de protocolos IPX.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de la estructura **\_ RTM IPX \_ ROUTE** están alineados **con DWORD.**

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

[Estructuras de Routing Table Manager versión \_ 1 \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IPX \_ NETWORK**](ipx-network.md)
</dt> <dt>

[**DIRECCIÓN DEL \_ PRÓXIMO \_ SALTO DE \_ IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**DATOS \_ ESPECÍFICOS DE IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





