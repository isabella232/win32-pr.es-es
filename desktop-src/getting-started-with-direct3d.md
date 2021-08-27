---
description: Direct3D es una API de bajo nivel para dibujar primitivas con la canalización de representación o realizar operaciones paralelas con el sombreador de proceso.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Introducción a Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092555"
---
# <a name="getting-started-with-direct3d"></a>Introducción a Direct3D

Direct3D es una API de bajo nivel para dibujar primitivas con la canalización de representación o para realizar operaciones paralelas con el sombreador de proceso.

## <a name="what-is-direct3d"></a>¿Qué es Direct3D?

Direct3D es una API de bajo nivel que se puede usar para dibujar triángulos, líneas o puntos por fotograma, o para iniciar operaciones muy paralelas en la GPU.

Direct3d:

-   Oculta diferentes implementaciones de GPU detrás de una abstracción coherente. Pero todavía necesita saber cómo dibujar gráficos 3D.
-   Está diseñado para impulsar un procesador independiente específico de gráficos. Las GPU más recientes tienen cientos o miles de procesadores paralelos.
-   Resalta el procesamiento paralelo. Configure una serie de representaciones o estado de proceso y, a continuación, inicie una operación. No espere a recibir comentarios inmediatos de la operación. No se mezclan las operaciones de CPU y GPU.

## <a name="which-direct3d-apis-can-you-use"></a>¿Qué API de Direct3D puede usar?

Las API de Direct3D que elija dependen del estilo de la aplicación que quiera escribir.

-   Si quieres escribir una aplicación para UWP, usa un subconjunto de LAS API de Direct3D 11, DXGI y HLSL. Para obtener una lista de estas API, consulta [Win32 y API COM para aplicaciones para UWP.](/uwp/win32-and-com/win32-and-com-for-uwp-apps) Para obtener información sobre cómo escribir una aplicación de Direct3D 11 Windows Store, consulte Creación de gráficos [3D con DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))
-   Si escribe una aplicación de escritorio, puede usar el conjunto completo de API de Direct3D 11, DXGI y HLSL.
-   A partir Windows 8, ya no se admite activamente el marco XNA para aplicaciones de escritorio. Pero Windows store, las aplicaciones para UWP y las aplicaciones de escritorio pueden usar el conjunto completo de las API [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) y [DirectXMath.](/windows/desktop/dxmath/directxmath-portal) Las aplicaciones de escritorio pueden usar el conjunto completo de las API [de XInput,](/windows/desktop/xinput/xinput-game-controller-apis-portal) mientras que Windows Store y las aplicaciones para UWP pueden usar la mayoría de las API de XInput. Para obtener más información, vea [Versiones de XInput.](/windows/desktop/xinput/xinput-versions)

## <a name="which-direct3d-version"></a>¿Qué versión de Direct3D?

La versión de la API de Direct3D que elija depende del sistema operativo y el nivel de hardware de destino.

-   Si desea tener como destino Windows 8 y versiones posteriores, use las API de Direct3D 11.
-   Use las API de Direct3D 9 con Windows XP y versiones posteriores. Todo el hardware admite las API de Direct3D 9, incluso hardware de nivel 11 de Direct3D más reciente.
-   Use las API de Direct3D 10 Windows Vista y versiones posteriores. Solo el hardware de nivel 10 de Direct3D y versiones posteriores admite las API de Direct3D 10.
-   Use las API de Direct3D 10.1 y Direct3D 11 con Windows 7 y versiones posteriores. También puede usar las API de Direct3D 10.1 y Direct3D 11 con Windows Vista con Service Pack 2 (SP2) descargando [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Canalización de representación de Direct3D

En la canalización [](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)de representación de Direct3D, los datos fluyen desde varios orígenes, como las vistas de un canal.

-   Algunas partes del flujo se pueden programar.
-   Algunas partes tienen botones y marcas.
-   Los orígenes de datos son secuencias serie de paquetes (vértices) o matrices indexables (recursos de sombreador).
-   Los vértices y los recursos del sombreador fluyen en primitivas, que se pueden ampliar.
-   Las primitivas y los recursos del sombreador fluyen en operaciones de píxeles.

## <a name="direct3d-compute-shader"></a>Sombreador de proceso de Direct3D

Con el sombreador de [proceso](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)de Direct3D, todos los procesadores de GPU se ejecutan en paralelo. Por lo tanto, el sombreador de proceso se comporta más como un casco que un lago.
