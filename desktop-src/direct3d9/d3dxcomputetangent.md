---
description: Calcula los vectores tangentes para las coordenadas de textura especificadas en la fase de textura. Proporcionado para admitir aplicaciones heredadas. Use D3DXComputeTangentFrameEx para obtener mejores resultados.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Función D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717745"
---
# <a name="d3dxcomputetangent-function"></a>D3DXComputeTangent función)

Calcula los vectores tangentes para las coordenadas de textura especificadas en la fase de textura. Proporcionado para admitir aplicaciones heredadas. Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obtener mejores resultados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Malla* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de entrada.

</dd> <dt>

*TexStageIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que representa la fase de textura.

</dd> <dt>

*TangentIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que proporciona el índice de uso de los datos de tangente. La declaración de vértices implica el uso; Este índice modifica el uso con el índice de uso. Para obtener más información sobre una declaración de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*BinormIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que proporciona el índice de uso de los datos binormales. La declaración de vértices implica el uso; Este índice modifica el uso con el índice de uso. Para obtener más información sobre una declaración de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Ajustar* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Establezca este valor en 0 para ningún ajuste, o en 1 para el ajuste en las direcciones de e.

</dd> <dt>

*pAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que se va a rellenar con índices de caras adyacentes. El número de bytes de esta matriz debe ser al menos ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Si la declaración del vértice de la malla especifica campos de tangente o binormalización, **D3DXComputeTangent** actualizará los datos de tangente o binormales proporcionados por el usuario. Como alternativa, establezca TangentIndex en [d3dx de \_ forma predeterminada](other-d3dx-constants.md) para no actualizar los datos de tangente proporcionados por el usuario o establezca BinormIndex en d3dx de \_ forma predeterminada para que no actualice los datos binormales proporcionados por el usuario. TexStageIndex no se puede establecer en el \_ valor predeterminado de D3DX.

**D3DXComputeTangent** depende de la declaración del vértice de la malla que contenga el campo binormal (BinormIndex), el campo tangente (TangentIndex) o ambos. Si faltan ambos, se producirá un error en esta función.

Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
