---
title: Método Id3DX11EffectGroup IsValid (D3dx11effect.h)
description: Pruebe un efecto para ver si contiene una sintaxis válida. | Método Id3DX11EffectGroup IsValid (D3dx11effect.h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11 , método IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28c0658c45e4091233e75c6456a9446da46a5a6d4a045bf3a533d881b42ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046253"
---
# <a name="id3dx11effectgroupisvalid-method"></a>Método ID3DX11EffectGroup::IsValid

Pruebe un efecto para ver si contiene una sintaxis válida.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** si la sintaxis de código es válida; en caso **contrario, FALSE**.

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

