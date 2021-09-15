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
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247442"
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
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |

## <a name="see-also"></a>Vea también

[**GetGestureConfig,**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig) [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [Windows touch gestures](multi-touch-gestures.md)
