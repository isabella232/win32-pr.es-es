---
title: Estructura de IPX_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ estructura de \_ dirección de próximo salto IPX \_ contiene la dirección del enrutador de próximo salto para una ruta IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS de la estructura RAS
- PIPX_NEXT_HOP_ADDRESS de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488950"
---
# <a name="ipx_next_hop_address-structure"></a>\_Estructura de dirección de próximo salto de IPX \_ \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ dirección de próximo \_ salto \_ IPX** contiene la dirección del enrutador de próximo salto para una ruta IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Mac Nha**
</dt> <dd>

Especifica la dirección MAC del enrutador de próximo salto.

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

[**\_ruta IPX de RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





