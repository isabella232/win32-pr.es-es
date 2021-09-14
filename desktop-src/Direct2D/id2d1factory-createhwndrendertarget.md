---
title: Métodos ID2D1Factory CreateHwndRenderTarget (D2d1.h)
description: Crea un ID2D1HwndRenderTarget, un destino de representación que se representa en una ventana.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Métodos CreateHwndRenderTarget de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163018"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>Métodos ID2D1Factory::CreateHwndRenderTarget

Crea un [**id2D1HwndRenderTarget,**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))un destino de representación que se representa en una ventana.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                                                                              | Descripción                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**CreateHwndRenderTarget(D2D1 \_ RENDER TARGET PROPERTIES \_ \_ \* ,D2D1 \_ HWND RENDER TARGET PROPERTIES \_ \_ \_ \* ,ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Crea un [**id2D1HwndRenderTarget,**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))un destino de representación que se representa en una ventana.<br/> |
| [**CreateHwndRenderTarget(D2D1 \_ RENDER TARGET PROPERTIES \_ \_&,D2D1 \_ HWND RENDER TARGET PROPERTIES \_ \_ \_&,ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Crea un [**id2D1HwndRenderTarget,**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))un destino de representación que se representa en una ventana.<br/> |



## <a name="remarks"></a>Observaciones

Cuando se crea un destino de representación y la aceleración de hardware está disponible, se asignan recursos en la GPU del equipo. Al crear un destino de representación una vez y conservarlo siempre que sea posible, se obtienen ventajas de rendimiento. La aplicación debe crear destinos de representación una vez y retenerlos durante la vida útil de la aplicación o hasta que se reciba el error [**D2DERR \_ RECREATE \_ TARGET.**](direct2d-error-codes.md) Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que creó).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea [**un id2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
