---
title: CQPM_GETPARAMETERS mensaje (Cmnquery.h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS mensaje Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64713c79fc2c1b72f1962363f1330ecd794ad804f0ab084b66c134c66133cd82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021236"
---
# <a name="cqpm_getparameters-message"></a>Mensaje GETPARAMETERS de CQPM \_

El **mensaje \_ GETPARAMETERS de CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un [**valor LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) que recibe datos sobre la consulta realizada por la página. Si este parámetro es **NULL,** la extensión debe asignar la estructura **DSQUERYPARAMS** mediante la [**función CoTaskMemAlloc.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S OK si \_ se** realiza correctamente o un código de error **HRESULT** estándar de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

