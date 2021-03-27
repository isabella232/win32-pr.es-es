---
title: Método ID3DX11EffectVectorVariable SetIntVector (D3dx11effect. h)
description: Establezca un vector de cuatro componentes que contenga datos enteros.
ms.assetid: d0546da4-c3b4-4e97-9aa9-d3b7022e22c5
keywords:
- Método SetIntVector Direct3D 11
- Método SetIntVector Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método SetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6141185459dbe7aad494312210b4517fe4f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280333"
---
# <a name="id3dx11effectvectorvariablesetintvector-method"></a>ID3DX11EffectVectorVariable:: SetIntVector (método)

Establezca un vector de cuatro componentes que contenga datos enteros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIntVector(
   int *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Puntero al primer componente.

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

 

