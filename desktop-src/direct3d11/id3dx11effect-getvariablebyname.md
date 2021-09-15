---
title: Método ID3DX11Effect GetVariableByName (D3dx11effect.h)
description: Obtenga una variable por nombre.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Método GetVariableByName Direct3D 11
- Método GetVariableByName Direct3D 11 , interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11 , método GetVariableByName
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465396"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>Método ID3DX11Effect::GetVariableByName

Obtenga una variable por nombre.

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

Puntero a [**id3DX11EffectVariable**](id3dx11effectvariable.md). Devuelve una variable no válida si no se encuentra el nombre especificado.

## <a name="remarks"></a>Observaciones

Un efecto puede contener una o varias variables. Las variables fuera de una técnica se consideran globales para todos los efectos, las que se encuentran dentro de una técnica son locales para esa técnica. Puede acceder a una variable de efecto mediante su nombre o con un índice.

El método devuelve un puntero a una [**interfaz de variable de efecto**](id3dx11effectvariable.md) independientemente de si se encuentra o no una variable. [**Se debe llamar a ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) para comprobar si el nombre existe o no.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

