---
description: D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d1f7dfe7f8d841220af4f5dbe650bd74e4c8dff86812650545a07129af644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986915"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

> [!NOTE]
> La biblioteca D3DX está en desuso. Si la actualización a una versión más reciente de Direct3D y el código de utilidad asociado no es una opción, puede usar el paquete [microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet en lugar de confiar en el SDK de DirectX heredado o DirectSetup.

D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).

Solo se proporciona una versión de D3DX en esta versión del SDK de DirectX. El archivo DLL D3DX comercial se incluye en el redistribuible proporcionado en el SDK y se instala automáticamente como parte de la instalación de **DirectX con DirectSetup.** La biblioteca D3DX incluida en esta versión depende de los entornos de ejecución de Direct3D que se incluyen con este SDK. Las aplicaciones que se vinculan con la versión de D3DX de esta versión también deben redistribuir el entorno de ejecución de este SDK.

Varias versiones de D3DX pueden residir de forma independiente en un único sistema simultáneamente. Al vincular estáticamente una aplicación a D3dx9.lib, la aplicación se vincula dinámicamente al archivo DLL D3DX comercial correspondiente en tiempo de ejecución. Este archivo DLL corresponde a los encabezados D3DX con los que se compila la aplicación (denominados con la constante VERSION del SDK D3DX en \_ \_ D3dx9core.h). A medida que se envíen nuevas versiones de D3DX en futuras versiones del SDK de DirectX, las aplicaciones que se vinculen a bibliotecas D3DX anteriores no se verán afectadas.

La biblioteca D3DX aborda estas áreas generales de funcionalidad:

-   [Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Compatibilidad con mallas en D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Compatibilidad con texturas en D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 



