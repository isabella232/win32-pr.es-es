---
title: CQPM_HELP mensaje (Cmnquery.h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP mensaje Active Directory
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
ms.openlocfilehash: 7a50be772a429a2eb2f87bf3cf1679dcfc68e811d80244f10dd4ec33f3f2b7d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021101"
---
# <a name="cqpm_help-message"></a>Mensaje DE AYUDA de CQPM \_

El mensaje HELP de **CQPM \_** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página. Si es posible, la extensión de página de consulta debe mostrar ayuda contextual en respuesta a este evento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene datos adicionales sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda contextual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

