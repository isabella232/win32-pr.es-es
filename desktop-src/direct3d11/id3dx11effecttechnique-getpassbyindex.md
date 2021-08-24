---
title: Método ID3DX11EffectTechnique GetPassByIndex (D3dx11effect.h)
description: Obtener un paso por índice.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Método GetPassByIndex Direct3D 11
- Método GetPassByIndex Direct3D 11 , interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11 , método GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd22cd5e7745b8e5a11018b930f6b544036780b118e9c745b67e730b693cdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565795"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>Método ID3DX11EffectTechnique::GetPassByIndex

Obtener un paso por índice.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Puntero a [**id3DX11EffectPass.**](id3dx11effectpass.md)

## <a name="remarks"></a>Comentarios

Una técnica contiene uno o varios pases; obtener un paso mediante un nombre o un índice.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

