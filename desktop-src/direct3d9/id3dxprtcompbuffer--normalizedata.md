---
description: Normaliza todos los pesos de análisis de componentes principales (PCA) para que estén entre -1 y 1. Los vectores de base se modifican para reflejar esta normalización.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: Método ID3DXPRTCompBuffer::NormalizeData (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565837"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a>Método ID3DXPRTCompBuffer::NormalizeData

Normaliza todos los pesos de análisis de componentes principales (PCA) para que estén entre -1 y 1. Los vectores de base se modifican para reflejar esta normalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




