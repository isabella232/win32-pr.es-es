---
description: 'Método ID3DX10Mesh::Optimize: genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: Método ID3DX10Mesh::Optimize (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41bc7b4ac7fb263073a88cd998190b0fa6e044d528f9d3f4613c3284f28c0f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302580"
---
# <a name="id3dx10meshoptimize-method"></a>Método ID3DX10Mesh::Optimize

Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifica el tipo de optimización que se debe realizar. Este parámetro se puede establecer en una combinación de una o varias marcas de D3DXMESHOPT y D3DXMESH (excepto D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY y D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matriz de UINT, una por cara, que identifica la cara de malla original que corresponde a cada cara de la malla optimizada. Si el valor proporcionado para este argumento es **NULL,** no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Dirección de un puntero a una interfaz [**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contiene un DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices antiguos. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Este método genera una nueva malla. Antes de ejecutar Optimize, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). El búfer de adyacencia contiene datos de adyacencia, como una lista de bordes y las caras adyacentes entre sí.

Este método es muy similar al método [**ID3DX10Mesh::CloneMesh,**](id3dx10mesh-clonemesh.md) salvo que puede realizar la optimización al generar el nuevo clon de la malla. La malla de salida hereda todos los parámetros de creación de la malla de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
