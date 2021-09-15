---
description: La siguiente estructura definida por el usuario se puede usar para los vértices que se combinarán entre dos matrices.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Uso de geometry blending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473237"
---
# <a name="using-geometry-blending-direct3d-9"></a>Uso de geometry blending (Direct3D 9)

La siguiente estructura definida por el usuario se puede usar para los vértices que se combinarán entre dos matrices.


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



El peso de mezcla debe aparecer después de la posición y los datos RHW en la FVF y antes de la normal del vértice.

Observe que el formato de vértice anterior solo contiene un valor de peso de mezcla. Esto se debe a que habrá dos matrices de mundo, definidas en los estados de transformación [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) y **D3DTS \_ WORLDMATRIX**(1). El sistema mezcla cada vértice entre estas dos matrices mediante el valor de peso único. Para tres matrices, solo se requieren dos pesos, y así sucesivamente.

> [!Note]
>
> La definición de los pesos de la máscara es fácil. El uso de una función lineal de la distancia entre las uniones es un buen inicio, pero una función sigmoid más suave se ve mejor. La elección de una función de distribución del peso de la máscara puede dar lugar a creaciones nítidas en las uniones, si se desea, mediante una gran variación en el peso de la máscara a corta distancia.

 

## <a name="setting-blending-matrices"></a>Establecer matrices de mezcla

Las matrices de transformación entre las que se combina el sistema se establecen mediante una llamada [**al método IDirect3DDevice9::SetTransform.**](/windows/desktop/api) Establezca el primer parámetro en un valor definido por la macro [**\_ WORLDMATRIX de D3DTS**](d3dts-worldmatrix.md) y establezca el segundo parámetro en la dirección de la matriz que se va a establecer.

En el siguiente ejemplo de código de C++ se establecen dos matrices de mundo, entre las que la geometría se combina para crear la sensación de un arm combinado.


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



Establecer una matriz de mezcla simplemente hace que el sistema almacena en caché la matriz para su uso posterior; no indica al sistema que empiece a mezclar vértices.

## <a name="enabling-geometry-blending"></a>Habilitación de la combinación de geometría

La combinación de geometría está deshabilitada de forma predeterminada. Para habilitar la combinación de geometría, llame al método [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) para establecer el estado de representación de D3DRS VERTEXBLEND en un valor del tipo enumerado \_ [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) En el ejemplo de código siguiente se muestra el aspecto que podría tener esta llamada al establecer el estado de representación de una mezcla entre dos matrices de mundo.


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



Cuando D3DRS VERTEXBLEND se establece en cualquier valor distinto de \_ D3DVBF DISABLE, el sistema asume que el número adecuado de pesos de mezcla se incluirá en el formato de \_ vértice. Es su responsabilidad proporcionar un formato de vértice compatible y proporcionar una descripción adecuada de ese formato a los métodos de representación de Direct3D.

Cuando se habilita, el sistema realiza la combinación de geometría para todos los objetos representados por los métodos de representación DrawPrimitive.

## <a name="see-also"></a>Consulte también

[Códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de geometría](geometry-blending.md)
</dt> </dl>

 

 
