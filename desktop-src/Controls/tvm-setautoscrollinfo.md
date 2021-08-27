---
title: TVM_SETAUTOSCROLLINFO mensaje (Commctrl.h)
description: Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la macro \_ SetAutoScrollInfo de TreeView.
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
ms.openlocfilehash: d8840045900fdbd63930219d199889cde018406779426cd767b49ab41a399efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060165"
---
# <a name="tvm_setautoscrollinfo-message"></a>Mensaje \_ SETAUTOSCROLLINFO de TVM

Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetAutoScrollInfo de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Especifica píxeles por segundo. El desplazamiento para desplazarse se divide por *wParam* para determinar la duración total del desplazamiento automático.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Especifica el intervalo de tiempo de volver a dibujar. Vuelva a dibujar en cada intervalo elaspedado, hasta que el elemento se desplace a la vista. Dado *wParam*, se calcula la ubicación del elemento y se vuelve a dibujar. Establezca este valor para crear un desplazamiento suave.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

La información de desplazamiento automático se usa para desplazar un elemento no invisible a la vista. El control debe tener el [**estilo extendido \_ TVS EX \_ AUTOHSCROLL.**](tree-view-control-window-extended-styles.md) Para obtener información sobre los estilos extendidos, vea Tree-View Control de estilos extendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





