---
title: EM_SETEDITSTYLE mensaje (Richedit.h)
description: Establece las marcas de estilo de edición actuales para un control de edición enriquecido.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06789b1d1fedfc76af205ac46aac7d3ea4bb882f2460676df96cd018d5a216b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048595"
---
# <a name="em_seteditstyle-message"></a>Mensaje \_ SETEDITSTYLE de EM

Establece las marcas de estilo de edición actuales para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica una o varias marcas de estilo de edición. Para obtener una lista de valores posibles, [**vea EM \_ GETEDITSTYLE**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara que consta de uno o varios de los *valores wParam.* Solo se establecerán o borrarán los valores especificados en esta máscara. Esto permite establecer o borrar una marca única sin leer los estados actuales de la marca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el estado de las marcas de estilo de edición después de que el control de edición enriquezca haya intentado implementar los cambios de estilo de edición. Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





