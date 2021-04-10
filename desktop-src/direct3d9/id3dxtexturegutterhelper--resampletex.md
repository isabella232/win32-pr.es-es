---
description: Remuestrea una textura en la parametrización de esta gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper:: ResampleTex (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280438"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>ID3DXTextureGutterHelper:: ResampleTex (método)

Remuestrea una textura en la parametrización de esta gutterhelper.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTextureIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura que corresponde a la parametrización original en pMeshIn. Esta textura se usará para crear pTextureOut.

</dd> <dt>

*pMeshIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla que contiene las parametrizaciones originales y nuevas. Es necesario almacenar la nueva parametrización en el \_ índice 0 de D3DDECLUSAGE TEXCOORD.

</dd> <dt>

*Uso* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Uso de datos de vértices (se usa en combinación con UsageIndex), que identifica el componente de la declaración de vértice que contiene la parametrización original en pMeshIn. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base cero (utilizado en combinación con uso), que identifica el componente de la declaración de vértice que contiene la parametrización original en pMeshIn. La combinación de D3DDECLUSAGE \_ TEXCOORD y index 0 es necesaria para la nueva parametrización; se puede usar cualquier combinación de uso/Índice.

</dd> <dt>

*pTextureOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textura remuestreada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Una parametrización en el caso de esta función es un conjunto de coordenadas de textura que asigna los triángulos de una malla a los triángulos de una textura. La nueva parametrización es el conjunto de coordenadas de textura contenidas en la interfaz auxiliar de medianil y la parametrización original es el conjunto de coordenadas de textura que contiene la malla de entrada.

Se supone que las coordenadas de textura están entre 0 y 1, ambos inclusive, y la nueva parametrización debe declararse en la declaración de vértices como índice de coordenadas de textura 0. La textura original y la textura remuestreada deben tener el mismo ancho y alto.

Por ejemplo, para prepararse para volver a muestrear una textura:

-   Cree la interfaz de textura original (pOriginalTex a continuación) mediante una función como [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Cree la nueva interfaz de textura para la textura remuestreada (pResampledTex a continuación). El tamaño de esta textura debe coincidir con el tamaño (ancho y alto) de la textura de la aplicación auxiliar de medianil.
-   Llame a [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) para obtener la nueva parametrización como se muestra aquí:


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Un escenario común podría ser usar UVAtlas para crear un Atlas de textura y, después, usar ResampleTex para volver a muestrear la textura en la nueva parametrización. Para obtener más información sobre Atlases, vea [uso de UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
