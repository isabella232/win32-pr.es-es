---
title: EN_ENDCOMPOSITION de notificación (Richedit.h)
description: Notifica a una ventana primaria de control de edición enriqueciendo que el usuario ha escrito datos nuevos o ha terminado de escribir datos mientras usa IME o Text Services Framework.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION código de notificación Windows controles
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
ms.openlocfilehash: 5d9fe75910ea018cf9d72dd14696067eb0b2bc00dabd4456cca63e41a099a75d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436855"
---
# <a name="en_endcomposition-notification-code"></a>Código de notificación EN \_ ENDCOMPOSITION

Notifica a una ventana primaria de control de edición enriqueciendo que el usuario ha escrito datos nuevos o ha terminado de escribir datos mientras usa IME [o Text Services Framework](/windows/desktop/TSF/text-services-framework).


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) que recibe información sobre la condición de composición final.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

