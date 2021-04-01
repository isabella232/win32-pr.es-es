---
title: Código de notificación de EN_STARTCOMPOSITION (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario ha empezado a escribir con IME o Text Services Framework.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150911"
---
# <a name="en_startcomposition-notification-code"></a>\_Código de notificación en STARTCOMPOSITION

Notifica a una ventana primaria de un control Rich Edit que el usuario ha empezado a escribir con IME o [Text Services Framework](/windows/desktop/TSF/text-services-framework).


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

