---
title: Gráficos de alta fidelidad con DirectX
description: Windows desarrolladores de aplicaciones han usado Microsoft DirectX durante mucho tiempo para proporcionar gráficos 3D y acelerados por hardware de alta calidad.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda45f911293b9d31b9ae28d89c25ed93ce33696
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359978"
---
# <a name="high-fidelity-graphics-with-directx"></a>Gráficos de alta fidelidad con DirectX

Windows desarrolladores de aplicaciones han usado Microsoft DirectX durante mucho tiempo para proporcionar gráficos 3D y acelerados por hardware de alta calidad. Cuando la tecnología se presentó en 1995, los desarrolladores podían proporcionar gráficos 3D de alta calidad para juegos y aplicaciones de ingeniería para jugadores y profesionales dispuestos a pagar más por una placa gráfica 3D. Ahora, incluso los equipos más económico incluyen hardware de gráficos 3D capaz.

Para aprovechar estas funcionalidades de gráficos, Windows Vista introdujo la infraestructura del modelo de controlador de pantalla (WDDM) de Windows para DirectX que permitía a varias aplicaciones y servicios compartir los recursos de la unidad de procesamiento de gráficos (GPU). El Administrador de ventanas de escritorio (DWM) usa esta tecnología para animar el cambio de tareas en 3D, proporcionar imágenes en miniatura dinámicas de ventanas de aplicación y proporcionar Windows efecto de cristal de Aero para aplicaciones de escritorio.

Windows 7 pone aún más funcionalidad gráfica en manos de los desarrolladores de aplicaciones. A través de un nuevo conjunto de DirectXAPI, los desarrolladores de Microsoft Win32 pueden aprovechar las últimas innovaciones de las GPU para agregar imágenes, texto e gráficos 2D, 2D y 3D rápidos, escalables y de alta calidad a sus aplicaciones. En las últimas pantallas *DE LAN,* DirectXAPIs puede mostrar contenido de escritorio y ventana con una profundidad de color superior a 8 bits por componente de color.

Con DirectX, los desarrolladores de Win32 también pueden usar el paralelismo de la GPU para el cálculo de uso general, como el procesamiento de imágenes, y se pueden representar en el hardware de DirectX 10, el hardware de DirectX 9, la CPU o en un equipo Windows remoto. Estas tecnologías se diseñaron para interoperar con Windows Interfaz de dispositivo gráfico (GDI) y Windows GDI+, lo que garantiza que los desarrolladores puedan conservar fácilmente sus inversiones existentes en código Win32. (Consulte las novedades del SDK de DirectX de marzo de [2009).](/previous-versions//bb173043(v=vs.85))

Estas funcionalidades de gráficos mejoradas las proporcionan las siguientes API basadas en *COM:*

-   [Direct2D para](../direct2d/direct2d-portal.md) dibujar gráficos 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para organizar y representar texto.
-   [Windows de creación de imágenes](/windows/desktop/wic/-wic-lh) para procesar y mostrar imágenes.
-   [Direct3D 10 para](/windows/desktop/direct3d10/d3d10-graphics) dibujar gráficos 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para dibujar gráficos 3D y proporcionar acceso a tecnologías de GPU de próxima generación, como teselación, compatibilidad limitada con el streaming de texturas y computación de uso general.
-   [Infraestructura de gráficos de DirectX (DXGI) para](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) administrar dispositivos de visualización locales y remotos y recursos de GPU, y proporcionar interoperabilidad entre DirectX y GDI.

## <a name="direct2d"></a>Direct2D

Basado en Microsoft Direct3D 10, [Direct2D](../direct2d/direct2d-portal.md) ofrece a los desarrolladores de Win32 API en modo inmediato, independientes de la resolución y 2D que usan la potencia del hardware gráfico de próxima generación, pero que interoperan bien con las aplicaciones GDI/GDI+ actuales y las aplicaciones de Direct3D 10. Direct2D proporciona una representación 2D de alta calidad con un rendimiento superior a GDI y GDI+. Proporciona a los desarrolladores de Win32 un control más preciso sobre los recursos y su administración. (Vea [Direct2D).](../direct2d/direct2d-portal.md)

## <a name="directwrite"></a>DirectWrite

Muchas de las aplicaciones actuales necesitan admitir la representación de texto de alta calidad, las fuentes de contorno independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), un nuevo componente de DirectX, proporciona estas características y mucho más:

-   Un sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.
-   Representación de texto *ClearType,* de sub píxeles y de alta calidad que puede usar GDI, [Direct2D](../direct2d/direct2d-portal.md)o tecnología de representación específica de la aplicación.
-   Texto acelerado por hardware, cuando se usa [con Direct2D.](../direct2d/direct2d-portal.md)
-   Compatibilidad con texto de varios formatos.
-   Compatibilidad con las características de tipografía avanzadas de *las fuentes OpenType.*
-   Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.
-   Diseño y representación compatibles con GDI.

El [sistema](/windows/desktop/DirectWrite/direct-write-portal) de fuentes DirectWrite permite el uso de fuentes "cualquier fuente en cualquier lugar", donde los usuarios no tienen que realizar un paso de instalación independiente solo para usar una fuente y una jerarquía estructural mejorada de la agrupación de fuentes para ayudar con la detección manual o mediante programación de fuentes. Las API admiten la medición, el dibujo y las pruebas de acceso del texto de varios formatos. DirectWrite texto en todos los idiomas admitidos para aplicaciones globales y localizadas, a partir de la infraestructura de lenguaje clave que se encuentra en Windows 7. DirectWrite también proporciona API de representación de glifos de bajo nivel para los desarrolladores que desean realizar su propio diseño y el procesamiento de Unicode a glifo. (Vea [DirectWrite](../directwrite/direct-write-portal.md)).

