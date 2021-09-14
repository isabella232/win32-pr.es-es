---
title: Método ID3DX11EffectScalarVariable SetBool (D3dx11effect.h)
description: Establezca una variable booleana.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- Método SetBool Direct3D 11
- Método SetBool Direct3D 11, interfaz ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , SetBool method
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172509"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a>Método ID3DX11EffectScalarVariable::SetBool

Establezca una variable booleana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* 
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Puntero a la variable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

