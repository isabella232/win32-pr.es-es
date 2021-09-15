---
description: 'Función D3DXSHPRTCompSplitMeshSC: se usa con los resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia precalutada (PRT).'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Función D3DXSHPRTCompSplitMeshSC (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567160"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>Función D3DXSHPRTCompSplitMeshSC

Se usa con resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia precalutada (PRT). Después de llamar a [**D3DXSHPRTCompSuperCluster,**](d3dxshprtcompsupercluster.md) esta función se puede usar para dividir la malla en un grupo de caras o vértices por superclúster. Cada superc cluster contiene todas las caras que contienen cualquier vértice clasificado en uno de sus clústeres. Todos los vértices conectados a este conjunto de caras también se incluyen con la matriz ppVertStatus devuelta que indica si el vértice pertenece o no al super clúster.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClusterIDs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

*Los IDs de clúster NumVertices* (extraídos de un búfer comprimido).

</dd> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices en la malla original.

</dd> <dt>

*NumCs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de clústeres (parámetro de entrada a compresión).

</dd> <dt>

*pSClusterIDs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matriz de *numcs de tamaño* que contendrá los valores de supercrones de clúster.

</dd> <dt>

*NumSCs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de superclústeres asignados en [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Búfer de índice sin procesar para mesh. El formato depende de *InputIBIs32Bit.*

</dd> <dt>

*InputIBIs32Bit* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** el búfer de índice se establece en 32 bits; de lo contrario, 16 bits.

</dd> <dt>

*NumFaces* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de caras de la malla original *(pInputIB* es tres veces esta longitud).

</dd> <dt>

*ppIBData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer de índice sin formato que contendrá las caras divididas resultantes. Formato determinado por *InputIBIs32Bit.* Asignado por función.

</dd> <dt>

*pIBDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Longitud de *ppIBData*, asignada en la función .

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** asigna una matriz de enteros sin signo; de lo contrario, asigna una matriz corta sin signo.

</dd> <dt>

*ppFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Asignación de cada cara de *ppIBData* a caras originales. La longitud \* *es pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nueva estructura de datos de vértices. Tamaño de *pVertDataLength.*

</dd> <dt>

*pVertDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Número de nuevos vértices en malla dividida. Se asigna en la función .

</dd> <dt>

*pSCClusterList* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matriz de *numcs* de longitud en la que *pSCData* indexa *(campos pClusterIDs)* para cada superclúster, contiene clústeres \* ordenados por superclúster.

</dd> <dt>

*pSCData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Estructura por superc cluster. Contiene índices en *ppIBData,* *pSCClusterList* y *ppVertData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
