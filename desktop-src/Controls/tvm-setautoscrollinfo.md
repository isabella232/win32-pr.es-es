---
title: Mensaje de TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la \_ macro SetAutoScrollInfo de TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656515"
---
# <a name="tvm_setautoscrollinfo-message"></a>\_Mensaje de SETAUTOSCROLLINFO TVM

Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetAutoScrollInfo de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Especifica los píxeles por segundo. El desplazamiento que se va a desplazar se divide por el *wParam* para determinar la duración total del desplazamiento automático.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Especifica el intervalo de tiempo de redibujo. Vuelva a dibujar en cada intervalo de ELASPED hasta que el elemento se desplace en la vista. Dado *wParam*, se calcula la ubicación del elemento y se produce un Repaint. Establezca este valor en crear desplazamiento suave.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="remarks"></a>Observaciones

La información de desplazamiento automático se utiliza para desplazarse por un elemento no visible en la vista. El control debe tener el estilo extendido [**TV \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) . Para obtener información sobre los estilos extendidos, vea Tree-View control Extended Styles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





