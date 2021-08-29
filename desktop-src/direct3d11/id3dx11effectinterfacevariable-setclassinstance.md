---
title: Método ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect.h)
description: Establece una instancia de clase.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Método SetClassInstance Direct3D 11
- Método SetClassInstance Direct3D 11 , interfaz ID3DX11EffectInterfaceVariable
- Interfaz ID3DX11EffectInterfaceVariable Direct3D 11, método SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e3dc8b982a5545c9860be92a51306fc438908864b2980bec5197fec76181c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046223"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a>Método ID3DX11EffectInterfaceVariable::SetClassInstance

Establece una instancia de clase.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEffectClassInstance* 
</dt> <dd>

Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Puntero a una [**interfaz ID3DX11EffectClassInstanceVariable.**](id3dx11effectclassinstancevariable.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





