---
description: Estira el patrón punteado a lo largo de la dirección de la línea.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine:: SetPatternScale (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280517"
---
# <a name="id3dxlinesetpatternscale-method"></a>ID3DXLine:: SetPatternScale (método)

Estira el patrón punteado a lo largo de la dirección de la línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fPatternScale* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor de escala del patrón punteado. 1.0 f es el valor predeterminado y no representa ningún ajuste de escala. Un valor menor que 1,0 f reduce el modelo y un valor mayor que 1,0 expande el patrón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
