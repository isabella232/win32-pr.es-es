---
title: Windows Constantes de gestos táctiles (Winuser.h)
description: En esta sección se enumeran las constantes que se usan Windows gestos táctiles.
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: 3e980619a4f0f2a0df83ebfbe2fb8e8a767ef5f988e2bb3b769bde64e714eb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435231"
---
# <a name="windows-touch-gestures-constants"></a>Windows Constantes de gestos táctiles

En esta sección se enumeran las constantes que se usan Windows gestos táctiles.

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

Define el número máximo de configuraciones de gestos que se pueden incluir en una sola llamada a [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) o [**GetGestureConfig.**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig)

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |

## <a name="see-also"></a>Vea también

[**GetGestureConfig,**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig) [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [Windows touch gestures](multi-touch-gestures.md)
