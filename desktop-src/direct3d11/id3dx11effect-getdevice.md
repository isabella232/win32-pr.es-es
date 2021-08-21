---
title: Método Id3DX11Effect GetDevice (D3dx11effect.h)
description: Obtenga el dispositivo que creó el efecto.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Método GetDevice Direct3D 11
- Método GetDevice Direct3D 11, interfaz ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , GetDevice method
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a27dece1915373699d130f8a537a22045f7e86f246402d85bbb400ceb1d8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124520"
---
# <a name="id3dx11effectgetdevice-method"></a>Método ID3DX11Effect::GetDevice

Obtenga el dispositivo que creó el efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Puntero a [**id3D11Dispositivo.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Se crea un efecto para un dispositivo específico mediante una llamada a una función como [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

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

 

 





