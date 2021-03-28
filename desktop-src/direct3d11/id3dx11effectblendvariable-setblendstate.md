---
title: Método ID3DX11EffectBlendVariable SetBlendState (D3dx11effect. h)
description: Establece el estado de fusión de un efecto.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Método SetBlendState Direct3D 11
- Método SetBlendState Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821311"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>ID3DX11EffectBlendVariable:: SetBlendState (método)

Establece el estado de fusión de un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de interfaces de estado de mezcla. Si solo hay una interfaz de estado de mezcla, use 0.

</dd> <dt>

*pBlendState* 
</dt> <dd>

Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Puntero a una interfaz [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) que contiene el estado de combinación que se va a establecer.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

