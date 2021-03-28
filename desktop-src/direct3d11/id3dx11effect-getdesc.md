---
title: Método ID3DX11Effect GetDesc (D3dx11effect. h)
description: Obtiene una descripción de efecto.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998634"
---
# <a name="id3dx11effectgetdesc-method"></a>ID3DX11Effect:: GetDesc (método)

Obtiene una descripción de efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ efecto \_ DESC**](d3dx11-effect-desc.md)\***

Un puntero a una descripción de efecto (vea [**D3DX11 \_ Effect \_ DESC**](d3dx11-effect-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Una descripción de efecto contiene información básica sobre un efecto, como las técnicas que contiene y los recursos de búfer de constantes que requiere.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





