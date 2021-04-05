---
title: Cómo recortar con un objeto de recorte de rectángulo
description: En este tema se muestra cómo usar un objeto de clip de rectángulo para recortar un árbol visual o visual.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078582"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Cómo recortar con un objeto de recorte de rectángulo

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se muestra cómo usar un objeto de clip de rectángulo para recortar un árbol visual o visual.

En el ejemplo de este tema se define un clip rectangular que se centra en la ubicación del mouse y se aplica el clip a un visual que está centrado en el área cliente de la ventana de destino de la composición. En esta captura de pantalla se muestra el resultado de aplicar el objeto de clip de rectángulo al objeto visual.

![resultado de aplicar un objeto de clip de rectángulo a un objeto visual](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [DirectComposition](directcomposition-portal.md)
-   [Gráficos de Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Infraestructura de gráficos de DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Microsoft Win32
-   Modelo de objetos componentes (COM)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-initialize-directcomposition-objects"></a>Paso 1: inicializar objetos DirectComposition

1.  Cree el objeto de dispositivo y el objeto de destino de composición.
2.  Cree un visual, establezca su contenido y agréguelo al árbol visual.

Para obtener más información, vea [cómo inicializar DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-rectangle-clip-object"></a>Paso 2: crear el objeto de clip de rectángulo

Use el método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) para crear una instancia del objeto de clip de rectángulo.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Paso 3: establecer las propiedades del objeto de clip de rectángulo

Llame a los métodos de la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) del objeto de clip de rectángulo para establecer las propiedades del rectángulo de recorte.

En el ejemplo siguiente se define un rectángulo de recorte que está centrado alrededor de la ubicación actual del mouse. Las `m_offsetX` `m_offsetY` variables de miembro y contienen los valores de las propiedades OffsetX y OffsetY del elemento visual.


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



Tenga en cuenta que la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) incluye los siguientes métodos para definir un rectángulo de recorte con esquinas redondeadas:

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Paso 4: establecer la propiedad clip del visual

Use el método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para asociar la propiedad clip del objeto visual con el objeto de clip de rectángulo.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Paso 5: confirmar la composición

Llame al método [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar el lote de comandos en Microsoft DirectComposition para su procesamiento. El resultado de aplicar el rectángulo de recorte aparece en la ventana de destino.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Paso 6: liberación de los objetos DirectComposition

Asegúrese de liberar el objeto de clip de rectángulo cuando ya no lo necesite, así como el objeto de dispositivo, el objeto de destino de composición y los objetos visuales. En el ejemplo siguiente se llama a la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida por la aplicación para liberar los objetos DirectComposition.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recorte](clipping.md)
</dt> </dl>

 

 