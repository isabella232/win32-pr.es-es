---
title: Estructura de IPX_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica de IPX \_ contiene datos específicos de IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA de la estructura RAS
- PIPX_SPECIFIC_DATA de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995901"
---
# <a name="ipx_specific_data-structure"></a>\_Estructura de datos específica de IPX \_

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La estructura de **\_ \_ datos específica de IPX** contiene datos específicos de IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas de FSD \_**
</dt> <dd>

Especifica las marcas que describen la ruta. Actualmente, este miembro es cero o el siguiente valor de marca.



| Value                                                                                                                                                                                                      | Significado                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**\_ \_ ruta WAN de cliente global \_ de \_ IPX**</dt> </dl> | Especifica que esta ruta es para la red global asignada a todos los clientes WAN.<br/> |



 

</dd> <dt>

**FSD \_ TickCount**
</dt> <dd>

Especifica el número de pasos que se tarda en llegar a la red de destino. Los protocolos de enrutamiento que no sean RIP deben convertir sus métricas en pasos.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Especifica el recuento de saltos asociado a la ruta.

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

 

 





