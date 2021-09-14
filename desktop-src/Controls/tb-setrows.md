---
title: TB_SETROWS mensaje (Commctrl.h)
description: Establece el número de filas de botones de una barra de herramientas.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166569"
---
# <a name="tb_setrows-message"></a>Mensaje \_ DE TB SETROWS

Establece el número de filas de botones de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el número de filas solicitadas. El número mínimo de filas es uno y el número máximo de filas es igual al número de botones de la barra de herramientas.

[**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **VALOR BOOL** que indica si se deben crear más filas de las solicitadas cuando el sistema no puede crear el número de filas especificado por *wParam*. Si **es TRUE,** el sistema crea más filas. Si **es FALSE,** el sistema crea menos filas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la barra de herramientas después de establecer las filas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que el sistema no separa los grupos de botones al establecer el número de filas, el número resultante de filas puede diferir del número solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

