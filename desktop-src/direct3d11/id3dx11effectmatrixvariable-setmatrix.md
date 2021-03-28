---
title: Método ID3DX11EffectMatrixVariable SetMatrix (D3dx11effect. h)
description: Establezca una matriz de punto flotante.
ms.assetid: 91c69bc0-c8c6-4232-8c70-801ac8ddbcda
keywords:
- Método SetMatrix Direct3D 11
- Método SetMatrix Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af7b64e7391461efc47b6f65ca676b870174347
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987048"
---
# <a name="id3dx11effectmatrixvariablesetmatrix-method"></a>ID3DX11EffectMatrixVariable:: SetMatrix (método)

Establezca una matriz de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrix(
   float *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntero al primer elemento de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





