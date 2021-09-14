---
title: Método ID3DX11EffectScalarVariable SetBoolArray (D3dx11effect.h)
description: Establezca una matriz de variables booleanas.
ms.assetid: 861634a2-547d-497b-b575-bbe6151ade25
keywords:
- Método SetBoolArray Direct3D 11
- Método SetBoolArray Direct3D 11, interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método SetBoolArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e982e2475fe20a2aa12bef9c52095eed228bf44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242253"
---
# <a name="id3dx11effectscalarvariablesetboolarray-method"></a>Método ID3DX11EffectScalarVariable::SetBoolArray

Establezca una matriz de variables booleanas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

Puntero al inicio de los datos que se establecerán.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Debe establecerse en 0; se reserva para su uso futuro.

</dd> <dt>

*Recuento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de matriz que se establecerán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

