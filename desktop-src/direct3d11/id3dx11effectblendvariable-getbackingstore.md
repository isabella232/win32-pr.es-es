---
title: Método ID3DX11EffectBlendVariable GetBackingStore (D3dx11effect.h)
description: Obtiene un puntero a una variable de estado de mezcla.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11 , interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02f09c0db4ec56ee592dc39ddbb7fef1ae52d328edec5d9a5c9fd17b769ef58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046563"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a>Método ID3DX11EffectBlendVariable::GetBackingStore

Obtiene un puntero a una variable de estado de mezcla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de descripciones de estado de mezcla. Si solo hay una variable de estado de mezcla en el efecto, use 0.

</dd> <dt>

*pBlendDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***

Puntero a una descripción de estado de mezcla (vea [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Las variables de efecto se guardan en la memoria del almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Los datos de almacenamiento de respaldo se pueden usar para volver a crear la variable cuando sea necesario.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

