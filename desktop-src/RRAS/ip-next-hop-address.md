---
title: IP_NEXT_HOP_ADDRESS estructura (Rtm.h)
description: La estructura IP \_ NEXT HOP ADDRESS contiene la dirección del enrutador del próximo salto para una ruta \_ \_ IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS ras de estructura
- PIP_NEXT_HOP_ADDRESS ras de estructura
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253730"
---
# <a name="ip_next_hop_address-structure"></a>Estructura IP \_ NEXT \_ HOP \_ ADDRESS

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura IP NEXT HOP \_ \_ \_ ADDRESS** contiene la dirección del enrutador del próximo salto para una ruta IP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Especifica la dirección de red IP expresada como una dirección IP en orden de bytes de máquina.

</dd> <dt>

**N \_ Máscaras de red**
</dt> <dd>

Especifica la máscara de red. Aplique esta máscara a la dirección IP para extraer la dirección de red. La máscara de red está en orden de bytes de máquina.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura IP NEXT HOP \_ \_ \_ ADDRESS** es una definición de tipo de la [**estructura IP \_ NETWORK.**](ip-network.md) La definición de tipo está en Rtm.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de Routing Table Manager versión 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RED \_ IP**](ip-network.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





