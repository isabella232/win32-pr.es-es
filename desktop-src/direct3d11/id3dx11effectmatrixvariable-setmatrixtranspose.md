---
title: Método ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Transponer y establecer una matriz de punto flotante.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Método SetMatrixTranspose Direct3D 11
- Método SetMatrixTranspose Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986934"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a>ID3DX11EffectMatrixVariable:: SetMatrixTranspose (método)

Transponer y establecer una matriz de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntero al primer elemento de una matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Transponer una matriz reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columnas (o viceversa).

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

 

 





