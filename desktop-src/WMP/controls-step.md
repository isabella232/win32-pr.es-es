---
title: Controls. Step (método)
description: El método Step hace que el elemento multimedia de vídeo actual inmovilizar la reproducción en el fotograma siguiente o en el anterior.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- método de paso de Windows Media Player
- método Step Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699607"
---
# <a name="controlsstep-method"></a>Controls. Step (método)

El método **Step** hace que el elemento multimedia de vídeo actual inmovilizar la reproducción en el fotograma siguiente o en el anterior.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*frameCount* \[ de\]
</dt> <dd>

**Número** (**largo**) que indica el número de fotogramas que se van a pasar antes de la inmovilización. Debe establecerse actualmente en 1 o-1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método solo admite actualmente los parámetros 1 o-1, por lo que solo se puede ejecutar un fotograma cada vez.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





