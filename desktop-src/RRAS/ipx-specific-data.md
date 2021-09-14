---
title: IPX_SPECIFIC_DATA estructura (Rtm.h)
description: La estructura DE DATOS ESPECÍFICOS de IPX \_ \_ contiene datos específicos de IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA ras de estructura
- PIPX_SPECIFIC_DATA ras de puntero de estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073883"
---
# <a name="ipx_specific_data-structure"></a>Estructura DE DATOS \_ ESPECÍFICOS de IPX \_

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **estructura DE DATOS \_ \_ ESPECÍFICOS de IPX** contiene datos específicos de IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Marcas \_ FSD**
</dt> <dd>

Especifica marcas que describen la ruta. Actualmente, este miembro es cero o el siguiente valor de marca.



| Value                                                                                                                                                                                                      | Significado                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**RUTA WAN \_ DE CLIENTE GLOBAL \_ \_ DE \_ IPX**</dt> </dl> | Especifica que esta ruta es para la red global asignada para todos los clientes WAN.<br/> |



 

</dd> <dt>

**TickCount de FSD \_**
</dt> <dd>

Especifica el número de pasos que se necesitan para llegar a la red de destino. Los protocolos de enrutamiento distintos de RIP deben convertir sus métricas en tics.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Especifica el número de saltos asociado a la ruta.

</dd> </dl>

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

[Estructuras de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

 





