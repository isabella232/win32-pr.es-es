---
title: Función UpdateSubresources (asignación de pila) (D3dx12.h)
description: Actualiza los subrecursos con una implementación de asignación de pila.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 43ffe9dd9e519b402126976db8ceaf1aba32f6d36a73745c951bb6a8db52a7fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300450"
---
# <a name="updatesubresources-stack-allocating-function"></a>Función UpdateSubresources (asignación de pila)

Actualiza los subrecursos con una implementación de asignación de pila.

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

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Desplazamiento, en bytes, al recurso intermedio.

</dd> <dt>

*FirstSubresource* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice del primer subrecurso del recurso. Los valores válidos van de 0 *a MaxSubresources.*

</dd> <dt>

*NumSubresources* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de subrecursos del recurso. Los valores válidos van de 1 a (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Puntero a una matriz (de longitud *NumSubresources)* de punteros a estructuras [**\_ SUBRESOURCE \_ DATA de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contienen descripciones de los datos de subrecursos usados para la actualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño del búfer en bytes.

## <a name="remarks"></a>Comentarios

La declaración de esta función comienza por: `template <UINT MaxSubresources>`

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

 

