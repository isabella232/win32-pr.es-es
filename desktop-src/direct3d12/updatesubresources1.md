---
title: Función UpdateSubresources (D3dx12. h)
description: Actualiza los Subrecursos, se deben rellenar todas las matrices de Subrecursos, normalmente llamando a ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708083"
---
# <a name="updatesubresources-function"></a>UpdateSubresources función)

Actualiza los Subrecursos, se deben rellenar todas las matrices de Subrecursos, normalmente mediante una llamada a [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Sintaxis


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
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

*FirstSubresource* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice del primer subrecurso del recurso. El intervalo de valores válidos es de 0 a D3D12 \_ req \_ subsources.

</dd> <dt>

*NumSubresources* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El número de Subrecursos del recurso. El intervalo de valores válidos es de 0 a (D3D12 \_ req \_ subsources- *FirstSubresource*).

</dd> <dt>

*RequiredSize* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño necesario, en bytes, para la actualización.

</dd> <dt>

*emisiones* \[ de\]
</dt> <dd>

Tipo: **\* const [**D3D12 \_ colocada \_ \_ superficie de Subrecursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**

Puntero a una matriz (de longitud *NumSubresources*) de punteros a las estructuras que contiene la descripción y la ubicación de los Subrecursos del recurso.

</dd> <dt>

*pNumRows* \[ de\]
</dt> <dd>

Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***

Puntero a una matriz (de longitud *NumSubresources*) de los uint que contienen el número de filas de cada subrecurso.

</dd> <dt>

*pRowSizesInBytes* \[ de\]
</dt> <dd>

Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Puntero a una matriz (de longitud *NumSubresources*) de los uint que contiene el tamaño, en bytes, de cada fila.

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **\* [**datos de \_ subrecurso \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) const**

Puntero a una matriz (de longitud *NumSubresources*) de punteros a estructuras de [**\_ \_ datos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de los Subrecursos utilizados para la actualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño del búfer en bytes.

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

 

