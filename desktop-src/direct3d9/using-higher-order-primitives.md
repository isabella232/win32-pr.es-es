---
description: En esta sección se muestra cómo usar primitivas de orden superior en la aplicación.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Usar Higher-Order primitivos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473236"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Usar Higher-Order primitivos (Direct3D 9)

En esta sección se muestra cómo usar primitivas de orden superior en la aplicación.

-   [Determinar la Higher-Order primitiva](#determining-higher-order-primitive-support)
-   [Dibujar revisiones](#drawing-patches)
-   [Generar normales y coordenadas de textura](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinar la Higher-Order primitiva

Se puede consultar el miembro DevCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar el nivel de compatibilidad con las operaciones que implican primitivas de orden superior. En la tabla siguiente se enumeran las funcionalidades del dispositivo relacionadas con las primitivas de orden superior en Direct3D 9.



| Funcionalidad del dispositivo             | Descripción                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | El dispositivo admite N revisiones y se basa en [triángulos PN curvados](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (un tipo especial de triángulos Bézier cúbicas). |
| D3DDEVCAPS \_ CHINTICRTPATCHES  | El dispositivo admite curvas Bézier y B-splines.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | El dispositivo admite revisiones rectangulares y triangulares (rt-patches).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | Las revisiones RT se pueden dibujar de forma eficaz mediante el identificador cero.                                                                                                     |



 

Tenga en cuenta que D3DDEVCAPS RTPATCHHANDLEZERO no significa que se pueda dibujar una revisión \_ con el identificador cero. Siempre se puede dibujar una revisión de identificador cero, independientemente de si esta funcionalidad del dispositivo está establecida o no. Cuando se establece esta funcionalidad, la arquitectura de hardware no requiere el almacenamiento en caché de ninguna información y que las revisiones no almacenadas en caché (controlar cero) se extraen de forma tan eficaz como las almacenadas en caché.

## <a name="drawing-patches"></a>Dibujar revisiones

Direct3D 9 admite dos tipos de primitivas de orden superior o revisiones. Se conocen como N revisiones y revisiones de tipo "Rect/Tri". Las N revisiones se pueden representar mediante cualquier llamada de representación de triángulos habilitando N-patches a través de la llamada a [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)( nSegments ) con un valor de nSegments mayor que 1.0. Las revisiones rect/tri deben representarse con los siguientes puntos de entrada explícitos.

Puede usar los métodos siguientes para dibujar revisiones.

-   [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Para comprender mejor cómo se hace referencia a los datos de revisión en el búfer de vértices, vea [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api). Para comprender mejor cómo se hace referencia a los datos de revisión en el búfer de vértices, vea [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) dibuja una revisión rectangular de orden alto especificada por el parámetro pRectPatchInfo mediante las secuencias establecidas actualmente. El parámetro Handle se usa para asociar la revisión a un identificador, de modo que la próxima vez que se dibuje la revisión, no es necesario volver a especificar pRectPatchInfo. Esto permite precalcribir y almacenar en caché coeficientes de diferencias de avance u otra información, lo que a su vez permite llamadas posteriores a **IDirect3DDevice9::D rawRectPatch** con el mismo identificador para ejecutarse de forma eficaz.

Está pensado para que, para las revisiones estáticas, una aplicación establezca el sombreador de vértices y las secuencias adecuadas, proporcione información de revisión en el parámetro pRectPatchInfo y especifique un identificador para que Direct3D pueda capturar y almacenar en caché información. A continuación, la aplicación puede llamar a [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) posteriormente con pRectPatchInfo establecido en **NULL** para dibujar eficazmente la revisión. Al dibujar una revisión almacenada en caché, se omiten las secuencias establecidas actualmente. Sin embargo, es posible invalidar los pNumSegs almacenados en caché especificando nuevos valores para pNumSegs. Además, es necesario establecer el mismo sombreador de vértices al representar una revisión almacenada en caché que se estableció cuando se capturó.

En el caso de las revisiones dinámicas, los datos de revisión cambian para cada representación de la revisión, por lo que no es eficaz almacenar en caché la información. La aplicación puede transmitir esto a Direct3D estableciendo Handle en 0. En este caso, Direct3D dibuja la revisión mediante los flujos establecidos actualmente y los valores pNumSegs y no almacena en caché ninguna información. No es válido establecer handle simultáneamente en 0 y pPatch en **NULL.**

Al volver a especificar pRectPatchInfo para el mismo identificador, la aplicación puede sobrescribir la información almacenada previamente en caché.

[**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) es similar a [**IDirect3DDevice9::D rawRectPatch,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) salvo que dibuja una revisión de orden superior triangular.

## <a name="generating-normals-and-texture-coordinates"></a>Generar normales y coordenadas de textura

Si usa un sombreador de formato de vértice flexible (FVF), no es posible la generación automática de normales y coordenadas de textura.

Para las normales, puede suministrarlas directamente o hacer que Direct3D las calcule automáticamente.

Las coordenadas generadas para las revisiones rectangulares son coordenadas basadas en spline, como se muestra en las ilustraciones siguientes.

![ilustración de una textura original y la textura con coordenadas basadas en spline](images/texturespline.png)

Las coordenadas generadas para las revisiones triangulares son coordenadas basadas en spline centradas en barras, como se muestra en las ilustraciones siguientes.

![ilustración de una textura original y la textura con coordenadas basadas en spline centradas en barras](images/texturebarycentricspline.png)

Si una aplicación debe cambiar el intervalo de las coordenadas de textura generadas, esto se puede hacer mediante transformaciones de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Primitivas de orden superior](higher-order-primitives.md)
</dt> </dl>

 

 
