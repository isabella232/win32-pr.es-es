---
description: Implementa la interfaz IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: InkD2DRenderer (clase)
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726735"
---
# <a name="inkd2drenderer-class"></a>InkD2DRenderer (clase)

Implementa la [**interfaz IInkD2DRenderer.**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)

Un [**objeto IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permite la representación de trazos de lápiz en el contexto de dispositivo Direct2D designado de una aplicación universal Windows, en lugar del control [**InkCanvas predeterminado.**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)

## <a name="members"></a>Miembros

La **clase InkD2DRenderer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkD2DRenderer** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase InkD2DRenderer** tiene estos métodos.

| Método                              | Descripción                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Representa el trazo de entrada de lápiz en el contexto de dispositivo Direct2D designado de la aplicación.<br/> |

## <a name="creationaccess-functions"></a>Creación de \\ funciones de acceso

Llame [<strong>a CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkD2DRenderer</strong> para recuperar una referencia al objeto .

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Ejemplos

Este fragmento de código del archivo "SceneComposer.cpp" del ejemplo de entrada manuscrita compleja muestra la representación de una colección de trazos de entrada de lápiz en un contexto de dispositivo Direct2D. [](/samples/microsoft/windows-universal-samples/complexink/)

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Este fragmento de código del archivo "InkRenderer.cpp" del ejemplo de entrada manuscrita compleja muestra el método Render (llamado en el fragmento de código anterior) que llama al método [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para representar los trazos. [](/samples/microsoft/windows-universal-samples/complexink/)

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Inkrenderer.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Inkrenderer.idl</dt> </dl> |
| IID<br/>                      | IID IInkD2DRenderer se define como \_ 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Temas relacionados

[Representador de entrada](ink-renderer.md)de lápiz, [interacciones de lápiz y](/windows/uwp/design/input/pen-and-stylus-interactions)lápiz, ejemplo de análisis de entrada de lápiz, ejemplo de entrada manuscrita [simple,](/samples/microsoft/windows-universal-samples/simpleink/) [ejemplo de entrada manuscrita compleja](/samples/microsoft/windows-universal-samples/complexink/) [](/samples/microsoft/windows-universal-samples/inkanalysis/)
