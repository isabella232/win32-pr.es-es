---
title: Función UpdateSubresources (D3dx12.h)
description: Actualiza los subrecursos; todas las matrices de subrecursos deben rellenarse, normalmente llamando a ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- Función UpdateSubresources
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072856"
---
# <a name="updatesubresources-function"></a>Función UpdateSubresources

Actualiza los subrecursos; todas las matrices de subrecursos deben rellenarse, normalmente llamando a [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

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

*pCmdList* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Lista de comandos, como puntero a [**id3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

</dd> <dt>

*pDestinationResource* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Recurso de destino, como puntero a [**id3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*pIntermediate* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Recurso intermedio, como puntero a [**id3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*FirstSubresource* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice del primer subrecurso del recurso. El intervalo de valores válidos es de 0 a D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de subrecursos del recurso. El intervalo de valores válidos es de 0 a (D3D12 \_ REQ \_ SUBRESOURCES - *FirstSubresource*).

</dd> <dt>

*RequiredSize* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño necesario, en bytes, para la actualización.

</dd> <dt>

*pLayouts* \[ En\]
</dt> <dd>

Tipo: **const [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \***

Puntero a una matriz (de longitud *NumSubresources)* de punteros a las estructuras que contiene la descripción y la ubicación de los subrecursos del recurso.

</dd> <dt>

*pNumRows* \[ En\]
</dt> <dd>

Tipo: **const [**UINT**](/windows/desktop/WinProg/windows-data-types) \***

Puntero a una matriz (de longitud *NumSubresources)* de UINTS que contiene el número de filas para cada subrecurso.

</dd> <dt>

*pRowSizesInBytes* \[ En\]
</dt> <dd>

Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Puntero a una matriz (de longitud *NumSubresources)* de UINTS que contiene el tamaño, en bytes, de cada fila.

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Puntero a una matriz (de longitud *NumSubresources)* de punteros a estructuras [**\_ SUBRESOURCE \_ DATA D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de subrecursos usados para la actualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño del búfer en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Subrecursos](subresources.md)
</dt> </dl>

 

