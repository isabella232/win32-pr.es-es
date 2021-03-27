---
title: Método ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Obtiene una instancia de clase.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11, interfaz ID3DX11EffectInterfaceVariable
- Interfaz ID3DX11EffectInterfaceVariable Direct3D 11, método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003881"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a>ID3DX11EffectInterfaceVariable:: GetClassInstance (método)

Obtiene una instancia de clase.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEffectClassInstance* 
</dt> <dd>

Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***

Puntero a un puntero [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) que se establecerá en la instancia de clase.

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





