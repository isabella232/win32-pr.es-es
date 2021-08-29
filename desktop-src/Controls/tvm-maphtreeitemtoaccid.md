---
title: TVM_MAPHTREEITEMTOACCID mensaje (Commctrl.h)
description: Mapas HTREEITEM a un identificador de accesibilidad.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c957f67841d71cfbc3d0737e82774fc0fba4798af7f48a88e018b05ef845704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816305"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>Mensaje \_ MAPHTREEITEMTOACCID de TVM

Mapas **HTREEITEM** a un identificador de accesibilidad.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM que** se asigna a un identificador de accesibilidad.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador de accesibilidad.

## <a name="remarks"></a>Comentarios

Cuando se agrega un elemento a un control de vista de árbol, se devuelve un **identificador HTREEITEM** que identifica de forma única el elemento.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TreeView \_ MapHTREEITEMtoAccID**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





