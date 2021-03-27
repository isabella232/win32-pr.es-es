---
title: Método IsValid ID3DX11EffectGroup (D3dx11effect. h)
description: Pruebe un efecto para ver si contiene una sintaxis válida. | Método IsValid ID3DX11EffectGroup (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- IsValid (método) Direct3D 11
- IsValid (método) Direct3D 11, ID3DX11EffectGroup (interfaz)
- Interfaz ID3DX11EffectGroup Direct3D 11, IsValid (método)
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
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986958"
---
# <a name="id3dx11effectgroupisvalid-method"></a>ID3DX11EffectGroup:: IsValid (método)

Pruebe un efecto para ver si contiene una sintaxis válida.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si la sintaxis del código es válida; en caso contrario, **false**.

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

