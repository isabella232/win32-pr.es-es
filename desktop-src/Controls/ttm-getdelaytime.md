---
title: Mensaje de TTM_GETDELAYTIME (commctrl. h)
description: Recupera las duraciones iniciales, emergentes y de visualización que se establecen actualmente para un control ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME controles de mensajes de Windows
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
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658191"
---
# <a name="ttm_getdelaytime-message"></a>TTM \_ GETDELAYTIME

Recupera las duraciones iniciales, emergentes y de visualización que se establecen actualmente para un control ToolTip.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el valor de duración que se recuperará. Este parámetro puede tener uno de los valores siguientes:



| Value                                                                                                                                                      | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | Recupera la cantidad de tiempo que la ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ inicial**</dt> </dl> | Recupera la cantidad de tiempo que el puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ Mostrar**</dt> </dl>    | Recupere la cantidad de tiempo que se tarda en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se desplaza de una herramienta a otra.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve e INT con la duración especificada en milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)
</dt> </dl>

 

 





