---
title: Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Obtiene una técnica por índice. | Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003884"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a>ID3DX11EffectGroup:: GetTechniqueByIndex (método)

Obtiene una técnica por índice.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
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

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

