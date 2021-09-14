---
title: TVM_SETAUTOSCROLLINFO mensaje (Commctrl.h)
description: Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetAutoScrollInfo.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165666"
---
# <a name="tvm_setautoscrollinfo-message"></a>Mensaje \_ SETAUTOSCROLLINFO de TVM

Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetAutoScrollInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Especifica píxeles por segundo. El desplazamiento que se va a desplazar se divide por *wParam* para determinar la duración total del desplazamiento automático.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Especifica el intervalo de tiempo de volver a dibujar. Vuelva a dibujar en cada intervalo elaspedado, hasta que el elemento se desplace a la vista. Dado *wParam*, se calcula la ubicación del elemento y se vuelve a dibujar. Establezca este valor para crear un desplazamiento sin problemas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

La información de desplazamiento automático se usa para desplazar un elemento novisible a la vista. El control debe tener el [**estilo extendido \_ TVS EX \_ AUTOHSCROLL.**](tree-view-control-window-extended-styles.md) Para obtener información sobre los estilos extendidos, vea Tree-View Control de estilos extendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





