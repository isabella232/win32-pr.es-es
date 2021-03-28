---
title: Método ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect. h)
description: Obtiene una instancia de clase.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11, interfaz ID3DX11EffectClassInstanceVariable
- Interfaz ID3DX11EffectClassInstanceVariable Direct3D 11, método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362807"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>ID3DX11EffectClassInstanceVariable:: GetClassInstance (método)

Obtiene una instancia de clase.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppClassInstance* 
</dt> <dd>

Tipo: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Puntero a un puntero [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) que se establecerá en la instancia de clase.

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

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





