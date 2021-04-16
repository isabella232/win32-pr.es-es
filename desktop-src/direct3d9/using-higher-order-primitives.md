---
description: En esta sección se muestra cómo usar primitivas de orden superior en la aplicación.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Usar primitivas de Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562719"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Usar primitivas de Higher-Order (Direct3D 9)

En esta sección se muestra cómo usar primitivas de orden superior en la aplicación.

-   [Determinación de la compatibilidad con Higher-Order primitiva](#determining-higher-order-primitive-support)
-   [Dibujar revisiones](#drawing-patches)
-   [Generar las coordenadas normales y de textura](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinación de la compatibilidad con Higher-Order primitiva

Se puede consultar el miembro DevCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar el nivel de compatibilidad para las operaciones que implican primitivas de orden superior. En la tabla siguiente se enumeran las funcionalidades del dispositivo relacionadas con los primitivos de orden superior en Direct3D 9.



| Funcionalidad del dispositivo             | Descripción                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | El dispositivo admite N-patches y se basa en [triángulos de PN curvos](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (un tipo especial de triángulos Bézier cúbicos). |
| D3DDEVCAPS \_ QUINTICRTPATCHES  | El dispositivo admite curvas Bézier quintales y B-Splines.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | El dispositivo es compatible con las revisiones rectangulares y triangulares (RT-patchs).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | RT: las revisiones se pueden dibujar eficazmente con el identificador cero.                                                                                                     |



 

Tenga en cuenta que D3DDEVCAPS \_ RTPATCHHANDLEZERO no significa que se pueda dibujar una revisión con el identificador cero. Siempre se puede dibujar un identificador sin revisión, si esta funcionalidad del dispositivo está establecida o no. Cuando se establece esta funcionalidad, la arquitectura de hardware no requiere almacenamiento en caché de ninguna información y las revisiones sin almacenamiento en caché (identificador cero) se dibujan de la manera más eficaz que las almacenadas en caché.

## <a name="drawing-patches"></a>Dibujar revisiones

Direct3D 9 admite dos tipos de elementos primitivos de orden superior o revisiones. Estas se conocen como parches N-patchs y Rect/Tri. N-las revisiones se pueden representar con cualquier llamada de representación por triángulo habilitando N-patches a través de la llamada a [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)(nSegments) con un valor de nSegments superior a 1,0. Las revisiones Rect/Tri se deben representar con los siguientes puntos de entrada explícitos.

Puede usar los métodos siguientes para dibujar revisiones.

-   [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Para comprender mejor cómo se hace referencia a los datos de la revisión en el búfer de vértices, consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api). Para comprender mejor cómo se hace referencia a los datos de la revisión en el búfer de vértices, consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) dibuja una revisión rectangular de orden superior especificada por el parámetro pRectPatchInfo mediante las secuencias establecidas actualmente. El parámetro Handle se usa para asociar la revisión a un identificador, de modo que la próxima vez que se dibuje la revisión, no sea necesario volver a especificar pRectPatchInfo. Esto hace posible calcular y almacenar en caché los coeficientes de diferencia y otra información, lo que a su vez permite llamadas posteriores a **IDirect3DDevice9::D rawrectpatch** con el mismo identificador para ejecutarse de forma eficaz.

Está pensada para las revisiones estáticas, una aplicación establecería el sombreador de vértices y las secuencias adecuadas, suministraría información de revisión en el parámetro pRectPatchInfo y especificaría un identificador para que Direct3D pueda capturar y almacenar en caché información. A continuación, la aplicación puede llamar a [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) posteriormente con pRectPatchInfo establecido en **null** para dibujar la revisión de forma eficaz. Al dibujar una revisión almacenada en caché, se omiten las secuencias establecidas actualmente. Sin embargo, es posible invalidar el pNumSegs almacenado en caché especificando nuevos valores para pNumSegs. Además, es necesario establecer el mismo sombreador de vértices al representar una revisión almacenada en caché tal y como se estableció cuando se capturó.

En el caso de las revisiones dinámicas, los datos de revisión cambian para cada representación de la revisión, por lo que no es eficaz almacenar en caché la información. La aplicación puede transmitir esto a Direct3D estableciendo el identificador en 0. En este caso, Direct3D dibuja la revisión mediante las secuencias establecidas actualmente y los valores pNumSegs y no almacena en caché ninguna información. No es válido establecer simultáneamente el identificador en 0 y pPatch en **null**.

Al volver a especificar pRectPatchInfo para el mismo identificador, la aplicación puede sobrescribir la información almacenada previamente en la memoria caché.

[**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) es similar a [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) , salvo que dibuja una revisión de orden superior triangular.

## <a name="generating-normals-and-texture-coordinates"></a>Generar las coordenadas normales y de textura

Si usa un sombreador de formato de vértice flexible (FVF), no es posible la generación automática de las coordenadas normales y de textura.

Para los valores normales, puede proporcionarlos directamente o hacer que Direct3D los calcule automáticamente.

Las coordenadas generadas para las revisiones rectangulares son coordenadas basadas en spline, tal como se muestra en las ilustraciones siguientes.

![Ilustración de una textura original y la textura con coordenadas basadas en spline](images/texturespline.png)

Las coordenadas generadas para las revisiones triangulares son coordenadas basadas en spline Barycentric, tal y como se muestra en las ilustraciones siguientes.

![Ilustración de una textura original y la textura con coordenadas basadas en spline Barycentric](images/texturebarycentricspline.png)

Si una aplicación debe cambiar el intervalo de las coordenadas de textura generadas, esto se puede hacer mediante transformaciones de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Primitivas de orden superior](higher-order-primitives.md)
</dt> </dl>

 

 
