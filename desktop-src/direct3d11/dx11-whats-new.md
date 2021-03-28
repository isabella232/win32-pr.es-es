---
title: Novedades del SDK de Windows 7/Direct3D 11 de agosto de 2009
description: Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794818"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Novedades del SDK de Windows 7/Direct3D 11 de agosto de 2009

Esta versión de Windows 7/Direct3D 11 se incluye como parte del SDK de DirectX y contiene nuevas características, herramientas y documentación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D es una API de gráficos 2D y con aceleración de hardware, que ofrece un alto rendimiento y una representación de alta calidad para geometría 2D, mapas de bits y texto. La API de Direct2D está diseñada para interoperar bien con Direct3D y GDI. Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones sencillas, con algunas de las funciones más avanzadas posibles en máquinas correctamente configuradas. <br/> La <a href="/windows/win32/direct2d/direct2d-portal">documentación</a> y los <a href="/previous-versions//dd372354(v=vs.85)">ejemplos</a> de Direct2D están disponibles actualmente en MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite proporciona compatibilidad para la representación de texto de alta calidad, fuentes de esquema independientes de la resolución, compatibilidad con el diseño y texto Unicode completo, y mucho, mucho más:<br/>
<ul>
<li>Sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.<br/></li>
<li>Representación de texto de alta calidad, subpíxel y ClearType que puede usar la tecnología de representación de GDI Direct3D, Direct2D o específica de la aplicación.<br/></li>
<li>Compatibilidad con texto con varios formatos. <br/></li>
<li>Compatibilidad con las características tipográficas avanzadas de las fuentes OpenType.<br/></li>
<li>Compatibilidad con el diseño y la representación de texto en todos los lenguajes compatibles con Windows.<br/></li>
</ul>
Este SDK permite a los desarrolladores evaluar la API y escribir aplicaciones básicas solo con fines de demostración.<br/> La <a href="/windows/win32/directwrite/direct-write-portal">documentación</a> y los <a href="/windows/win32/directwrite/samples">ejemplos</a> de DirectWrite están disponibles actualmente en MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">Dxgi 1,1</a> se basa en dxgi 1,0 y estará disponible en Windows Vista y Windows 7. DXGI 1,1 agrega varias características nuevas:<br/>
<ul>
<li>Compatibilidad con superficies compartidas sincronizadas. Esto permite compartir de forma eficaz la superficie de lectura y escritura entre varios D3D (puede estar entre los dispositivos D3D10 y D3D11).<br/></li>
<li>Compatibilidad con el formato BGRA. Esto permite que GDI se represente en la misma superficie de DXGI de destino de un dispositivo Direct2D, Direct3D 10,1 o Direct3D 11. <br/></li>
<li>Latencia máxima de fotogramas. Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> y <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, los títulos pueden controlar el número de fotogramas que se pueden almacenar en una cola, antes de enviarlos para su representación. La latencia se usa a menudo para controlar el modo en que la CPU elige entre responder a los datos proporcionados por el usuario y a los fotogramas que se encuentran en la cola de representación.<br/></li>
<li>Enumeración de adaptadores. Con <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, titles puede enumerar los adaptadores locales sin monitores ni salidas adjuntos, así como adaptadores con salidas adjuntas.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Ejemplos actualizados<br/></td>
<td>Esta versión tiene varios ejemplos nuevos y actualizados.<br/>
<ul>
<li>El nuevo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> es una ilustración de técnicas de procesamiento de sombreador de cálculo más avanzadas que se pueden ejecutar en una GPU D3D10 o D3D11.</li>
<li>El <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">ejemplo HDRToneMappingCS11</a> se ha expandido para implementar efectos de desenfoque y floración (además de la asignación de tono) mediante el sombreador de cálculo, así como para proporcionar implementaciones del sombreador de píxeles para la comparación.</li>
<li>El <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">ejemplo MultithreadedRendering11</a> se ha actualizado significativamente, con recursos de arte más complejos y un procesamiento por subprocesos más intensivo.</li>
<li>El <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">ejemplo SubD11</a> se ha actualizado con un nuevo modelo facial y el ejemplo ahora aprovecha la característica de cálculo de adyacencias del exportador de contenido de ejemplo.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características introducidas en versiones anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

