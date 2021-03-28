---
title: Método ID3DX11EffectVariable GetMemberByName (D3dx11effect. h)
description: Obtiene un miembro de estructura por nombre.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Método GetMemberByName Direct3D 11
- Método GetMemberByName Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetMemberByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998749"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a>ID3DX11EffectVariable:: GetMemberByName (método)

Obtiene un miembro de estructura por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del miembro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Observaciones

Si la variable de efecto es una estructura, use este método para buscar un miembro por nombre.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

