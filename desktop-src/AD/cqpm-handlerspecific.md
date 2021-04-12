---
title: Mensaje de CQPM_HANDLERSPECIFIC (Cmnquery. h)
description: Valor base utilizado para los mensajes que son privados para el controlador de consultas.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC Active Directory de mensaje
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
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489478"
---
# <a name="cqpm_handlerspecific-message"></a>CQPM \_ HANDLERSPECIFIC

El mensaje **CQPM \_ HANDLERSPECIFIC** es el valor base que se usa para los mensajes que son privados para el controlador de consultas. El controlador de consultas debe agregar este valor a los mensajes privados para asegurarse de que no se producen colisiones de mensajes.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene datos de mensajes adicionales. El contenido de este parámetro se define mediante el controlador de consultas.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene datos de mensajes adicionales. El contenido de este parámetro se define mediante el controlador de consultas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El identificador de consulta define el significado del valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





