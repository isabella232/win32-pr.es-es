---
title: ID2D1HwndRenderTarget cambiar el tamaño de los métodos (D2d1. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660915"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>ID2D1HwndRenderTarget:: Resize (métodos)

Cambia el tamaño del destino de representación al tamaño de píxel especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                         | Descripción                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Cambiar tamaño (D2D1 \_ tamaño \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Cambia el tamaño del destino de representación al tamaño de píxel especificado. <br/> |
| [**Cambiar tamaño (D2D1 \_ tamaño \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Cambia el tamaño del destino de representación al tamaño de píxel especificado.<br/>  |



## <a name="remarks"></a>Observaciones

Una vez que se llama a este método, no se define el contenido del búfer de reserva del destino de representación, aunque se haya especificado la opción de [**\_ \_ \_ conservación \_ de las opciones presentes de D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) cuando se creó el destino de representación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
