---
title: Método ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect.h)
description: Establezca un búfer constante.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Método SetConstantBuffer Direct3D 11
- Método SetConstantBuffer Direct3D 11, interfaz ID3DX11EffectConstantBuffer
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, método SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16519067857d89fb7b28c9fd74af8de5e12029d71ac0d60763692bdd45e27138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046413"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a>Método ID3DX11EffectConstantBuffer::SetConstantBuffer

Establezca un búfer constante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConstantBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***

Puntero a una interfaz de búfer constante. Vea [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





