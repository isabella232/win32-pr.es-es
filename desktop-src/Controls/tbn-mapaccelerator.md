---
title: TBN_MAPACCELERATOR de notificación (Commctrl.h)
description: Solicita el índice del botón de la barra de herramientas correspondiente al carácter de acelerador especificado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434195"
---
# <a name="tbn_mapaccelerator-notification-code"></a>Código de notificación \_ MAPACCELERATOR de TBN

Solicita el índice del botón de la barra de herramientas correspondiente al carácter de acelerador especificado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente. El **campo dwItemNext** es -1 si el acelerador no se corresponde con un comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE si **NMCHAR.dwItemNext** está establecido en un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





