---
description: La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación universal.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformación universal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422795"
---
# <a name="world-transform-direct3d-9"></a>Transformación universal (Direct3D 9)

La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación universal.

## <a name="what-is-a-world-transform"></a>¿Qué es una transformación mundial?

Una transformación de mundo cambia las coordenadas del espacio del modelo, donde los vértices se definen en relación con el origen local de un modelo, en el espacio universal, donde se definen los vértices en relación con un origen común a todos los objetos de una escena. En esencia, la transformación mundial coloca un modelo en el mundo; por lo tanto, su nombre. En el diagrama siguiente se muestra la relación entre el sistema de coordenadas universal y el sistema de coordenadas local de un modelo.

![diagrama de cómo se relacionan las coordenadas del mundo y las coordenadas locales](images/worldcrd.png)

La transformación del mundo puede incluir cualquier combinación de traducciones, giros y escalado.

## <a name="setting-up-a-world-matrix"></a>Configuración de una matriz mundial

Como con cualquier otra transformación, cree la transformación universal mediante la concatenación de una serie de matrices en una matriz única que contenga la suma total de sus efectos. En el caso más simple, cuando un modelo está en el origen del mundo y sus ejes de coordenadas locales están orientados igual que el espacio del mundo, la matriz mundial es la matriz de identidad. Normalmente, la matriz mundial es una combinación de una traducción en el espacio universal y, posiblemente, una o más rotaciones para convertir el modelo según sea necesario.

En el ejemplo siguiente, de una clase de modelo 3D ficticia escrita en C++, se usan las funciones auxiliares incluidas en la biblioteca de utilidades de D3DX para crear una matriz universal que incluye tres giros para orientar un modelo y una traslación para reubicarlo en relación con su posición en el espacio universal.


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



Después de preparar la matriz universal, llame al método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) para establecerla, especificando la macro [**D3DTS \_ World**](d3dts-world.md) para el primer parámetro.

> [!Note]  
> Direct3D usa el mundo y las matrices de vistas que se establecen para configurar varias estructuras de datos internas. Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia (por ejemplo, miles de veces por fotograma) es un proceso que consume mucho tiempo. Puede minimizar el número de cálculos necesarios concatenando el mundo y ver las matrices en una matriz de vista mundial que establezca como la matriz universal y, a continuación, estableciendo la matriz de la vista en la identidad. Mantenga copias en caché de matrices de todo el mundo y vistas para que pueda modificar, concatenar y restablecer la matriz universal según sea necesario. Para mayor claridad, en esta documentación los ejemplos de Direct3D raramente emplean esta optimización.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 



