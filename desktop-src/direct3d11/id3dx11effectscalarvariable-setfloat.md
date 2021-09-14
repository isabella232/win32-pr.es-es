---
title: Método ID3DX11EffectScalarVariable SetFloat (D3dx11effect.h)
description: Establezca una variable de punto flotante.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- Método SetFloat Direct3D 11
- Método SetFloat Direct3D 11, interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método SetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad3c3e9f020e5094cd03f7b25ee907dcc6e2c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172506"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a>Método ID3DX11EffectScalarVariable::SetFloat

Establezca una variable de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* 
</dt> <dd>

Tipo: **float**

Puntero a la variable.

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

 

 





