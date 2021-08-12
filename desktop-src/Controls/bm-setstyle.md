---
title: BM_SETSTYLE mensaje (Winuser.h)
description: Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar la \_ macro Button SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE controles de Windows mensaje
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
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674423"
---
# <a name="bm_setstyle-message"></a>Mensaje \_ DE BM SETSTYLE

Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button SetStyle.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estilo del botón. Este parámetro puede ser una combinación de estilos de botón. Para obtener una tabla de estilos de botón, vea [Estilos de botón](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* es **un BOOL** que especifica si el botón se va a volver a dibujar. Un valor **true vuelve** a dibujar el botón; Un valor **false no** vuelve a dibujar el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

