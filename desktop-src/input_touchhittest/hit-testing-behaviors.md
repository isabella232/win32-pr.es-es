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
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569168"
---
# <a name="touch-hit-testing-behaviors"></a>Comportamientos de las pruebas de impacto táctiles

Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo las ventanas que se registran a través de la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) procesan los mensajes de las pruebas de acceso táctil.

| Constante o valor | Descripción |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Indica que los [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) no se envían a la ventana de destino, sino que se envían a ventanas secundarias.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes se envían a la ventana de destino.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Indica que los [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) no se envían a la ventana de destino ni a las ventanas secundarias.<br/>              |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Winuser.h |

## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
