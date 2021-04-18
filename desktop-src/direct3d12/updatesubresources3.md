---
title: Función UpdateSubresources (asignación de la pila) (D3dx12. h)
description: Actualiza Subrecursos con una implementación de asignación de pila.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
keywords:
- UpdateSubresources función)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707805"
---
# <a name="updatesubresources-stack-allocating-function"></a>Función UpdateSubresources (asignación de pila)

Actualiza Subrecursos con una implementación de asignación de pila.

## <a name="syntax"></a>Sintaxis


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCmdList* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

La lista de comandos, como un puntero a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pDestinationResource* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

El recurso de destino, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pIntermediate* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

El recurso intermedio, como un puntero a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Desplazamiento, en bytes, al recurso intermedio.

</dd> <dt>

*FirstSubresource* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice del primer subrecurso del recurso. Los valores válidos oscilan entre 0 y *MaxSubresources*.

</dd> <dt>

*NumSubresources* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El número de Subrecursos del recurso. Los valores válidos van de 1 a (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntero a una matriz (de longitud *NumSubresources*) de punteros a estructuras de [**\_ \_ datos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de los Subrecursos utilizados para la actualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño del búfer en bytes.

## <a name="remarks"></a>Observaciones

La declaración de esta función comienza por: `template <UINT MaxSubresources>`

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Subrecursos](subresources.md)
</dt> </dl>

 

