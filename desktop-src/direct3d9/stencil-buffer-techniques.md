---
description: Las aplicaciones usan el búfer de galería de símbolos para enmascarar píxeles en una imagen. La máscara controla si el píxel se dibuja o no. A continuación se muestran algunos de los efectos más comunes.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Técnicas de búfer de galería de símbolos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358880"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Técnicas de búfer de galería de símbolos (Direct3D 9)

Las aplicaciones usan el búfer de galería de símbolos para enmascarar píxeles en una imagen. La máscara controla si el píxel se dibuja o no. A continuación se muestran algunos de los efectos más comunes.

-   [Composición](compositing.md)
-   [Escalado](decaling.md)
-   [Efectos, desvanecimientos y deslizamientos](dissolves--fades--and-swipes.md)
-   [Contornos y sobresalciones](outlines-and-silhouettes.md)
-   [Galería de símbolos de dos lados](two-sided-stencil.md)

El búfer de galería de símbolos habilita o deshabilita el dibujo en la superficie de destino de representación en cada píxel. En su nivel más fundamental, permite a las aplicaciones enmascarar las secciones de la imagen representado para que no se muestren. A menudo, las aplicaciones usan búferes de galería de símbolos para efectos especiales, como distensión, descalización y delineación.

La información del búfer de galería de símbolos se inserta en los datos del búfer z. La aplicación puede usar el método [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) para comprobar la compatibilidad con la galería de símbolos de hardware, como se muestra en el ejemplo de código siguiente.


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



[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) permite elegir un dispositivo para crear en función de las funcionalidades de ese dispositivo. En este caso, se rechazan los dispositivos que no admiten búferes de galería de símbolos de 8 bits. Tenga en cuenta que este es solo un uso posible **para IDirect3D9::CheckDeviceFormat**; Para obtener más información, [vea Determinar la compatibilidad con hardware (Direct3D 9).](determining-hardware-support.md)

## <a name="how-the-stencil-buffer-works"></a>Funcionamiento del búfer de galería de símbolos

Direct3D realiza una prueba en el contenido del búfer de la galería de símbolos de forma píxel a píxel. Para cada píxel de la superficie de destino, realiza una prueba con el valor correspondiente en el búfer de la galería de símbolos, un valor de referencia de galería de símbolos y un valor de máscara de galería de símbolos. Si la prueba se supera, Direct3D realiza una acción. La prueba se realiza mediante los pasos siguientes.

1.  Realice una operación AND bit a bit del valor de referencia de la galería de símbolos con la máscara de galería de símbolos.
2.  Realice una operación AND bit a bit del valor del búfer de la galería de símbolos para el píxel actual con la máscara de galería de símbolos.
3.  Compare el resultado del paso 1 con el resultado del paso 2, mediante la función de comparación.

Estos pasos se muestran en el ejemplo de código siguiente.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



es el contenido del búfer de galería de símbolos para el píxel actual. En este ejemplo de código se usa el símbolo de y comercial (&) para representar la operación AND bit a bit.


```
StencilMask
```



representa el valor de la máscara de galería de símbolos y


```
StencilRef
```



representa el valor de referencia de la galería de símbolos.


```
CompFunc
```



es la función de comparación.

El píxel actual se escribe en la superficie de destino si se supera la prueba de galería de símbolos y, en caso contrario, se omite. El comportamiento de comparación predeterminado es escribir el píxel, independientemente de cómo salga cada operación bit a bit (D3DCMP \_ ALWAYS). Puede cambiar este comportamiento cambiando el valor del estado de representación D3DRS STENCILFUNC, pasando un miembro del tipo enumerado \_ [**D3DCMPFUNC**](./d3dcmpfunc.md) para identificar la función de comparación deseada.

La aplicación puede personalizar el funcionamiento del búfer de galería de símbolos. Puede establecer la función de comparación, la máscara de galería de símbolos y el valor de referencia de la galería de símbolos. También puede controlar la acción que Realiza Direct3D cuando la prueba de galería de símbolos se supera o produce un error. Para obtener más información, vea Estado del búfer de galería [de símbolos (Direct3D 9).](stencil-buffer-state.md)

## <a name="examples"></a>Ejemplos

En los ejemplos de código siguientes se muestra cómo configurar el búfer de galería de símbolos.


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



De forma predeterminada, el valor de referencia de la galería de símbolos es cero. Cualquier valor entero es válido. Direct3D realiza un AND bit a bit del valor de referencia de la galería de símbolos y un valor de máscara de galería de símbolos antes de la prueba de galería de símbolos.

Puede controlar qué información de píxeles se escribe en función de la comparación de galería de símbolos.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



Puede escribir su propia fórmula para el valor que desea escribir en el búfer de la galería de símbolos, como se muestra en el ejemplo siguiente.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
