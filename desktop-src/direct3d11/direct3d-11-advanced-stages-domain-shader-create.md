---
title: Cómo crear un sombreador de dominio
description: En este tema se muestra cómo crear un sombreador de dominio.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e76c581062460f7ec9d232e3594d88a4dd2bd4a346ccc30a373917671ffafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566225"
---
# <a name="how-to-create-a-domain-shader"></a>Cómo: Crear un sombreador de dominio

Un sombreador de dominio es la tercera de las tres fases que funcionan conjuntamente para implementar [la teselación](direct3d-11-advanced-stages-tessellation.md). Las entradas de la fase de sombreador de dominio proceden de un sombreador de casco. En este tema se muestra cómo crear un sombreador de dominio.

Un sombreador de dominio transforma la geometría de la superficie (creada por la fase tessellator de función fija) mediante puntos de control de salida del sombreador de casco, datos de revisión constante de salida del sombreador de casco y un único conjunto de coordenadas uv del teselador.

**Para crear un sombreador de dominio**

1.  Diseñar un sombreador de dominio. Vea [Cómo: Diseñar un sombreador de dominio.](direct3d-11-advanced-stages-domain-shader-design.md)
2.  Compile el código del sombreador.
3.  Cree un objeto de sombreador de dominio [**mediante ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Inicialice la fase de canalización [**mediante ID3D11DeviceContext::D SSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 




