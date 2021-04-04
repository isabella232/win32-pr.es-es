---
title: Gráficos de alta fidelidad con DirectX
description: Los desarrolladores de aplicaciones de Windows han utilizado Microsoft DirectX para ofrecer gráficos 3D de alta calidad y con aceleración de hardware.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda45f911293b9d31b9ae28d89c25ed93ce33696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793545"
---
# <a name="high-fidelity-graphics-with-directx"></a>Gráficos de alta fidelidad con DirectX

Los desarrolladores de aplicaciones de Windows han utilizado Microsoft DirectX para ofrecer gráficos 3D de alta calidad y con aceleración de hardware. Cuando la tecnología se incorporó en 1995, los desarrolladores podían ofrecer gráficos 3D de alta calidad para juegos y aplicaciones de ingeniería para jugadores y profesionales dispuestos a pagar extra por una placa de gráficos 3D. Ahora, incluso los equipos más económicos incluyen hardware compatible con gráficos 3D.

Para aprovechar estas capacidades de gráficos, Windows Vista presentó la infraestructura del modelo de controladores de pantalla (WDDM) de Windows para DirectX que permitió que varias aplicaciones y servicios compartan los recursos de la unidad de procesamiento de gráficos (GPU). El Administrador de ventanas de escritorio (DWM) utiliza esta tecnología para animar el cambio de tareas en 3D, proporcionar imágenes en miniatura dinámicas de las ventanas de la aplicación y proporcionar efectos de cristal de Windows Aero para aplicaciones de escritorio.

Windows 7 ofrece aún más capacidad de gráficos a las manos de los desarrolladores de aplicaciones. A través de un nuevo conjunto de DirectXAPIs, los desarrolladores de Microsoft Win32 pueden aprovechar las últimas innovaciones en GPU para agregar gráficos, texto e imágenes rápidos, escalables y de alta calidad a sus aplicaciones. En las pantallas *LCD* más recientes, DirectXAPIs puede mostrar el contenido de la ventana y el escritorio con una profundidad de color superior a 8 bits por componente de color.

Con DirectX, los desarrolladores de Win32 también pueden usar el paralelismo de la GPU para el cálculo de uso general, como el procesamiento de imágenes, y pueden representarse en hardware de DirectX 10, DirectX 9, CPU o en un equipo remoto de Windows. Estas tecnologías se diseñaron para interoperar con Windows Interfaz de dispositivo gráfico (GDI) y Windows GDI+, lo que garantiza que los desarrolladores puedan conservar fácilmente sus inversiones existentes en código Win32. (Vea [las novedades del SDK de DirectX 2009 de marzo](/previous-versions//bb173043(v=vs.85))).

Estas funcionalidades de gráficos mejoradas las proporcionan las siguientes API basadas en *com*:

-   [Direct2D](../direct2d/direct2d-portal.md) para dibujar gráficos 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para organizar y representar texto.
-   [Componente de creación de imágenes de Windows](/windows/desktop/wic/-wic-lh) para procesar y mostrar imágenes.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) para dibujar gráficos 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para dibujar gráficos 3D y proporcionar acceso a las tecnologías GPU de la próxima generación, como teselación, compatibilidad limitada para el streaming de texturas y informática de uso general.
-   [Infraestructura de gráficos de DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) para administrar dispositivos de pantalla locales y remotos y recursos de GPU, y proporcionar interoperabilidad entre DirectX y GDI.

## <a name="direct2d"></a>Direct2D

Basado en Microsoft Direct3D 10, [Direct2D](../direct2d/direct2d-portal.md) ofrece a los desarrolladores de Win32 API en modo inmediato, independientes de la resolución y en 2D que usan el potencial de hardware gráfico de próxima generación, pero interoperan bien con las aplicaciones GDI/GDI+ actuales y con las aplicaciones de Direct3D 10. Direct2D proporciona una representación 2D de alta calidad con un rendimiento superior a GDI y GDI+. Proporciona a los desarrolladores de Win32 un mayor control sobre los recursos y su administración. (Consulte [Direct2D](../direct2d/direct2d-portal.md)).

## <a name="directwrite"></a>DirectWrite

Muchas de las aplicaciones actuales necesitan admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad con el diseño y el texto Unicode completo. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), un nuevo componente de DirectX, proporciona estas características y mucho más:

-   Sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.
-   Representación de texto de alta calidad, subpíxel y *ClearType* que puede usar la tecnología de representación de GDI, [Direct2D](../direct2d/direct2d-portal.md)o específica de la aplicación.
-   Texto con aceleración de hardware, cuando se usa con [Direct2D](../direct2d/direct2d-portal.md).
-   Compatibilidad con texto con varios formatos.
-   Compatibilidad con las características tipográficas avanzadas de las fuentes *OpenType* .
-   Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.
-   Diseño y representación compatibles con GDI.

El sistema de fuentes [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) habilita el uso de fuentes "cualquier fuente cualquier lugar", donde los usuarios no tienen que realizar un paso de instalación independiente solo para usar una fuente, y una jerarquía estructural mejorada de la agrupación de fuentes para ayudar con la detección de fuentes manual o mediante programación. Las API admiten la medición, el dibujo y la prueba de posicionamiento de texto de varios formatos. DirectWrite controla el texto en todos los idiomas admitidos para las aplicaciones globales y localizadas, y se basa en la infraestructura de idioma clave que se encuentra en Windows 7. DirectWrite también proporciona API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y el procesamiento de Unicode a glifo. (Consulte [DirectWrite](../directwrite/direct-write-portal.md)).

