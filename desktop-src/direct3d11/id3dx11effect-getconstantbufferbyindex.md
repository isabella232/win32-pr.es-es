---
title: Método ID3DX11Effect GetConstantBufferByIndex (D3dx11effect.h)
description: Obtiene un búfer constante por índice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Método GetConstantBufferByIndex Direct3D 11
- Método GetConstantBufferByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11 , método GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d2ce34bb6bde85600e57182151e8c270885e60f919f22a723228b14dd17927a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632605"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>Método ID3DX11Effect::GetConstantBufferByIndex

Obtiene un búfer constante por índice.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
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

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntero a [**id3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Comentarios

Un efecto que contiene una variable que una aplicación leerá o escribirá requiere al menos un búfer constante. Para obtener el mejor rendimiento, un efecto debe organizar las variables en uno o varios búferes constantes en función de su frecuencia de actualización.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

