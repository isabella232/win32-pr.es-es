---
title: Comportamientos de la prueba de posicionamiento táctil
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los mensajes para las pruebas de posicionamiento táctil mediante Windows que se registran a través de la función RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720228"
---
# <a name="touch-hit-testing-behaviors"></a>Comportamientos de la prueba de posicionamiento táctil

Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los mensajes para las pruebas de posicionamiento táctil mediante Windows que se registran a través de la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

| Constante o valor | Descripción |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0X0) | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes no se envían a la ventana de destino, sino que se envían a las ventanas secundarias.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indica que se envían [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes a la ventana de destino.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0X2)          | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes no se envían a la ventana de destino o a las ventanas secundarias.<br/>              |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Winuser. h |

## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
