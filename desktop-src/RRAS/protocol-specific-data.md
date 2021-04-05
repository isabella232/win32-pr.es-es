---
title: Estructura de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica del protocolo \_ contiene memoria reservada para los datos específicos de un protocolo de enrutamiento determinado.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA de la estructura RAS
- PPROTOCOL_SPECIFIC_DATA de puntero de estructura RAS
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
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802792"
---
# <a name="protocol_specific_data-structure"></a>\_Estructura de datos específica del protocolo \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ \_ datos específica del protocolo** contiene memoria reservada para los datos específicos de un protocolo de enrutamiento determinado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Datos PSD**
</dt> <dd>

Especifica una matriz de variables **DWORD** . Esta memoria está reservada para los datos específicos de los protocolos de enrutamiento.

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
</dt> <dt>

[**\_ruta IPX de RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





