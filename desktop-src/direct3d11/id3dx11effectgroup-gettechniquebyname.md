---
title: Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Obtener una técnica por nombre. | Método ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986965"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a>ID3DX11EffectGroup:: GetTechniqueByName (método)

Obtener una técnica por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

El nombre de la técnica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Un puntero a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), o **null** si no se encuentra la técnica.

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

 

