---
title: Cómo crear un sombreador de dominios
description: En este tema se muestra cómo crear un sombreador de dominios.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075247"
---
# <a name="how-to-create-a-domain-shader"></a>Cómo: crear un sombreador de dominios

Un sombreador de dominios es el tercero de tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md). Las entradas de la fase del sombreador de dominios proceden de un sombreador de casco. En este tema se muestra cómo crear un sombreador de dominios.

Un sombreador de dominio transforma la geometría de la superficie (creada por la fase del teselador de la función fija) mediante los puntos de control de salida del sombreador de casco, la revisión de salida del sombreador de casco-datos constantes y un único conjunto de coordenadas del teselador UV.

**Para crear un sombreador de dominios**

1.  Diseñar un sombreador de dominios. Vea [Cómo: diseñar un sombreador de dominios](direct3d-11-advanced-stages-domain-shader-design.md).
2.  Compile el código del sombreador.
3.  Cree un objeto de sombreador de dominio mediante [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Inicialice la fase de canalización con [**ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 




