---
title: LVM_GETVIEW mensaje (Commctrl.h)
description: Recupera la vista actual de un control list-view.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431b0a7b3fba9a45370c372347285489a56082c4a04396c273a45c4da41b05b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915515"
---
# <a name="lvm_getview-message"></a>Mensaje \_ GETVIEW de LVM

Recupera la vista actual de un control list-view.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **DWORD** que especifica la vista actual.

## <a name="remarks"></a>Comentarios

A continuación se encuentran los valores de las vistas.

-   DETALLES \_ DE LA VISTA DE LV \_
-   ICONO \_ DE VISTA DE \_ LV
-   LISTA \_ DE VISTAS DE \_ LV
-   LV \_ VIEW \_ SMALLICON
-   ICONO \_ DE VISTA DE \_ LV

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





