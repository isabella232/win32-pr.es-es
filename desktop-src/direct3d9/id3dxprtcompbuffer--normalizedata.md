---
description: Normaliza todos los pesos del análisis de componentes principales (PCA) para que estén entre-1 y 1. Los vectores de base se modifican para reflejar esta normalización.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'ID3DXPRTCompBuffer:: NormalizeData (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718453"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a>ID3DXPRTCompBuffer:: NormalizeData (método)

Normaliza todos los pesos del análisis de componentes principales (PCA) para que estén entre-1 y 1. Los vectores de base se modifican para reflejar esta normalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




