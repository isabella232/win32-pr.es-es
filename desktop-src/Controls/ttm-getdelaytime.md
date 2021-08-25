---
title: TTM_GETDELAYTIME mensaje (Commctrl.h)
description: Recupera las duraciones iniciales, emergentes y de volver a mostrar establecidas actualmente para un control de información sobre herramientas.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e63eca126477a6f602e6e23be75495319d30aa2814d2d72b8426a96c078326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769265"
---
# <a name="ttm_getdelaytime-message"></a>Mensaje \_ GETDELAYTIME de TTM

Recupera las duraciones iniciales, emergentes y de volver a mostrar establecidas actualmente para un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica qué valor de duración se recuperará. Este parámetro puede tener uno de los valores siguientes:



| Value                                                                                                                                                      | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**AUTOPOP de TTDT \_**</dt> </dl> | Recupere la cantidad de tiempo que la ventana de información sobre herramientas permanece visible si el puntero está estacionado dentro del rectángulo delimitador de una herramienta.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ INITIAL**</dt> </dl> | Recupere la cantidad de tiempo que el puntero debe permanecer estacionado dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>    | Recupere la cantidad de tiempo que tardan en aparecer las ventanas de información sobre herramientas posteriores a medida que el puntero se mueve de una herramienta a otra.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve y el valor INT con la duración especificada en milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETDELAYTIME de TTM**](ttm-setdelaytime.md)
</dt> </dl>

 

 





