---
title: EM_SETOLECALLBACK mensaje (Richedit.h)
description: Proporciona a un control de edición enriquecido un objeto IRichEditOleCallback que el control usa para obtener información y recursos relacionados con OLE del cliente.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062091"
---
# <a name="em_setolecallback-message"></a>Mensaje EM \_ SETOLECALLBACK

Proporciona a un control de edición enriquecido un [**objeto IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que el control usa para obtener información y recursos relacionados con OLE del cliente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un [**objeto IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) El control llama al [**método AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) del objeto antes de devolverlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

