---
title: Código de notificación de TBN_GETINFOTIP (commctrl. h)
description: Recupera información de recuadro informativo para un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079117"
---
# <a name="tbn_getinfotip-notification-code"></a>Código de notificación de GETINFOTIP de TBN \_

Recupera información de recuadro informativo para un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contiene información sobre los elementos y recibe información de recuadro informativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="remarks"></a>Observaciones

La compatibilidad con el recuadro informativo de la barra de herramientas permite que la barra de herramientas muestre información sobre herramientas para los elementos que tienen un tamaño de INFOTIPSIZE caracteres. Si no se procesa este código de notificación, la barra de herramientas usará el texto del elemento para el recuadro informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) y **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





