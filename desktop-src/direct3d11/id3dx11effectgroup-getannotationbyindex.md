---
title: Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect.h)
description: Obtiene una anotación por índice. | Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect.h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11 , interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11 , método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1cdceb5824ab3700ea5e971859967b4df26294fa458558611e0ecc3d0140ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046303"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a>Método ID3DX11EffectGroup::GetAnnotationByIndex

Obtiene una anotación por índice.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de la anotación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a una [**interfaz ID3DX11EffectVariable.**](id3dx11effectvariable.md)

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

