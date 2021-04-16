---
title: Función GetRequiredIntermediateSize (D3dx12. h)
description: Devuelve el tamaño necesario de un búfer que se va a utilizar para la carga de datos.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize función)
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649429"
---
# <a name="getrequiredintermediatesize-function"></a>GetRequiredIntermediateSize función)

Devuelve el tamaño necesario de un búfer que se va a utilizar para la carga de datos.

## <a name="syntax"></a>Sintaxis


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestinationResource* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntero a la interfaz [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso de destino.

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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Tamaño del búfer, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

