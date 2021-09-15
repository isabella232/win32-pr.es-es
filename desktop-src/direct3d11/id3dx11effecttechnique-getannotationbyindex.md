---
title: Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect.h)
description: Obtiene una anotación por índice. | Método ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect.h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11 , método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e30712ba38f1360a992a8e409c249a746cca036
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581228"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a>Método ID3DX11EffectTechnique::GetAnnotationByIndex

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

Índice de base cero del puntero de interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a [**id3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Observaciones

Use una anotación para adjuntar un fragmento de metadatos a una técnica.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

