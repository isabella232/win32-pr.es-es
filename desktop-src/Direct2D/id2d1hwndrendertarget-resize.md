---
title: Métodos de cambio de tamaño ID2D1HwndRenderTarget (D2d1.h)
description: Cambia el tamaño del destino de representación al tamaño de píxel especificado.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Cambiar el tamaño de los métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162934"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>Métodos ID2D1HwndRenderTarget::Resize

Cambia el tamaño del destino de representación al tamaño de píxel especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                         | Descripción                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Resize(D2D1 \_ SIZE \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Cambia el tamaño del destino de representación al tamaño de píxel especificado. <br/> |
| [**Resize(D2D1 \_ SIZE \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Cambia el tamaño del destino de representación al tamaño de píxel especificado.<br/>  |



## <a name="remarks"></a>Observaciones

Después de llamar a este método, no se define el contenido del búfer de reserva del destino de representación, incluso si se especificó la opción [**D2D1 \_ PRESENT OPTIONS RETAIN \_ \_ \_ CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) cuando se creó el destino de representación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
