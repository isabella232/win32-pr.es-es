---
title: Método ID3DX11EffectScalarVariable GetInt (D3dx11effect.h)
description: Obtiene una variable de entero.
ms.assetid: 82a5a7a5-17cb-4e5e-ae4e-57c0ff9757c5
keywords:
- Método GetInt Direct3D 11
- Método GetInt Direct3D 11 , interfaz ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , GetInt (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b7b74ce68c9258b221db8915618b318a0ff92f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160472"
---
# <a name="id3dx11effectscalarvariablegetint-method"></a>Método ID3DX11EffectScalarVariable::GetInt

Obtiene una variable de entero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInt(
   int *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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

 

