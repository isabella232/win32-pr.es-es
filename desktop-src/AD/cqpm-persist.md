---
title: CQPM_PERSIST mensaje (Cmnquery.h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST mensaje Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66eeeba5f80397aa422c465cb224064c58a4544f4d64ae2fba3bed5030b1c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020976"
---
# <a name="cqpm_persist-message"></a>Mensaje CQPM \_ PERSIST

El **mensaje CQPM \_ PERSIST** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene distinto de cero para leer los datos de consulta o cero para escribir los datos de consulta.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**interfaz IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) desde la que se deben leer o escribir los datos de la consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S OK si \_ se** realiza correctamente o un código de error **HRESULT** estándar de lo contrario.

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

[**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

