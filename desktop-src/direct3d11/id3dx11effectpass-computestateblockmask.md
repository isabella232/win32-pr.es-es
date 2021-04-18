---
title: Método ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Generar una máscara para permitir o evitar cambios de estado.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987037"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>ID3DX11EffectPass:: ComputeStateBlockMask (método)

Generar una máscara para permitir o evitar cambios de estado.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





