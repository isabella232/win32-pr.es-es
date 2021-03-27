---
title: Método ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Establezca un búfer de constantes.
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
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280477"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a>ID3DX11EffectConstantBuffer:: SetConstantBuffer (método)

Establezca un búfer de constantes.

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

Puntero a una interfaz de búfer de constantes. Vea [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





