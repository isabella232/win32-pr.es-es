---
title: LVM_INSERTGROUP mensaje (Commctrl.h)
description: Inserta un grupo en un control de vista de lista.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019253"
---
# <a name="lvm_insertgroup-message"></a>Mensaje \_ INSERTGROUP de LVM

Inserta un grupo en un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Índice donde se va a agregar el grupo. Si es -1, el grupo se agrega al final de la lista.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**estructura LVGROUP**</a> que contiene el grupo que se agregará.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento al que se agregó el grupo o -1 si se ha fallado la operación.

## <a name="remarks"></a>Comentarios

Para activar el modo de grupo, llame a [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Un grupo no se puede insertar en un control de vista de lista vacío.

Asegúrese de establecer **iGroupId** en los elementos a los que se agregó el grupo. De lo contrario, después del procesamiento de [**mensajes \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) de LVM **con TRUE,** el control listview no mostrará ningún elemento.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32 versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





