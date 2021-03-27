---
title: Método ID3DX11EffectGroup GetDesc (D3dx11effect. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003904"
---
# <a name="id3dx11effectgroupgetdesc-method"></a>ID3DX11EffectGroup:: GetDesc (método)

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

Tipo: **[ **\_ \_ DESC de grupo de D3DX11**](d3dx11-group-desc.md)\***

Puntero a una estructura [**de \_ \_ DESC de grupo de D3DX11**](d3dx11-group-desc.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

 

 





