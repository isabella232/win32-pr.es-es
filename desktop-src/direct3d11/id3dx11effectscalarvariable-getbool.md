---
title: Método ID3DX11EffectScalarVariable GetBool (D3dx11effect. h)
description: Obtiene una variable booleana.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Método GetBool Direct3D 11
- Método GetBool Direct3D 11, interfaz ID3DX11EffectScalarVariable
- Interfaz ID3DX11EffectScalarVariable Direct3D 11, método GetBool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821450"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a>ID3DX11EffectScalarVariable:: GetBool (método)

Obtiene una variable booleana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* 
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

Puntero a la variable.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

