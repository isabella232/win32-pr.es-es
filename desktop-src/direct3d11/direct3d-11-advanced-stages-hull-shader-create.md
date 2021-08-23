---
title: Cómo crear un sombreador de casco
description: En este tema se muestra cómo crear un sombreador de casco.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa9fe55a11c68e4cbc247f6509c52b6bac1d01b823d48637ee51073437316f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608995"
---
# <a name="how-to-create-a-hull-shader"></a>Cómo: Crear un sombreador de casco

Un sombreador de casco es la primera de tres fases que funcionan conjuntamente para implementar [la teselación](direct3d-11-advanced-stages-tessellation.md). Las salidas del sombreador de casco impulsan la fase del teselador, así como la fase del sombreador de dominio. En este tema se muestra cómo crear un sombreador de casco.

Un sombreador de casco transforma un conjunto de puntos de control de entrada (de un sombreador de vértices) en un conjunto de puntos de control de salida. El número de puntos de entrada y salida puede variar en el contenido y el número en función de la transformación (una transformación típica sería una transformación base).

Un sombreador de casco también genera información de constantes de revisión, como factores de teselación, para un sombreador de dominio y el teselador. La fase de teselador de función fija usa los factores de teselación, así como otro estado declarado en un sombreador de casco para determinar cuánto se debe tesentar.

**Para crear un sombreador de casco**

1.  Diseñar un sombreador de casco. Vea [Cómo: Diseñar un sombreador de casco.](direct3d-11-advanced-stages-hull-shader-design.md)
2.  Compilación del código del sombreador
3.  Cree un objeto de sombreador de casco [**mediante ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Inicialice la fase de canalización [**mediante ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Un sombreador de dominio debe enlazarse a la canalización si se enlaza un sombreador de casco. En concreto, no es válido transmitir directamente los puntos de control del sombreador de casco con el sombreador de geometría.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Introducción a la teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




