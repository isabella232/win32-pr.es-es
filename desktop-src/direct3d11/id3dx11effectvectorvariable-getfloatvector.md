---
title: Método ID3DX11EffectVectorVariable GetFloatVector (D3dx11effect.h)
description: Obtiene un vector de cuatro componentes que contiene datos de punto flotante.
ms.assetid: 980c85db-0d40-49e0-99d0-5049fdf62540
keywords:
- Método GetFloatVector Direct3D 11
- Método GetFloatVector Direct3D 11 , interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable direct3D 11 , método GetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861121c89bbeda277610c0c3e42d4d6e41795b5cd82b48ae8ba42a1783ee5eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989675"
---
# <a name="id3dx11effectvectorvariablegetfloatvector-method"></a>Método ID3DX11EffectVectorVariable::GetFloatVector

Obtiene un vector de cuatro componentes que contiene datos de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **\* float**

Puntero al primer componente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





