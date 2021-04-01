---
title: Código de notificación de TBN_ENDDRAG (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha dejado de arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150736"
---
# <a name="tbn_enddrag-notification-code"></a>Código de notificación de ENDDRAG de TBN \_

Notifica a la ventana primaria de la barra de herramientas que el usuario ha dejado de arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . El miembro **iItem** contiene el identificador de comando del botón que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





