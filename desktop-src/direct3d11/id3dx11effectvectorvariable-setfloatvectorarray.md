---
title: Método ID3DX11EffectVectorVariable SetFloatVectorArray (D3dx11effect. h)
description: Establezca una matriz de vectores de cuatro componentes que contengan datos de punto flotante.
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- Método SetFloatVectorArray Direct3D 11
- Método SetFloatVectorArray Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método SetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987067"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a>ID3DX11EffectVectorVariable:: SetFloatVectorArray (método)

Establezca una matriz de vectores de cuatro componentes que contengan datos de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntero al principio de los datos que se van a establecer.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Debe establecerse en 0; está reservado para uso futuro.

</dd> <dt>

*Recuento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de matriz que se van a establecer.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

