---
description: El contenido de la textura suele almacenarse en formato sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714657"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

El contenido de la textura suele almacenarse en formato sRGB. Tradicionalmente, las canalizaciones de píxeles suponía que los colores eran lineales, por lo que las operaciones de combinación se realizaban en el espacio lineal. Sin embargo, dado que el contenido de sRGB se corrigió en gamma, las operaciones de mezcla en el espacio lineal producirán resultados incorrectos. Ahora, las tarjetas de vídeo pueden solucionar este problema deshaciendo la corrección de gamma cuando leen el contenido de sRGB y convierten los datos de píxeles al formato sRGB al escribir los píxeles. En este caso, todas las operaciones dentro de la canalización de píxeles se realizan en el espacio lineal.

## <a name="gamma-correction"></a>Corrección gamma

Direct3D 9 puede:

-   Indicar si una textura es gamma 2,2 corregida o no (sRGB o not). El controlador se convertirá en un gamma lineal para las operaciones de fusión en tiempo de SetTexture, o la muestra lo convertirá en datos lineales en el momento de la búsqueda.
-   Indique si la canalización de píxeles debe volver a corregir el espacio sRGB al escribir en el destino de representación.

Se supone que todos los demás colores (color claro, color del material, color de vértice, etc.) están en el espacio lineal. Las aplicaciones pueden corregir los colores que se escriben en el búfer de fotogramas mediante instrucciones del sombreador de píxeles. La linealidad solo debe aplicarse a los canales RGB y no al canal alfa.

No todos los formatos de superficie se pueden alinear. Solo los formatos que pasan [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ consulta \_ SRGBREAD se pueden alinear. El estado de muestra D3DSAMP \_ SRGBTEXTURE se omite en el resto. Solo se espera que los formatos de textura sin firmar admitan esta conversión. Los formatos de textura sin signo incluyen solo los componentes R, G, B y L. Si el canal alfa está presente, se omite. Si los formatos mixtos admiten la linealidad sRGB, solo se ven afectados los canales sin signo. Idealmente, el hardware debe realizar la linealización antes del filtrado, pero en Direct3D 9, el hardware puede realizar la linealización después del filtrado.

No todos los formatos de superficie se pueden escribir en el espacio sRGB. Solo se pueden alinear los formatos que pasan [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con la marca de uso D3DUSAGE \_ consulta \_ SRGBWRITE. El estado de representación D3DRS \_ SRGBWRITEENABLE se omite en el resto. Se espera que los formatos sin signo RGB de ocho bits por canal expongan esta capacidad.

Idealmente, el hardware debe realizar las operaciones de fusión de búfer de fotogramas en el espacio lineal, pero el hardware puede realizarla después del sombreador de píxeles, pero antes del mezclador de búfer de fotogramas. Esto significa que las operaciones de fusión de búfer de fotogramas que tienen lugar en el espacio sRGB producirán resultados incorrectos. D3DRS \_ SRGBWRITEENABLE se respeta mientras se realiza un borrado del destino de representación. En el caso de hardware que admita [varios destinos de representación (Direct3D 9)](multiple-render-targets.md) o [texturas de varios elementos (Direct3D 9)](multiple-element-textures.md), solo se escribe el primer destino o elemento de representación.

### <a name="api-changes"></a>Cambios de la API


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>Cadenas de intercambio en ventanas

Es importante que las aplicaciones mantengan los búferes de reserva de sus cadenas de intercambio en el espacio lineal para habilitar las operaciones de mezcla correctas. Dado que el escritorio no suele estar en el espacio lineal, se requiere una corrección gamma antes de que se pueda presentar el contenido del búfer de reserva. La aplicación puede afectar a esta corrección mediante la asignación de un búfer adicional y la realización de su propia copia de corrección del búfer lineal en el búfer de reserva. Esto requiere una copia adicional que se puede evitar si el controlador realiza una corrección gamma como parte de la presentación.

En Direct3D 9, existe una nueva marca, [D3DPRESENT \_ linear \_ Content](d3dpresent.md) [**, que permite**](/windows/desktop/api) que la presentación se convierta implícitamente del espacio lineal al sRGB/gamma 2,2. Las aplicaciones deben especificar esta marca si el formato de búfer de reserva es un punto flotante de 16 bits para que coincida con el modo de ventana presente en el comportamiento de gamma de pantalla completa, siempre que \_ \_ \_ se devuelva la presentación D3DCAPS3 linear to sRGB \_ para las funcionalidades de dispositivo recuperadas a través de [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búfer de fotogramas](frame-buffer.md)
</dt> </dl>

 

 