## <a name="windows-imaging-component"></a>Windows Imaging Component

En Windows Vista, el [componente de creación de imágenes de Windows](/windows/desktop/wic/-wic-lh) presentó un marco extensible para trabajar con imágenes y metadatos de imágenes. Los formatos de imagen admitidos por el componente de creación de imágenes de Windows incluyen *JPEG*, *PNG* y *TIFF*, y los formatos de metadatos admitidos son *XMP* y *Exif*. Con Windows 7, el componente de creación de imágenes de Windows amplía su compatibilidad con estándares proporcionando compatibilidad para descodificación progresiva de imágenes, características de *PNG* expandidas, metadatos *GIF* y metadatos que abarcan segmentos *APPN* . (Vea las novedades [de WIC en Windows 7](/previous-versions//ee720061(v=vs.85))).

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 amplía la funcionalidad de la canalización de Direct3D 10 y proporciona juegos de Windows 7 y aplicaciones 3D de alto nivel con acceso eficaz, sólido y escalable a la próxima generación de GPU y CPU de varios núcleos. Además de la funcionalidad que se encuentra en Direct3D 10, Direct3D 11 presenta varias características nuevas.

Ahora, las superficies de geometría y de orden superior pueden ser teselas para admitir contenido dinámico y escalable en representaciones de superficie de revisión y subdivisión.

Para hacer un buen uso de la capacidad de procesamiento en paralelo disponible desde varios núcleos de CPU, el multithreading aumenta el número de llamadas de representación potenciales por fotogramas mediante la distribución de la aplicación, el tiempo de ejecución y las llamadas de controlador entre varios núcleos. Además, la creación y administración de recursos se ha optimizado para el uso multiproceso, lo que permite una administración de texturas dinámica más eficaz para la transmisión por secuencias.

Se han creado nuevos sombreadores de cálculo de uso general para Direct3D 11. A diferencia de los sombreadores existentes, son extensiones de la canalización programable que permiten que la aplicación realice más trabajo completamente en la GPU, independientemente de la CPU. [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), que se presentó en Direct3D 10, se ha ampliado para interactuar con un sombreador de cálculo.

Se han realizado varias mejoras en el lenguaje de sombreado de alto nivel ([HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)), como una forma limitada de vinculación dinámica en los sombreadores para mejorar la complejidad de la especialización, y las construcciones de programación orientada a objetos como clases e interfaces. (Vea [las novedades del SDK de DirectX 2009 de marzo](/previous-versions//bb173043(v=vs.85))).

## <a name="direct3d-10-improvements"></a>Mejoras en Direct3D 10

Direct3D 10 incluye una canalización de gráficos rediseñada con fases del sombreador programables y objetos de estado inmutables para inicializar las fases de la función fija. Los objetos de estado simplifican la canalización y mejoran el rendimiento al minimizar el número de cambios de estado necesarios. La programación de las fases del sombreador ahora ofrece extensiones de lenguaje de sombreado de alto nivel para admitir instrucciones de sombreador ilimitadas, recursos de sombreador generalizados y cálculos enteros y bit a bit.

La canalización también presenta la fase del sombreador de geometría, que descarga todo el trabajo de la CPU a la GPU. Esta nueva fase permite crear geometría, transmitir los datos a la memoria y representar la geometría sin interacción de la CPU.

Muchas otras mejoras están diseñadas específicamente para un rendimiento más rápido. La representación de predicados realiza la selección de la oclusión para reducir la cantidad de geometría que se representa. Las API de creación de instancias pueden reducir drásticamente la cantidad de geometría que se debe transferir a la GPU dibujando varias instancias de objetos similares. Las matrices de textura permiten que la GPU realice el intercambio de texturas sin la intervención de la CPU.

Se han realizado varias adiciones a Direct3D 10 y Direct3D 11 para ampliar la gama de configuraciones que se pueden usar con estas API. [Windows Advanced rasterization Platform (warp)](/windows/desktop/direct3darticles/directx-warp) implementa una representación de CPU escalable rápida y de varios núcleos para Direct3D 10, lo que permite la representación de gráficos con todas las características en sistemas sin hardware de gráficos. La adición de nuevos "niveles de características", específicamente denominado [Direct3D 10 nivel 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9), permite a Direct3D 10 y Direct3D 11APIs controlar el hardware de Microsoft Direct3D 9-Class, lo que amplía el número de configuraciones que una aplicación de Direct3D 10 o Direct3D 11 puede dirigirse a casi todos los equipos del mercado. (Vea [gráficos de Direct3D 10](../direct3d10/d3d10-graphics.md)).

## <a name="directxgdi-interoperability"></a>Interoperabilidad de DirectX/GDI

En Windows Vista, el comportamiento de una aplicación que usa tanto DirectX como GDI para representar en una superficie compartida es diferente en función de si DWM está activado o desactivado. Además, cuando DWM está activado, las aplicaciones que usan tanto DirectX como GDI se comportan de manera diferente en Windows Vista que en Windows XP. Esto provocó que varios ISV deshabilitaran DWM al ejecutar sus aplicaciones en Windows Vista para garantizar un comportamiento coherente. Con las mejoras de DirectX en Windows 7, una aplicación ahora puede mezclar libremente DirectX y GDI sin deshabilitar DWM. Windows 7 también incluye un rendimiento mejorado para escenarios que requieren interoperación entre DirectX y GDI mediante el uso de las API de Direct3D 10 más eficaces. (Consulte [información general sobre interoperación de Direct2D e GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md)).

 

 