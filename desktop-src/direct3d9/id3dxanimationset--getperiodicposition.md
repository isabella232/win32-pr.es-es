---
description: Devuelve la posición de tiempo en el período de tiempo local de un conjunto de animación.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: Método ID3DXAnimationSet::GetPeriodicPosition (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969684"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>Método ID3DXAnimationSet::GetPeriodicPosition

Devuelve la posición de tiempo en el período de tiempo local de un conjunto de animación.

## <a name="syntax"></a>Sintaxis


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Posición* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Hora local del conjunto de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Posición de tiempo medida en el período de tiempo del conjunto de animación. Este valor se delimitará por el período del conjunto de animación.

## <a name="remarks"></a>Observaciones

La posición de hora devuelta por este método se puede usar como parámetro PeriodicPosition de [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
