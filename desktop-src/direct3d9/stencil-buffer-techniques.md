---
description: Las aplicaciones usan el búfer de estarcido para enmascarar los píxeles de una imagen. La máscara controla si el píxel se dibuja o no. A continuación se muestran algunos de los efectos más comunes.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Técnicas de búfer de estarcido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423151"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Técnicas de búfer de estarcido (Direct3D 9)

Las aplicaciones usan el búfer de estarcido para enmascarar los píxeles de una imagen. La máscara controla si el píxel se dibuja o no. A continuación se muestran algunos de los efectos más comunes.

-   [Composición](compositing.md)
-   [Marcas](decaling.md)
-   [Resuelve, atenúa y deslizar rápidamente](dissolves--fades--and-swipes.md)
-   [Contornos y siluetas](outlines-and-silhouettes.md)
-   [Galería de símbolos de dos caras](two-sided-stencil.md)

El búfer de estarcido habilita o deshabilita el dibujo en la superficie de destino de representación en píxel por píxel. En su nivel más básico, permite a las aplicaciones enmascarar las secciones de la imagen representada para que no se muestren. A menudo, las aplicaciones utilizan búferes de estarcido para efectos especiales como la resolución, la alineación y la esquematización.

La información del búfer de estarcido se incrusta en los datos del búfer z. La aplicación puede usar el método [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) para comprobar la compatibilidad con la galería de símbolos de hardware, tal como se muestra en el ejemplo de código siguiente.


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) permite elegir un dispositivo para crearlo en función de las capacidades de dicho dispositivo. En este caso, se rechazan los dispositivos que no admiten búferes de estarcido de 8 bits. Tenga en cuenta que este es solo un uso posible para **IDirect3D9:: CheckDeviceFormat**; para obtener más información [, vea determinar la compatibilidad de hardware (Direct3D 9)](determining-hardware-support.md).

## <a name="how-the-stencil-buffer-works"></a>Cómo funciona el búfer de estarcido

Direct3D realiza una prueba en el contenido del búfer de estarcido píxel a píxel. Para cada píxel de la superficie de destino, realiza una prueba usando el valor correspondiente en el búfer de la galería de símbolos, un valor de referencia de la galería de símbolos y un valor de máscara de estarcido. Si se supera la prueba, Direct3D realiza una acción. La prueba se realiza mediante los pasos siguientes.

1.  Realiza una operación and bit a bit del valor de referencia de la galería de símbolos con la máscara de la galería de símbolos.
2.  Realiza una operación and bit a bit del valor del búfer de estarcido del píxel actual con la máscara de la galería de símbolos.
3.  Compare el resultado del paso 1 con el resultado del paso 2, mediante la función de comparación.

Estos pasos se muestran en el ejemplo de código siguiente.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



es el contenido del búfer de estarcido del píxel actual. En este ejemplo de código se usa el símbolo de y comercial (&) para representar la operación and bit a bit.


```
StencilMask
```



representa el valor de la máscara de la galería de símbolos y


```
StencilRef
```



representa el valor de referencia de la galería de símbolos.


```
CompFunc
```



es la función de comparación.

El píxel actual se escribe en la superficie de destino si se supera la prueba del estarcido y se omite en caso contrario. El comportamiento de comparación predeterminado es escribir el píxel, independientemente de cómo se desactive cada operación bit a bit (D3DCMP \_ siempre). Puede cambiar este comportamiento cambiando el valor de D3DRS \_ STENCILFUNC Render State, pasando un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) para identificar la función de comparación deseada.

La aplicación puede personalizar el funcionamiento del búfer de estarcido. Puede establecer la función de comparación, la máscara de la galería de símbolos y el valor de referencia de la galería de símbolos. También puede controlar la acción que Direct3D realiza cuando la prueba de estarcido supera o produce un error. Para obtener más información, vea [cliché buffer State (Direct3D 9)](stencil-buffer-state.md).

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos de código se muestra cómo configurar el búfer de estarcido.


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



De forma predeterminada, el valor de referencia de la galería de símbolos es cero. Cualquier valor entero es válido. Direct3D realiza una operación and bit a bit del valor de referencia de la galería de símbolos y un valor de máscara de galería de símbolos antes de la prueba.

Puede controlar qué información de píxeles se escribe en función de la comparación de la galería de símbolos.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



Puede escribir su propia fórmula para el valor que desea escribir en el búfer de estarcido, tal como se muestra en el ejemplo siguiente.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