## <a name="windows-imaging-component"></a>Windows Imaging Component

En Windows Vista, [Windows Imaging Component](/windows/desktop/wic/-wic-lh) introdujo un marco extensible para trabajar con imágenes y metadatos de imagen. Los formatos de imagen admitidos por Windows Imaging Component incluyen *JPEG,* *PNG* y *TIFF,* y los formatos de metadatos admitidos incluyen *XMP* *y EXIF.* Con Windows 7, Windows Imaging Component amplía su cumplimiento de estándares al proporcionar compatibilidad con la decodificación progresiva de imágenes, las características *PNG* expandida, los metadatos *GIF* y los metadatos que abarcan segmentos *de APPn.* (Vea [Novedades de WIC en Windows 7).](/previous-versions//ee720061(v=vs.85))

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 amplía la funcionalidad de la canalización de Direct3D 10 y proporciona Windows 7 juegos y aplicaciones 3D de gama alta con acceso eficaz, sólido y escalable a la próxima generación de GPU y CPU de varios núcleos. Además de la funcionalidad que se encuentra en Direct3D 10, Direct3D 11 presenta varias características nuevas.

Ahora, la geometría y las superficies de orden superior se pueden teselar para admitir contenido dinámico y escalable en representaciones de superficie de revisión y de subdivisión.

Para hacer un buen uso de la potencia de procesamiento en paralelo disponible desde varios núcleos de CPU, multithreading aumenta el número de llamadas de representación potenciales por fotograma mediante la distribución de las llamadas de aplicación, tiempo de ejecución y controlador entre varios núcleos. Además, la creación y administración de recursos se ha optimizado para uso multiproceso, lo que permite una administración dinámica de texturas más eficaz para el streaming.

Se han creado nuevos sombreadores de proceso de uso general para Direct3D 11. A diferencia de los sombreadores existentes, se trata de extensiones de la canalización programable que permiten a la aplicación realizar más trabajo completamente en la GPU, independientemente de la CPU. [**DrawAuto,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto)que se introdujo en Direct3D 10, se ha ampliado para interactuar con un sombreador de proceso.

Se han realizado varias mejoras en el lenguaje de sombreado de alto nivel[(HLSL),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)como una forma limitada de vinculación dinámica en sombreadores para mejorar la complejidad de la especialización y construcciones de programación orientadas a objetos como clases e interfaces. (Consulte las novedades del SDK de DirectX de marzo de [2009).](/previous-versions//bb173043(v=vs.85))

## <a name="direct3d-10-improvements"></a>Mejoras de Direct3D 10

Direct3D 10 incluye una canalización de gráficos rediseñada con fases de sombreador programables y objetos de estado inmutables para inicializar las fases de función fija. Los objetos de estado simplifican la canalización y mejoran el rendimiento minimizando el número de cambios de estado necesarios. La programación de las fases del sombreador ahora ofrece extensiones de lenguaje de sombreado de alto nivel para admitir instrucciones de sombreador ilimitadas, recursos de sombreador generalizados y cálculos enteros y bit a bit.

La canalización también presenta la fase del sombreador de geometría, que descarga completamente el trabajo desde la CPU a la GPU. Esta nueva fase le permite crear geometría, transmitir los datos a la memoria y representar la geometría sin interacción con la CPU.

Otras mejoras están diseñadas específicamente para un rendimiento más rápido. La representación predicada realiza la selección de oclusión para reducir la cantidad de geometría que se representa. Las API de creación de instancias pueden reducir drásticamente la cantidad de geometría que se debe transferir a la GPU mediante el dibujo de varias instancias de objetos similares. Las matrices de textura permiten que la GPU realice el intercambio de texturas sin intervención de la CPU.

Se han realizado varias adiciones a Direct3D 10 y Direct3D 11 para ampliar la gama de configuraciones que se pueden usar con estas API. La [Windows Advanced Rasterization Platform (WARP)](/windows/desktop/direct3darticles/directx-warp) implementa una representación rápida y escalable de CPU de varios núcleos para Direct3D 10, lo que permite la representación completa de gráficos en sistemas sin hardware gráfico. La adición de nuevos "niveles de características", específicamente [denominados Direct3D 10 Nivel 9,](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9)permite que las API de Direct3D 10 y Direct3D 11 dirijan hardware de clase 9 de Microsoft Direct3D, ampliando el número de configuraciones que una aplicación Direct3D 10 o Direct3D 11 puede tener como destino casi todos los sistemas informáticos del mercado. (Vea [Gráficos de Direct3D 10).](../direct3d10/d3d10-graphics.md)

## <a name="directxgdi-interoperability"></a>Interoperabilidad de DirectX/GDI

En Windows Vista, el comportamiento de una aplicación que usa DirectX y GDI para representar en una superficie compartida es diferente en función de si DWM está o no. Además, cuando DWM está en, las aplicaciones que usan DirectX y GDI se comportan de forma diferente en Windows Vista que en Windows XP. Esto hizo que muchos ISV deshabilitaran DWM al ejecutar sus aplicaciones en Windows Vista para garantizar un comportamiento coherente. Con las mejoras de DirectX en Windows 7, una aplicación ahora puede combinar libremente DirectX y GDI sin deshabilitar DWM. Windows 7 también ofrece un rendimiento mejorado para escenarios que requieren interoperación entre DirectX y GDI mediante el uso de las API de Direct3D 10 más eficaces. (Vea [Introducción a la interoperación de Direct2D y GDI).](../direct2d/direct2d-and-gdi-interoperation-overview.md)

 

 