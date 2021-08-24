---
description: Obtiene el valor de escala de patrón de stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: Método ID3DXLine::GetPatternScale (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3799901d071da08ee1bb0de4994ed330fabe2d8fedf3b59ce556105f0a280e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675154"
---
# <a name="id3dxlinegetpatternscale-method"></a>Método ID3DXLine::GetPatternScale

Obtiene el valor de escala de patrón de stipple.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Devuelve el valor utilizado para escalar el patrón de stipple. 1.0f es el valor predeterminado y no representa ningún escalado. Un valor menor que 1,0f reduce el patrón y un valor mayor que 1,0 extiende el patrón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
