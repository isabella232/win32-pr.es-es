---
title: Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect.h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect.h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766366497187fec9c6dab3c5f92f5fbca23f5729297976d2c9e2c7e4ffb0deef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376465"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>Método ID3DX11EffectVariable::GetAnnotationByName

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

Nombre de la anotación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a [**id3DX11EffectVariable**](id3dx11effectvariable.md). Tenga en cuenta que si no se encuentra la **anotación, el ID3DX11EffectVariable** devuelto estará vacío. Se debe llamar al método [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) para determinar si se encontró la anotación.

## <a name="remarks"></a>Comentarios

Las anaonaciones se pueden adjuntar a una técnica, un paso o una variable global.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

