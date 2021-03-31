---
title: Mensaje de CQPM_HELP (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149986"
---
# <a name="cqpm_help-message"></a>CQPM \_ mensaje de ayuda

El mensaje de **\_ ayuda CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página. Si es posible, la extensión de página de consulta debe mostrar ayuda contextual en respuesta a este evento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene datos adicionales sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda contextual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

