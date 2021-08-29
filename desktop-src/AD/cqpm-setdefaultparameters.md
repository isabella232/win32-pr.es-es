---
title: CQPM_SETDEFAULTPARAMETERS mensaje (Cmnquery.h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para establecer parámetros predeterminados alternativos para la página.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS mensaje Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e8c3120651e2bdd2ffb8fd861563aa45cb4009c7a37bb3236e914e0def7d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020956"
---
# <a name="cqpm_setdefaultparameters-message"></a>Mensaje SETDEFAULTPARAMETERS de CQPM \_

El **mensaje CQPM \_ SETDEFAULTPARAMETERS** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para establecer parámetros predeterminados alternativos para la página.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valor distinto de cero si la página es la predeterminada o cero en caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OPENQUERYWINDOW que**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) contiene datos sobre el cuadro de diálogo de consulta del servicio de directorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





