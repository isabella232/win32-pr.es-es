---
description: Direct3D es una API de bajo nivel para dibujar primitivos con la canalización de representación o para realizar operaciones paralelas con el sombreador de cálculo.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Introducción a Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706433"
---
# <a name="getting-started-with-direct3d"></a>Introducción a Direct3D

Direct3D es una API de bajo nivel para dibujar primitivos con la canalización de representación, o para realizar operaciones paralelas con el sombreador de cálculo.

## <a name="what-is-direct3d"></a>¿Qué es Direct3D?

Direct3D es una API de bajo nivel que puede usar para dibujar triángulos, líneas o puntos por fotograma, o para iniciar operaciones muy paralelas en la GPU.

3D

-   Oculta diferentes implementaciones de GPU detrás de una abstracción coherente. Pero todavía necesita saber cómo dibujar gráficos 3D.
-   Está diseñado para impulsar un procesador independiente específico de gráficos. Las GPU más recientes tienen cientos o miles de procesadores en paralelo.
-   Enfatiza el procesamiento paralelo. Configure un grupo de representación o estado de proceso y, a continuación, inicie una operación. No espera los comentarios inmediatos de la operación. No se combinan las operaciones de CPU y GPU.

## <a name="which-direct3d-apis-can-you-use"></a>¿Qué API de Direct3D puede usar?

Las API de Direct3D que elija dependen del estilo de la aplicación que desee escribir.

-   Si desea escribir una aplicación para UWP, use un subconjunto de las API de Direct3D 11, DXGI y HLSL. Para obtener una lista de estas API, consulte [Win32 y API de com para aplicaciones de UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Para obtener información sobre cómo escribir una aplicación de la tienda Windows de Direct3D 11, consulte [crear gráficos 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Si escribe una aplicación de escritorio, puede usar el conjunto completo de las API de Direct3D 11, DXGI y HLSL.
-   A partir de Windows 8, ya no se admite activamente el marco XNA para aplicaciones de escritorio. Sin embargo, las aplicaciones de la tienda Windows, las aplicaciones para UWP y las aplicaciones de escritorio pueden usar el conjunto completo de las API de [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) y [DirectXMath](/windows/desktop/dxmath/directxmath-portal) . Las aplicaciones de escritorio pueden usar el conjunto completo de las API de [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) , mientras que las aplicaciones de la tienda Windows y las aplicaciones para UWP pueden usar la mayoría de las API de XInput. para obtener más información, consulte [las versiones de XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>¿Qué versión de Direct3D?

La versión de la API de Direct3D que elija dependerá del sistema operativo y del nivel de hardware que desee usar como destino.

-   Si desea tener como destino Windows 8 y versiones posteriores, use las API de Direct3D 11.
-   Usar las API de Direct3D 9 con Windows XP y versiones posteriores. Todo el hardware es compatible con las API de Direct3D 9, incluso con hardware más reciente de nivel 11 de Direct3D.
-   Use las API de Direct3D 10 con Windows Vista y versiones posteriores. Solo Direct3D de nivel 10 y versiones posteriores admiten las API de Direct3D 10.
-   Use las API de Direct3D 10,1 y Direct3D 11 con Windows 7 y versiones posteriores. También puede usar las API de Direct3D 10,1 y Direct3D 11 con Windows Vista con Service Pack 2 (SP2) Si descarga [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Canalización de representación de Direct3D

En la [canalización de representación](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)de Direct3D, los datos fluyen desde varios orígenes, como el Tributaries de un río.

-   Algunas partes del flujo son programables.
-   Algunas partes tienen botones y dials.
-   Los orígenes de datos son secuencias en serie de paquetes (vértices) o matrices indexables (recursos del sombreador).
-   Los vértices y los recursos del sombreador fluyen en primitivos, que se pueden ampliar.
-   Los elementos primitivos y los recursos del sombreador fluyen en operaciones de píxeles.

## <a name="direct3d-compute-shader"></a>Sombreador de cálculo de Direct3D

Con el [sombreador de cálculo](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)de Direct3D, todos los procesadores de la GPU se ejecutan en paralelo. Por lo tanto, el sombreador de cálculo se comporta más como un estanque que un río.
