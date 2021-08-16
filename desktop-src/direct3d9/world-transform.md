---
description: La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación mundial.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: World Transform (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbddefbaa5ad4bd41e7dafa79e086605d8f40e761cca2bd6ce9b9c0b212950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518913"
---
# <a name="world-transform-direct3d-9"></a>World Transform (Direct3D 9)

La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación mundial.

## <a name="what-is-a-world-transform"></a>¿Qué es una transformación mundial?

Una transformación del mundo cambia las coordenadas del espacio del modelo, donde los vértices se definen en relación con el origen local de un modelo, al espacio mundial, donde los vértices se definen en relación con un origen común a todos los objetos de una escena. Básicamente, la transformación del mundo coloca un modelo en el mundo; por lo tanto, su nombre. En el diagrama siguiente se muestra la relación entre el sistema de coordenadas mundial y el sistema de coordenadas local de un modelo.

![diagrama de cómo se relacionan las coordenadas globales y las coordenadas locales](images/worldcrd.png)

La transformación mundial puede incluir cualquier combinación de traducciones, rotaciones y escalas.

## <a name="setting-up-a-world-matrix"></a>Configuración de una matriz mundial

Como con cualquier otra transformación, cree la transformación del mundo concatenando una serie de matrices en una sola matriz que contenga la suma total de sus efectos. En el caso más sencillo, cuando un modelo está en el origen mundial y sus ejes de coordenadas locales están orientados al mismo que el espacio mundial, la matriz del mundo es la matriz de identidad. Más comúnmente, la matriz mundial es una combinación de una traducción al espacio mundial y, posiblemente, una o varias rotaciones para convertir el modelo según sea necesario.

En el ejemplo siguiente, de una clase de modelo 3D ficticia escrita en C++, se usan las funciones auxiliares incluidas en la biblioteca de utilidades D3DX para crear una matriz mundial que incluye tres rotaciones para orientar un modelo y una traducción para reubicarlos en relación con su posición en el espacio mundial.


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



Después de preparar la matriz mundial, llame al método [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) para establecerla y especifique la macro [**D3DTS \_ WORLD**](d3dts-world.md) para el primer parámetro.

> [!Note]  
> Direct3D usa el mundo y las matrices de vistas que se establecen para configurar varias estructuras de datos internas. Cada vez que se establece una nueva matriz de mundo o vista, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia (por ejemplo, miles de veces por fotograma) lleva mucho tiempo. Puede minimizar el número de cálculos necesarios concatenando el mundo y ver matrices en una matriz de vista mundial que estableció como matriz de mundo y, a continuación, estableciendo la matriz de vistas en la identidad. Mantenga copias almacenadas en caché de mundos individuales y vea matrices para poder modificar, concatenar y restablecer la matriz mundial según sea necesario. Para mayor claridad, en esta documentación, los ejemplos de Direct3D rara vez emplean esta optimización.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 



