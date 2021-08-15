---
title: Método ID3DX11EffectTechnique GetPassByName (D3dx11effect.h)
description: Obtenga un pase por nombre.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Método GetPassByName Direct3D 11
- Método GetPassByName Direct3D 11 , interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11 , método GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfad489fe6c4eda8ea417a9f272bcc0a7d4035eb04bc675cf599e4f5381234db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532367"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>Método ID3DX11EffectTechnique::GetPassByName

Obtenga un pase por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del paso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Puntero a [**id3DX11EffectPass.**](id3dx11effectpass.md)

## <a name="remarks"></a>Comentarios

Una técnica contiene uno o varios pases; obtener un paso mediante un nombre o un índice.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

