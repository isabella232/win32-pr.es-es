---
title: Método Id3DX11Effect IsValid (D3dx11effect.h)
description: Pruebe un efecto para ver si contiene una sintaxis válida. | Método Id3DX11Effect IsValid (D3dx11effect.h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d49cff0f745caddf571b0f0e8d3d2d351d8a90058335611c43edd89f79d84810
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608795"
---
# <a name="id3dx11effectisvalid-method"></a>Método ID3DX11Effect::IsValid

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

