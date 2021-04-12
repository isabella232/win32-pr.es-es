---
title: Información general sobre interoperabilidad
description: Resume las diferentes tecnologías que puede usar con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interoperación de GDI
- Direct2D, interoperación GDI+
- Direct2D, interoperabilidad
- Interoperación de Direct2D, DirectWrite
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- interoperabilidad, GDI+
- Interoperabilidad de DirectWrite
- interoperabilidad, DirectWrite
- Windows Imaging Component (WIC)
- WIC (componente de Windows Imaging)
- interoperabilidad, componente de creación de imágenes de Windows (WIC)
- Direct2D, interoperación de WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420887"
---
# <a name="interoperability-overview"></a>Información general sobre interoperabilidad

Una de las características clave de Direct2d es la habilitación de la interoperabilidad entre Direct2D y otras plataformas de representación para que los desarrolladores puedan usar los puntos fuertes específicos de cada plataforma sin tener que estar en peligro eligiendo una plataforma para todas las necesidades. En este tema se resumen las distintas plataformas con las que Direct2D es interoperable. Contiene las siguientes secciones:

-   [Interoperabilidad con GDI](#gdi-interoperability)
-   [Interoperabilidad con GDI+](#gdi-interoperability)
-   [Interoperabilidad de Direct3D](#direct3d-interoperability)
-   [Interoperabilidad de DirectWrite](#directwrite-interoperability)
-   [Interoperabilidad de Windows Imaging Component (WIC)](#windows-imaging-component-wic-interoperability)
-   [Temas relacionados](#related-topics)

En el diagrama siguiente se resumen las distintas plataformas con las que Direct2D es interoperable y se enumeran algunos métodos e interfaces que proporcionan interoperabilidad.

![diagrama de plataformas con el que direct2d interopera, incluidos Direct3D 10,1, directwrite, WIC, GDI+ y GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilidad con GDI

Direct2D habilita la interoperabilidad bidireccional con GDI. Puede usar un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en un [contexto de dispositivo](/windows/desktop/gdi/device-contexts) GDI (DC) o puede usar [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obtener una representación de DC de un destino de representación.

Para obtener más información y ejemplos, vea [información general sobre la interoperabilidad de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>Interoperabilidad con GDI+

Puede usar GDI+ con Direct2D de la misma manera que GDI. Puede usar un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en el mismo DC que el contenido de GDI+. Este enfoque permite empezar a agregar contenido de Direct2D a las aplicaciones que se representan principalmente mediante GDI+.

También puede usar un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para proporcionar acceso a un controlador de dominio de GDI que escribe mediante Direct2D y, a continuación, usar el método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para crear un objeto. Este enfoque es útil para las aplicaciones que se representan principalmente con Direct2D, pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de presentar con GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilidad de Direct3D

Direct2D puede usar un destino de representación de la superficie de DXGI (creado por el método [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) para escribir en un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Esta acción le permite agregar las interfaces y los trabajos en segundo plano a las escenas 3D y usar el contenido de Direct2D como textura para un modelo 3D. Direct2D también puede tomar un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) y usar el método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear una representación de mapa de bits.

Para obtener más información y ejemplos, vea [información general sobre interoperabilidad de Direct2D y Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>Interoperabilidad de DirectWrite

Direct2D se integra estrechamente con DirectWrite. Direct2D facilita el procesamiento de contenido de DirectWrite proporcionando los métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)y [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Interoperabilidad de Windows Imaging Component (WIC)

Direct2D proporciona los métodos [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)y [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular los mapas de bits de WIC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre interoperabilidad de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Introducción a la interoperabilidad de Direct2D y Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 