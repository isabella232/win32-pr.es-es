---
title: Método ID3DX11EffectMatrixVariable GetMatrixTranspose (D3dx11effect.h)
description: Transponer y obtener una matriz de punto flotante.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Método GetMatrixTranspose Direct3D 11
- Método GetMatrixTranspose Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d2f04057dac5bc432cc3c6a9a3060654d8f6d181836823aa29f0a02f82f667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046183"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a>Método ID3DX11EffectMatrixVariable::GetMatrixTranspose

Transponer y obtener una matriz de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **\* float**

Puntero al primer elemento de una matriz transpuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Si se reorganiza una matriz, se reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columna (o viceversa).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





