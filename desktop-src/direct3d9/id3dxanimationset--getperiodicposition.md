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
ms.openlocfilehash: 8451e3332b61d7e6e993de7df0832a78c0c45c0240633fd5f421998816f7f26f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122066"
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

## <a name="remarks"></a>Comentarios

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

 

 
