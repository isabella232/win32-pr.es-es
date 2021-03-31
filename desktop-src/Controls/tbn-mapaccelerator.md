---
title: Código de notificación de TBN_MAPACCELERATOR (commctrl. h)
description: Solicita el índice del botón en la barra de herramientas correspondiente al carácter acelerador especificado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR controles de código de notificación de Windows
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
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995923"
---
# <a name="tbn_mapaccelerator-notification-code"></a>Código de notificación de MAPACCELERATOR de TBN \_

Solicita el índice del botón en la barra de herramientas correspondiente al carácter acelerador especificado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente. El campo **dwItemNext** es-1 si el acelerador no se corresponde con un comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE si **NMCHAR. dwItemNext** está establecido en un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





