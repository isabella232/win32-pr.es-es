---
title: Método Id3DX11EffectGroup GetDesc (D3dx11effect.h)
description: Obtiene una descripción del grupo.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c32d44e215a6c89a7d71e899d9839509cbe39417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963807"
---
# <a name="id3dx11effectgroupgetdesc-method"></a>Método ID3DX11EffectGroup::GetDesc

Obtiene una descripción del grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ GROUP \_ DESC**](d3dx11-group-desc.md)\***

Puntero a una [**estructura D3DX11 \_ GROUP \_ DESC.**](d3dx11-group-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

 





