---
title: Código de notificación de TBN_WRAPACCELERATOR (commctrl. h)
description: Solicita el índice del botón en una o más barras de herramientas correspondientes al carácter de aceleración especificado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656486"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>Código de notificación de WRAPACCELERATOR de TBN \_

Solicita el índice del botón en una o más barras de herramientas correspondientes al carácter de aceleración especificado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente. El índice es-1 si el acelerador no se corresponde con un comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si se devuelve un índice; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Es posible que las aplicaciones con una o más barras de herramientas reciban este código de notificación.

La estructura **NMTBWRAPACCELERATOR** debe definirse mediante la aplicación de la siguiente manera:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





