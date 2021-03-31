---
title: Constantes de gestos táctiles de Windows (Winuser. h)
description: En esta sección se enumeran las constantes utilizadas para los gestos táctiles de Windows.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996437"
---
# <a name="windows-touch-gestures-constants"></a>Constantes de gestos táctiles de Windows

En esta sección se enumeran las constantes utilizadas para los gestos táctiles de Windows.

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

Define el número máximo de configuraciones de gesto que se pueden incluir en una única llamada a [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) o [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |

## <a name="see-also"></a>Vea también

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [gestos táctiles de Windows](multi-touch-gestures.md)
