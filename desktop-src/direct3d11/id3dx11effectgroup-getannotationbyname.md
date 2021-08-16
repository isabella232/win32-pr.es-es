---
title: Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect.h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect.h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11 , interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11 , método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d80c0d59a1fd0a58c756d72f6215f13b4e3391e44828aa8e1bcff23063292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535750"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a>Método ID3DX11EffectGroup::GetAnnotationByName

Obtiene una anotación por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

El nombre de la anotación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a [**id3DX11EffectVariable**](id3dx11effectvariable.md). Tenga en cuenta que si no se encuentra la **anotación, id3DX11EffectVariable** devuelto estará vacío. Se debe llamar al método [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) para determinar si se encontró la anotación.

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

