---
title: Función UpdateSubresources (asignación de montón) (D3dx12.h)
description: Actualiza los subrecursos con una implementación de asignación de montón.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072857"
---
# <a name="updatesubresources-heap-allocating-function"></a>Función UpdateSubresources (asignación de montón)

Actualiza los subrecursos con una implementación de asignación de montón.

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

*pCmdList* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Puntero a la [**interfaz ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) de la lista de comandos.

</dd> <dt>

*pDestinationResource* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntero a la [**interfaz ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso de destino.

</dd> <dt>

*pIntermediate* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntero a la [**interfaz ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso intermedio.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Desplazamiento, en bytes, al recurso intermedio.

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

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntero a una matriz (de longitud *NumSubresources)* de punteros a estructuras [**\_ SUBRESOURCE \_ DATA de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de subrecursos usados para la actualización.

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

 

