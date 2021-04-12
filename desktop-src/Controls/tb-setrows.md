---
title: Mensaje de TB_SETROWS (commctrl. h)
description: Establece el número de filas de los botones de una barra de herramientas.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079776"
---
# <a name="tb_setrows-message"></a>\_Mensaje SETROWS TB

Establece el número de filas de los botones de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el número de filas solicitadas. El número mínimo de filas es uno y el número máximo de filas es igual al número de botones de la barra de herramientas.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **booleano** que indica si se van a crear más filas de las que se solicitan cuando el sistema no puede crear el número de filas especificado por *wParam*. Si **es true**, el sistema crea más filas. Si **es false**, el sistema crea menos filas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la barra de herramientas una vez establecidas las filas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que el sistema no divide los grupos de botones al establecer el número de filas, el número resultante de filas podría diferir del número solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

