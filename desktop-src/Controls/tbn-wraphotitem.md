---
title: Código de notificación de TBN_WRAPHOTITEM (commctrl. h)
description: Notifica a una aplicación con dos o más barras de herramientas que el elemento activo va a cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490192"
---
# <a name="tbn_wraphotitem-notification-code"></a>Código de notificación de WRAPHOTITEM de TBN \_

Notifica a una aplicación con dos o más barras de herramientas que el elemento activo va a cambiar. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene el elemento activo anterior (**iStart**) y si el nuevo elemento activo está delante de él (**iDir** =-1) o después de él (**iDir** = 1), así como un motivo por el que el elemento activo está cambiando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si la aplicación controla el propio cambio de elemento activo. en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

La estructura **NMTBWRAPHOTITEM** debe definirse mediante la aplicación de la siguiente manera:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





