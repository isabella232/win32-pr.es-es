---
title: Método ID3DX11Effect GetClassLinkage (D3dx11effect.h)
description: Obtiene una interfaz de vinculación de clases.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Método GetClassLinkage Direct3D 11
- Método GetClassLinkage Direct3D 11 , interfaz ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , GetClassLinkage method
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f4a34ad8ff2e53d521d4fd7a1510332dddf8ff7197eac17bf4231a26e98f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632665"
---
# <a name="id3dx11effectgetclasslinkage-method"></a>Método ID3DX11Effect::GetClassLinkage

Obtiene una interfaz de vinculación de clases.

## <a name="syntax"></a>Sintaxis


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***

Devuelve un puntero a una [**interfaz ID3D11ClassLinkage.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





