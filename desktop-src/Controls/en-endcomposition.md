---
title: Código de notificación de EN_ENDCOMPOSITION (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario ha escrito nuevos datos o que ha terminado de escribir datos mientras usa el marco de trabajo de servicios de texto o IME.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489281"
---
# <a name="en_endcomposition-notification-code"></a>\_Código de notificación en ENDCOMPOSITION

Notifica a una ventana primaria de un control Rich Edit que el usuario ha escrito nuevos datos o que ha terminado de escribir datos mientras usa el [marco de trabajo de servicios de texto](/windows/desktop/TSF/text-services-framework)o IME.


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Una estructura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) que recibe información sobre la condición de finalización de composición.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

