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
# <a name="inkd2drenderer-class"></a><span data-ttu-id="d7926-103">Clase InkD2DRenderer</span><span class="sxs-lookup"><span data-stu-id="d7926-103">InkD2DRenderer class</span></span>

<span data-ttu-id="d7926-104">Implementa la interfaz [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .</span><span class="sxs-lookup"><span data-stu-id="d7926-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="d7926-105">Un objeto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) habilita la representación de trazos de entrada de lápiz en el contexto de dispositivo de Direct2D designado de una aplicación universal de Windows, en lugar del control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d7926-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="d7926-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7926-106">Members</span></span>

<span data-ttu-id="d7926-107">La clase **InkD2DRenderer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7926-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7926-108">**InkD2DRenderer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d7926-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="d7926-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7926-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7926-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7926-110">Methods</span></span>

<span data-ttu-id="d7926-111">La clase **InkD2DRenderer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7926-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="d7926-112">Método</span><span class="sxs-lookup"><span data-stu-id="d7926-112">Method</span></span>                              | <span data-ttu-id="d7926-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7926-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7926-114">**Dibujar**</span><span class="sxs-lookup"><span data-stu-id="d7926-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="d7926-115">Representa el trazo de tinta en el contexto de dispositivo de Direct2D designado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d7926-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="d7926-116">Funciones de acceso de creación \\</span><span class="sxs-lookup"><span data-stu-id="d7926-116">Creation\\Access Functions</span></span>

<span data-ttu-id="d7926-117">Llame a [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkD2DRenderer</strong> para recuperar una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="d7926-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="d7926-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7926-118">Examples</span></span>

<span data-ttu-id="d7926-119">Este fragmento de código del archivo "SceneComposer. cpp" del [ejemplo de entrada de lápiz compleja](/samples/microsoft/windows-universal-samples/complexink/) muestra la representación de una colección de trazos de tinta en un contexto de dispositivo de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d7926-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="d7926-120">Este fragmento de código del archivo "InkRenderer. cpp" del [ejemplo de entrada de lápiz compleja](/samples/microsoft/windows-universal-samples/complexink/) muestra el método Render (llamado en el fragmento de código anterior) que llama al método [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para representar los trazos.</span><span class="sxs-lookup"><span data-stu-id="d7926-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="d7926-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7926-121">Requirements</span></span>

| <span data-ttu-id="d7926-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7926-122">Requirement</span></span> | <span data-ttu-id="d7926-123">Value</span><span class="sxs-lookup"><span data-stu-id="d7926-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7926-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7926-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7926-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7926-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7926-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7926-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7926-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7926-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="d7926-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7926-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7926-129"><dt>Inkrenderer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7926-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7926-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d7926-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7926-131"><dt>Inkrenderer. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7926-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7926-132">IID</span><span class="sxs-lookup"><span data-stu-id="d7926-132">IID</span></span><br/>                      | <span data-ttu-id="d7926-133">IID \_ IInkD2DRenderer se define como 4044e60c-7b01-4671-a97c-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="d7926-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="d7926-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7926-134">Related topics</span></span>

<span data-ttu-id="d7926-135">[Representador de tinta](ink-renderer.md), [interacciones de lápiz y lápiz óptico](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de tinta [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="d7926-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
