---
description: Implementa la interfaz IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: Clase InkD2DRenderer
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
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279761"
---
# <a name="inkd2drenderer-class"></a>Clase InkD2DRenderer

Implementa la interfaz [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .

Un objeto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) habilita la representación de trazos de entrada de lápiz en el contexto de dispositivo de Direct2D designado de una aplicación universal de Windows, en lugar del control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predeterminado.

## <a name="members"></a>Miembros

La clase **InkD2DRenderer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkD2DRenderer** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **InkD2DRenderer** tiene estos métodos.

| Método                              | Descripción                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Representa el trazo de tinta en el contexto de dispositivo de Direct2D designado de la aplicación.<br/> |

## <a name="creationaccess-functions"></a>Funciones de acceso de creación \\

Llame a [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkD2DRenderer</strong> para recuperar una referencia al objeto.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Ejemplos

Este fragmento de código del archivo "SceneComposer. cpp" del [ejemplo de entrada de lápiz compleja](/samples/microsoft/windows-universal-samples/complexink/) muestra la representación de una colección de trazos de tinta en un contexto de dispositivo de Direct2D.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Este fragmento de código del archivo "InkRenderer. cpp" del [ejemplo de entrada de lápiz compleja](/samples/microsoft/windows-universal-samples/complexink/) muestra el método Render (llamado en el fragmento de código anterior) que llama al método [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para representar los trazos.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Inkrenderer. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Inkrenderer. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer se define como 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Temas relacionados

[Representador de tinta](ink-renderer.md), [interacciones de lápiz y lápiz óptico](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de tinta [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)
