---
title: Mensaje de CQPM_PERSIST (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST Active Directory de mensaje
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
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079315"
---
# <a name="cqpm_persist-message"></a>CQPM \_ mensaje persistente

El mensaje **CQPM \_ Persist** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la página lea o escriba datos de consulta de la memoria persistente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valor distinto de cero para leer los datos de la consulta o cero para escribir los datos de la consulta.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una interfaz [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) en la que se deben leer o escribir los datos de la consulta.

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

[**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

