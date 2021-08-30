---
title: IPX_NETWORK estructura (Rtm.h)
description: La estructura IPX \_ NETWORK describe una dirección de red IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- IPX_NETWORK estructura RAS
- PIPX_NETWORK puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e667dd21176d88070cdf775fc9b38ca601e59dd542f6237beaffe2711b1ee5ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074165"
---
# <a name="ipx_network-structure"></a>Estructura NETWORK de IPX \_

\[Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura IPX \_ NETWORK** describe una dirección de red IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a>Miembros

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Contiene el número de red IPX en orden de bytes de máquina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

 





