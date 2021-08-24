---
title: PROTOCOL_SPECIFIC_DATA estructura (Rtm.h)
description: La estructura DATOS ESPECÍFICOS DEL PROTOCOLO \_ contiene memoria reservada para datos \_ específicos de un protocolo de enrutamiento determinado.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA ras de estructura
- PPROTOCOL_SPECIFIC_DATA de estructura ras
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe43e17827a4c6308c7bfd4499de60ec9105a9fa525ab5aad0226887d02ae8e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036465"
---
# <a name="protocol_specific_data-structure"></a>Estructura \_ DE DATOS \_ ESPECÍFICOS DEL PROTOCOLO

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura \_ DATOS \_ ESPECÍFICOS DEL** PROTOCOLO contiene memoria reservada para datos específicos de un protocolo de enrutamiento determinado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Datos \_ de PSD**
</dt> <dd>

Especifica una matriz de variables **DWORD.** Esta memoria está reservada para los datos específicos de los protocolos de enrutamiento.

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

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estructuras de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

 





