---
title: Método ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect. h)
description: Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280265"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>ID3DX11EffectTechnique:: ComputeStateBlockMask (método)

Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Tipo: **[ **\_ máscara de \_ bloque \_ de estado de D3DX11**](d3dx11-state-block-mask.md)\***

Un puntero a una máscara de bloque de estado (consulte [**D3DX11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).

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

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





