---
title: Método ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Obtiene un paso por índice.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Método GetPassByIndex Direct3D 11
- Método GetPassByIndex Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetPassByIndex
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
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003933"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>ID3DX11EffectTechnique:: GetPassByIndex (método)

Obtiene un paso por índice.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Un puntero a un [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Observaciones

Una técnica contiene uno o más pasos; obtener un paso mediante un nombre o un índice.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

