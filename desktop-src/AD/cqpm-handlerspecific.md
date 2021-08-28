---
title: CQPM_HANDLERSPECIFIC mensaje (Cmnquery.h)
description: Valor base utilizado para los mensajes que son privados para el controlador de consultas.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC mensaje Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd01907a6c5e0e83f9264da56c93b58e56f8b4cb9204f64796af2f7c2b2e788a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021172"
---
# <a name="cqpm_handlerspecific-message"></a>Mensaje CQPM \_ HANDLERSPECIFIC

El **mensaje CQPM \_ HANDLERSPECIFIC** es el valor base utilizado para los mensajes que son privados para el controlador de consultas. El controlador de consultas debe agregar este valor a los mensajes privados para asegurarse de que no se produzcan colisiones de mensajes.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene datos de mensaje adicionales. El controlador de consultas define el contenido de este parámetro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene datos de mensaje adicionales. El controlador de consultas define el contenido de este parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El controlador de consultas define el significado del valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





