---
title: Mensaje de CQPM_GETPARAMETERS (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS Active Directory de mensaje
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
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905064"
---
# <a name="cqpm_getparameters-message"></a>CQPM \_ mensaje de GETPARAMETERS

El mensaje de **\_ GETPARAMETERS de CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor de [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) que recibe datos sobre la consulta realizada por la página. Si este parámetro es **null**, la extensión **DSQUERYPARAMS** debe estar asignada mediante la función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si es correcto o un código de error **HRESULT** estándar en caso contrario.

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

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

