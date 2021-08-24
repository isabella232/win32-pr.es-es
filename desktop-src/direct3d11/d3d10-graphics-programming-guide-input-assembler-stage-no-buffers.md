---
title: Uso de la Input-Assembler sin búferes
description: No es necesario crear y enlazar búferes si los sombreadores no requieren búferes. Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un solo triángulo.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bccbdb059e58efbef9e6c80eacbd9af5eb8a24045bdaab20bf540c13a9b719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752545"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a>Uso de la Input-Assembler sin búferes

No es necesario crear y enlazar búferes si los sombreadores no requieren búferes. Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un solo triángulo.

-   [Sombreador de vértices](#vertex-shader)
-   [Sombreador de píxeles](#pixel-shader)
-   [Técnica](#technique)
-   [Código de aplicación](#application-code)
-   [Temas relacionados](#related-topics)

## <a name="vertex-shader"></a>Sombreador de vértices

Por ejemplo, podría declarar un sombreador de vértices que cree sus propios vértices.


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a>Sombreador de píxeles


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a>Técnica

Una técnica es una colección de pases de representación (debe haber al menos un paso).


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a>Código de aplicación


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con la fase Input-Assembler de trabajo](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




