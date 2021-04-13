---
description: Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Método ID3DX10Mesh:: Optimize (D3DX10. h)'
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
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362654"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh:: Optimize (método)

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

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica el tipo de optimización que se va a realizar. Este parámetro se puede establecer en una combinación de una o varias marcas de D3DXMESHOPT y D3DXMESH (excepto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WRITEONLY y D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matriz de UINT, uno por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla optimizada. Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Dirección de un puntero a una [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Este método genera una nueva malla. Antes de ejecutar optimizar, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). El búfer de adyacencia contiene datos de adyacencias, como una lista de bordes y las caras adyacentes entre sí.

Este método es muy similar al método [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , salvo que puede realizar la optimización mientras genera el nuevo clon de la malla. La malla de salida hereda todos los parámetros de creación de la malla de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
