---
title: Método ID3DX11Effect GetVariableBySemantic (D3dx11effect.h)
description: Obtiene una variable por semántica.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Método GetVariableBySemantic Direct3D 11
- Método GetVariableBySemantic Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11 , método GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465563"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>Método ID3DX11Effect::GetVariableBySemantic

Obtiene una variable por semántica.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Semántica* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre semántico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a la variable de efecto indicada por semántica. Vea [**ID3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Observaciones

Cada variable de efecto puede tener asociada una semántica, que es una cadena de metadatos definida por el usuario. Algunas [semánticas de valores del sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) son palabras reservadas que desencadenan la funcionalidad integrada por fases de canalización.

El método devuelve un puntero a una [**interfaz effect-variable**](id3dx11effectvariable.md) si no se encuentra una variable; Puede llamar a [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) para comprobar si existe o no la semántica.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

