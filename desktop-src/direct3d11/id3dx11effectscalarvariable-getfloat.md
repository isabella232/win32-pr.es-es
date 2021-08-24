---
title: Método ID3DX11EffectScalarVariable GetFloat (D3dx11effect.h)
description: Obtiene una variable de punto flotante.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Método GetFloat Direct3D 11
- Método GetFloat Direct3D 11 , interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f00e5f4863b54a208b1b9f9b32e4292c274575271e447c3ac20e7b09a686ace
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952725"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>Método ID3DX11EffectScalarVariable::GetFloat

Obtiene una variable de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* 
</dt> <dd>

Tipo: **\* float**

Puntero a la variable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





