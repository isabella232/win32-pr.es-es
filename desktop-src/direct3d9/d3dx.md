---
description: D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360041"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).

En esta versión del SDK de DirectX, solo se proporciona una versión de D3DX. El archivo DLL de D3DX comercial se incluye en el redistribuible proporcionado en el SDK y se instala automáticamente como parte de la [instalación de DirectX con DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx). La biblioteca de D3DX incluida en esta versión depende de los tiempos de ejecución de Direct3D que se incluyen con este SDK. Las aplicaciones que se vinculan a la versión de D3DX en esta versión también deben redistribuir el Runtime desde este SDK.

Varias versiones de D3DX pueden residir de forma independiente en un único sistema simultáneamente. Al vincular estáticamente una aplicación a D3dx9. lib, la aplicación se vincula dinámicamente a la DLL de la versión de lanzamiento correspondiente en tiempo de ejecución. Este archivo DLL corresponde a los encabezados de D3DX en los que se compila la aplicación (denominados con la \_ \_ constante versión del SDK de D3dx en D3dx9core. h). A medida que se publiquen nuevas versiones de D3DX en versiones futuras del SDK de DirectX, las aplicaciones que se vinculan a bibliotecas de D3DX anteriores permanecerán inalteradas.

La biblioteca de D3DX aborda estas áreas generales de funcionalidad:

-   [Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Compatibilidad de malla en D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Compatibilidad con texturas en D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 



