---
description: Extiende el patrón detippla a lo largo de la dirección de la línea.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: Método ID3DXLine::SetPatternScale (D3dx9core.h)
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
ms.openlocfilehash: df460f8040b1f73d4837b51533586a19630eed1ddcf435291857b05dc4bae1a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951365"
---
# <a name="id3dxlinesetpatternscale-method"></a>Método ID3DXLine::SetPatternScale

Extiende el patrón detippla a lo largo de la dirección de la línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fPatternScale* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de escalado del patrón de stipple. 1.0f es el valor predeterminado y no representa ningún escalado. Un valor menor que 1,0f reduce el patrón y un valor mayor que 1,0 extiende el patrón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
