---
title: Método ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Obtiene una matriz de matrices.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Método GetMatrixArray Direct3D 11
- Método GetMatrixArray Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003880"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a>ID3DX11EffectMatrixVariable:: GetMatrixArray (método)

Obtiene una matriz de matrices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntero al primer elemento de la primera matriz de una matriz de matrices.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Desplazamiento (en número de matrices) entre el inicio de la matriz y la primera matriz devuelta.

</dd> <dt>

*Recuento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de matrices de la matriz devuelta.

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

 

