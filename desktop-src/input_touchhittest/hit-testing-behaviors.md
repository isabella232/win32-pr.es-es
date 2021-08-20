---
title: Comportamientos de las pruebas de impacto táctiles
description: Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo las ventanas que se registran a través de la función RegisterTouchHitTestingWindow procesan los mensajes de las pruebas de acceso táctil.
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
ms.openlocfilehash: 0093ff98a255a99606d46db4f6008dbab1dd8688bd789f144e20045b4c714857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884420"
---
# <a name="touch-hit-testing-behaviors"></a>Comportamientos de las pruebas de impacto táctiles

Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo las ventanas que se registran a través de la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) procesan los mensajes de las pruebas de acceso táctil.

| Constante o valor | Descripción |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Indica que los [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) no se envían a la ventana de destino, sino que se envían a ventanas secundarias.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes se envían a la ventana de destino.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Indica que los [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) no se envían a la ventana de destino o a las ventanas secundarias.<br/>              |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Winuser.h |

## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
