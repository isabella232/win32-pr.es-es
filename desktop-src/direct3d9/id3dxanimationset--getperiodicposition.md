---
description: Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet:: GetPeriodicPosition (método) (D3dx9anim. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362786"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>ID3DXAnimationSet:: GetPeriodicPosition (método)

Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Posición* \[ de de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Hora local del conjunto de animaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posición de hora medida en el período de tiempo del conjunto de animaciones. Este valor estará limitado por el período del conjunto de animaciones.

## <a name="remarks"></a>Observaciones

La posición de hora devuelta por este método se puede usar como el parámetro PeriodicPosition de [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
