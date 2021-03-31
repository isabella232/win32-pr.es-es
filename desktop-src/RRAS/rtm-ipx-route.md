---
title: Estructura de RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ estructura de ruta de IPX RTM contiene información que describe una ruta para la familia del protocolo IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE de la estructura RAS
- PRTM_IPX_ROUTE de puntero de estructura RAS
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
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996167"
---
# <a name="rtm_ipx_route-structure"></a>\_Estructura de ruta IPX de RTM \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ \_ ruta de IPX RTM** contiene información que describe una ruta para la familia del protocolo IPX.

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

**Marca de tiempo de RR \_**
</dt> <dd>

Especifica la hora a la que se creó o se actualizó por última vez la entrada de ruta. Este miembro lo establece el administrador de tablas de enrutamiento. La hora se expresa como una estructura de FILETIME.

</dd> <dt>

**RR \_ RoutingProtocol**
</dt> <dd>

Especifica el protocolo de enrutamiento que ha agregado la ruta.

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

Especifica la interfaz a través de la que se obtuvo la ruta.

</dd> <dt>

**RR \_ ProtocolSpecificData**
</dt> <dd>

Especifica una estructura de [**\_ \_ datos específica del protocolo**](protocol-specific-data.md) que contiene la memoria reservada para los datos específicos de los protocolos de enrutamiento.

</dd> <dt>

**\_Red RR**
</dt> <dd>

Especifica una estructura de [**\_ red IPX**](ipx-network.md) que contiene una dirección de red IP.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Especifica una estructura de [**\_ dirección de próximo \_ salto \_ IPX**](ipx-next-hop-address.md) que contiene la dirección del enrutador de próximo salto.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Especifica una estructura de [**\_ \_ datos específica de IPX**](ipx-specific-data.md) que contiene datos específicos de la familia de protocolos IPX.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de la estructura de **\_ \_ ruta IPX RTM** están alineados con el **valor DWORD** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de la versión 1 del administrador de tablas de enrutamiento \_ \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_red IPX**](ipx-network.md)
</dt> <dt>

[**\_dirección de próximo \_ salto \_ de IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**\_datos específicos de IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





