---
title: Creación de un sombreador de casco
description: En este tema se muestra cómo crear un sombreador de casco.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773717"
---
# <a name="how-to-create-a-hull-shader"></a>Cómo: crear un sombreador de casco

Un sombreador de casco es la primera de las tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md). La salida del sombreador de casco controla la fase de del teselador, así como la fase del sombreador del dominio. En este tema se muestra cómo crear un sombreador de casco.

Un sombreador de casco transforma un conjunto de puntos de control de entrada (de un sombreador de vértices) en un conjunto de puntos de control de salida. El número de puntos de entrada y salida puede variar en el contenido y el número dependiendo de la transformación (una transformación típica sería una transformación de base).

Un sombreador de casco también genera información de constantes de revisión, como factores de teselación, para un sombreador de dominio y del teselador. La fase del teselador de función fija usa los factores de teselación, así como otro estado declarado en un sombreador de casco para determinar cuánto dividirlas.

**Para crear un sombreador de casco**

1.  Diseñar un sombreador de casco. Vea [Cómo: diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Compilar el código del sombreador
3.  Cree un objeto de sombreador de casco mediante [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Inicialice la fase de canalización mediante [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Un sombreador de dominio debe estar enlazado a la canalización si un sombreador de casco está enlazado. En concreto, no es válido transmitir directamente los puntos de control del sombreador de casco con el sombreador de geometría.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Información general sobre teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




