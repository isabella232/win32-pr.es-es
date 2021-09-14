---
title: Novedades del SDK de agosto de 2009 Windows 7/Direct3D 11
description: Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6955d00cb9a2b5b59bf89e59a809a1b93f6fc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060837"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Novedades del SDK de agosto de 2009 Windows 7/Direct3D 11

Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.




| Elemento | Descripción | 
|------|-------------|
| <span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br /> | Direct2D es una API de gráficos 2D acelerada por hardware, en modo inmediato que proporciona un alto rendimiento y una representación de alta calidad para geometría 2D, mapas de bits y texto. La API de Direct2D está diseñada para interoperar bien con Direct3D y GDI. Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones sencillas, con algunas de las funcionalidades más avanzadas posibles en máquinas configuradas correctamente. <br /><a href="/windows/win32/direct2d/direct2d-portal">La</a> documentación <a href="/previous-versions//dd372354(v=vs.85)">y los</a> ejemplos de Direct2D están disponibles actualmente en MSDN.<br /> | 
| <span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br /> | DirectWrite compatibilidad con la representación de texto de alta calidad, fuentes de esquema independientes de la resolución, compatibilidad con texto Unicode completo y diseño, y mucho más:<br /><ul><li>Un sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.<br /></li><li>Representación de texto ClearType de sub píxeles de alta calidad que puede usar GDI Direct3D, Direct2D o tecnología de representación específica de la aplicación.<br /></li><li>Compatibilidad con texto de varios formatos. <br /></li><li>Compatibilidad con las características de tipografía avanzadas de las fuentes OpenType.<br /></li><li>Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos por Windows.<br /></li></ul>Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones básicas solo con fines de demostración.<br /><a href="/windows/win32/directwrite/direct-write-portal">La</a> documentación <a href="/windows/win32/directwrite/samples">y los</a> ejemplos DirectWrite están disponibles actualmente en MSDN.<br /> | 
| <span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1<br /> | <a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> se basa en DXGI 1.0 y estará disponible en Windows Vista y Windows 7. DXGI 1.1 agrega varias características nuevas:<br /><ul><li>Compatibilidad con superficies compartidas sincronizadas. Esto permite un uso compartido eficaz de la superficie de lectura y escritura entre varios dispositivos D3D (podría estar entre D3D10 y D3D11).<br /></li><li>Compatibilidad con el formato BGRA. Esto permite que GDI se represente en la misma superficie DXGI destinada a un dispositivo Direct2D, Direct3D 10.1 o Direct3D 11. <br /></li><li>Latencia máxima de fotogramas. Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency,</strong></a>los títulos pueden controlar el número de fotogramas que se pueden almacenar en una cola, antes del envío para su representación. La latencia se suele usar para controlar cómo la CPU elige entre responder a la entrada del usuario y los fotogramas que están en la cola de representación.<br /></li><li>Enumeración del adaptador. Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, los títulos pueden enumerar adaptadores locales sin monitores o salidas asociados, así como adaptadores con salidas asociadas.<br /></li></ul> | 
| <span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Ejemplos actualizados<br /> | Esta versión tiene varios ejemplos nuevos y actualizados.<br /><ul><li>La nueva <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> es una ilustración de técnicas de procesamiento de sombreador de proceso más avanzadas que se pueden ejecutar en una GPU D3D10 o D3D11.</li><li>El <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">ejemplo HDRToneMappingCS11</a> se ha ampliado para implementar efectos de desenfoque y desenfoque (además de la asignación de tono) mediante el sombreador de proceso, así como para proporcionar implementaciones de sombreador de píxeles para la comparación.</li><li>El <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">ejemplo MultithreadedRendering11</a> se ha actualizado significativamente, con recursos de arte más complejos y un procesamiento por subproceso más intensivo.</li><li>El <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">ejemplo SubD11</a> se ha actualizado con un nuevo modelo facial y ahora aprovecha la característica de cálculo de adyacencia del exportador de contenido de ejemplos.</li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características introducidas en versiones anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

