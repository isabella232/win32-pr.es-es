---
title: Registro float constante (referencia de HLSL VS)
description: Registro de entrada del sombreador de vértices para una constante de punto flotante de cuatro componentes. Establezca un registro constante con def - vs o SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949935"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Registro float constante (referencia de HLSL VS)

Registro de entrada del sombreador de vértices para una constante de punto flotante de cuatro componentes. Establezca un registro constante con [def - vs](def---vs.md) o [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).

El archivo de registro constante es de solo lectura desde la perspectiva del sombreador de vértices. Cualquier instrucción única solo puede tener acceso a un registro constante. Sin embargo, cada origen de esa instrucción puede deslizar y negar ese vector de forma independiente a medida que se lee.

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   Para Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx solo se limita a la ejecución de ese sombreador. Por el contrario, las constantes establecidas mediante las API SetXXXShaderConstantX inicializan constantes en el espacio global. Las constantes del espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   Para Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes, independientemente de la técnica utilizada para establecerlas.

Un registro constante se designa como absoluto o relativo:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Por lo tanto, el registro constante se puede leer mediante un índice absoluto o con un índice relativo de un registro de direcciones. Las lecturas de registros fuera del intervalo devuelven (0.0, 0.0, 0.0, 0.0).

## <a name="examples"></a>Ejemplos

Este es un ejemplo que declara dos constantes de punto flotante dentro de un sombreador.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Estas constantes se cargan cada vez que se llama a [**SetVertexShader.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)

Este es un ejemplo de uso de la API.


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



Si va a establecer valores constantes con la API, no se requiere ninguna declaración de sombreador.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro constante      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 