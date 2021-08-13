---
title: Información general sobre interoperabilidad
description: Resume las distintas tecnologías que puede usar con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Interoperación de Direct2D,GDI
- Direct2D, GDI+ interoperación
- Direct2D, interoperabilidad
- Direct2D, DirectWrite interoperación
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- interoperabilidad, GDI+
- DirectWrite interoperabilidad
- interoperabilidad, DirectWrite
- Windows Imaging Component (WIC)
- WIC (Windows imaging component)
- interoperabilidad,Windows imaging component (WIC)
- Interoperación de Direct2D,WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385334"
---
# <a name="interoperability-overview"></a>Información general sobre interoperabilidad

Una de las características clave de Direct2D es habilitar la interoperabilidad entre Direct2D y otras plataformas de representación para que los desarrolladores puedan usar los puntos fuertes específicos de cada plataforma sin verse obligados a poner en peligro al elegir una plataforma para todas las necesidades. En este tema se resumen las distintas plataformas con las que Direct2D es interoperable. Contiene las siguientes secciones:

-   [Interoperabilidad de GDI](#gdi-interoperability)
-   [GDI+ Interoperabilidad](#gdi-interoperability)
-   [Interoperabilidad de Direct3D](#direct3d-interoperability)
-   [DirectWrite Interoperabilidad](#directwrite-interoperability)
-   [Windows Interoperabilidad del componente de creación de imágenes (WIC)](#windows-imaging-component-wic-interoperability)
-   [Temas relacionados](#related-topics)

En el diagrama siguiente se resumen las distintas plataformas con las que Direct2D es interoperable y se enumeran algunos métodos e interfaces que proporcionan interoperabilidad.

![diagrama de plataformas con las que direct2d interopera, incluidos direct3d 10.1, directwrite, wic, gdi+ y gdi](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilidad de GDI

Direct2D permite la interoperabilidad en dos sentidos con GDI. Puede usar un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en un contexto de dispositivo [GDI](/windows/desktop/gdi/device-contexts) (DC), o puede usar [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obtener una representación de controlador de dominio de un destino de representación.

Para obtener más información y ejemplos, vea Introducción a la interoperabilidad de [Direct2D y GDI.](direct2d-and-gdi-interoperation-overview.md)

## <a name="gdi-interoperability"></a>GDI+ Interoperabilidad

Puede usar GDI+ con Direct2D de la misma manera que GDI. Puede usar [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en el mismo controlador de dominio que GDI+ contenido. Este enfoque le permite empezar a agregar contenido de Direct2D a las aplicaciones que se representan principalmente mediante GDI+.

También puede usar [**un id2D1GdiInteropRenderTarget para**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) proporcionar acceso a un controlador de dominio de GDI que escribe mediante Direct2D y, a continuación, usar el método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para crear un objeto. Este enfoque es útil para las aplicaciones que se representan principalmente con Direct2D, pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de representar con GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilidad de Direct3D

Direct2D puede usar un destino de representación de superficie DXGI (creado por el [**método CreateDxgiSurfaceRender)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para escribir en [un IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Esta acción le permite agregar fondos 2D e interfaces a escenas 3D y usar contenido de Direct2D como textura para un modelo 3D. Direct2D también puede tomar [un IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) y usar el [**método CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear una representación de mapa de bits.

Para obtener más información y ejemplos, vea Introducción a la interoperabilidad de [Direct2D y Direct3D.](direct2d-and-direct3d-interoperation-overview.md)

## <a name="directwrite-interoperability"></a>DirectWrite Interoperabilidad

Direct2D está estrechamente integrado con DirectWrite. Direct2D facilita la representación del contenido DirectWrite proporcionando los métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)y [**DrawGlyphRun.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

## <a name="windows-imaging-component-wic-interoperability"></a>Windows Interoperabilidad del componente de creación de imágenes (WIC)

Direct2D proporciona los [**métodos CreateBitmapFromWicBitmap,**](id2d1rendertarget-createbitmapfromwicbitmap.md) [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)y [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular mapas de bits de WIC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la interoperabilidad de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Introducción a la interoperabilidad de Direct2D y Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 