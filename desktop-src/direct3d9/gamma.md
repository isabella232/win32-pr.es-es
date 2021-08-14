---
description: El contenido de textura a menudo se almacena en formato sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ede077347d67c1657b86ad09b778625e22fd19a39c8333d7f11fec51be53b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523028"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

El contenido de textura a menudo se almacena en formato sRGB. Tradicionalmente, las canalizaciones de píxeles suponen que los colores son lineales, por lo que las operaciones de combinación se realizaron en el espacio lineal. Sin embargo, dado que el contenido de sRGB se corrige gamma, las operaciones de combinación en el espacio lineal producirán resultados incorrectos. Las tarjetas de vídeo ahora pueden corregir este problema si se deshace la corrección gamma cuando se lee cualquier contenido sRGB y se convierten los datos de píxeles al formato sRGB al escribir píxeles. En este caso, todas las operaciones dentro de la canalización de píxeles se realizan en el espacio lineal.

## <a name="gamma-correction"></a>Corrección gamma

Direct3D 9 puede:

-   Indique si una textura es gamma 2.2 corregida o no (sRGB o no). El controlador se convertirá en un gamma lineal para combinar operaciones en el momento de SetTexture, o bien el muestreador lo convertirá en datos lineales en tiempo de búsqueda.
-   Indique si la canalización de píxeles debe volver a corregir gamma al espacio sRGB al escribir en el destino de representación.

Se supone que todos los demás colores (color claro, color de material, color de vértice, etc.) están en un espacio lineal. Las aplicaciones pueden corregir gammamente los colores escritos en el búfer de fotogramas mediante instrucciones del sombreador de píxeles. La linealización solo se debe aplicar a los canales RGB y no al canal alfa.

No todos los formatos de superficie se pueden linealizar. Solo se pueden linealizar los formatos que pasan [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ SRGBREAD. El estado del muestreador D3DSAMP \_ SRGBTEXTURE se omite para el resto. Solo se espera que los formatos de textura sin signo admitan esta conversión. Los formatos de textura sin signo incluyen solo los componentes R, G, B y L. Si el canal alfa está presente, se omite. Si los formatos mixtos admiten la linealización sRGB, solo se verán afectados los canales sin signo. Idealmente, el hardware debe realizar la linealización antes del filtrado, pero en Direct3D 9, el hardware puede realizar la linealización después del filtrado.

No todos los formatos de superficie se pueden escribir en espacio sRGB. Solo se pueden linealizar los formatos que pasan [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con la marca de uso D3DUSAGE \_ QUERY \_ SRGBWRITE. El estado de representación D3DRS \_ SRGBWRITEENABLE se omite para el resto. Se espera que los formatos RGB sin signo de ocho bits por canal exponán esta capacidad.

Lo ideal es que el hardware realice las operaciones de combinación del búfer de fotogramas en el espacio lineal, pero el hardware puede realizarlo después del sombreador de píxeles, pero antes del combinador de búfer de fotogramas. Esto significa que las operaciones de combinación del búfer de fotogramas que se producen en el espacio sRGB producirán resultados incorrectos. D3DRS \_ SRGBWRITEENABLE se respeta mientras se realiza una despejación del destino de representación. Para el hardware que admite varios destinos de representación [(Direct3D 9)](multiple-render-targets.md) o texturas de varios elementos [(Direct3D 9),](multiple-element-textures.md)solo se escribe el primer destino o elemento de representación.

### <a name="api-changes"></a>Cambios de API


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



### <a name="windowed-swap-chains"></a>Cadenas de intercambio por ventanas

Resulta útil para las aplicaciones mantener los búferes de reserva de sus cadenas de intercambio en el espacio lineal con el fin de habilitar las operaciones de combinación correctas. Dado que el escritorio no suele estar en un espacio lineal, se requiere una corrección gamma antes de que se pueda presentar el contenido del búfer de reserva. La aplicación puede realizar esta corrección asignando un búfer adicional y realizando su propia copia de corrección del búfer lineal al búfer de reserva. Esto requiere una copia adicional que se puede evitar si el controlador realiza la corrección gamma como parte de la presentación blit.

En Direct3D 9 hay disponible una nueva marca, [D3DPRESENT \_ LINEAR \_ CONTENT](d3dpresent.md), para [**Present**](/windows/desktop/api) que permite a la presentación convertir implícitamente el espacio lineal a sRGB/gamma 2.2. Las aplicaciones deben especificar esta marca si el formato de búfer de reserva es de punto flotante de 16 bits con el fin de hacer coincidir el modo de ventana presente con el comportamiento gamma de pantalla completa, siempre que D3DCAPS3 LINEAR TO SRGB PRESENTATION se devuelva para las funcionalidades del dispositivo recuperadas a través de \_ \_ \_ \_ [**GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búfer de fotogramas](frame-buffer.md)
</dt> </dl>

 

 
