---
title: Método ID3DX11EffectScalarVariable SetInt (D3dx11effect.h)
description: Establezca una variable de entero.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- Método SetInt Direct3D 11
- Método SetInt Direct3D 11, interfaz ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , SetInt (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 215083d35bfbdd67cd970bfe31b81a1e19594b2bf849e1c19692fa96af257036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377545"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>Método ID3DX11EffectScalarVariable::SetInt

Establezca una variable de entero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Puntero a la variable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

