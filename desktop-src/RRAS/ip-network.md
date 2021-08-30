---
title: IP_NETWORK estructura (Rtm.h)
description: La estructura \_ IP NETWORK describe una dirección de red IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK ras de estructura
- PIP_NETWORK puntero de estructura RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5976211d0aea5936278353a9fb1b172585c0ee63531dde229ef4bf561c5dbb4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029965"
---
# <a name="ip_network-structure"></a>Estructura \_ DE RED IP

\[Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura \_ IP NETWORK** describe una dirección de red IP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a>Miembros

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Especifica el número de red IP expresado como una dirección IP en orden de bytes de máquina.

</dd> <dt>

**N \_ NetMask**
</dt> <dd>

Especifica la máscara de red. Aplique esta máscara a la dirección IP para extraer la dirección de red. La máscara de red está en orden de bytes de máquina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de Routing Table Manager versión 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





