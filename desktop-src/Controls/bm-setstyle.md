---
title: Mensaje de BM_SETSTYLE (Winuser. h)
description: Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar el botón \_ setStyle macro.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996115"
---
# <a name="bm_setstyle-message"></a>\_Mensaje SETSTYLE de BM

Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar el [**botón \_ setStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estilo de botón. Este parámetro puede ser una combinación de estilos de botón. Para obtener una tabla de estilos de botón, consulte [estilos de botón](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* es un **booleano** que especifica si se debe volver a dibujar el botón. Un valor de **true** vuelve a dibujar el botón; un valor **false** no vuelve a dibujar el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

