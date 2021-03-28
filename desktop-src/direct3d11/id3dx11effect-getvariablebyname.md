---
title: Método ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obtiene una variable por nombre.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Método GetVariableByName Direct3D 11
- Método GetVariableByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998610"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>ID3DX11Effect:: GetVariableByName (método)

Obtiene una variable por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

El nombre de la variable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Devuelve una variable no válida si no se encuentra el nombre especificado.

## <a name="remarks"></a>Observaciones

Un efecto puede contener una o más variables. Las variables fuera de una técnica se consideran globales para todos los efectos, las que se encuentran dentro de una técnica son locales para esa técnica. Puede tener acceso a una variable de efecto mediante su nombre o con un índice.

El método devuelve un puntero a una [**interfaz de variable de efecto**](id3dx11effectvariable.md) tanto si se encuentra una variable como si no. Se debe llamar a [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para comprobar si existe o no el nombre.

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

 

