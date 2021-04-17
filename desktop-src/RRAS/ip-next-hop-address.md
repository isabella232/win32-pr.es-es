---
title: Estructura de IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ estructura de \_ dirección de próximo salto IP \_ contiene la dirección del enrutador de próximo salto para una ruta IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS de la estructura RAS
- PIP_NEXT_HOP_ADDRESS de la estructura RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651409"
---
# <a name="ip_next_hop_address-structure"></a>\_Estructura de dirección de próximo \_ salto IP \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ dirección de próximo \_ salto \_ IP** contiene la dirección del enrutador de próximo salto para una ruta IP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Especifica la dirección de red IP expresada como una dirección IP en orden de bytes de la máquina.

</dd> <dt>

**\_Máscara de máscara**
</dt> <dd>

Especifica la máscara de red. Aplique esta máscara a la dirección IP para extraer la dirección de red. La máscara de red está en orden de bytes de la máquina.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ dirección de próximo \_ salto \_ IP** es una definición de tipo de la estructura de [**\_ red IP**](ip-network.md) . La definición de tipo está en RTM. h.

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

[**\_red IP**](ip-network.md)
</dt> <dt>

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> </dl>

 

 





