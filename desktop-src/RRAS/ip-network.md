---
title: Estructura de IP_NETWORK (RTM. h)
description: La \_ estructura de red IP describe una dirección de red IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK de la estructura RAS
- PIP_NETWORK de puntero de estructura RAS
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
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803008"
---
# <a name="ip_network-structure"></a>\_Estructura de red IP

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ red IP** describe una dirección de red IP.

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

Especifica el número de red IP expresado como una dirección IP en orden de bytes de la máquina.

</dd> <dt>

**\_Máscara de máscara**
</dt> <dd>

Especifica la máscara de red. Aplique esta máscara a la dirección IP para extraer la dirección de red. La máscara de red está en orden de bytes de la máquina.

</dd> </dl>

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

[Estructuras de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> </dl>

 

 





