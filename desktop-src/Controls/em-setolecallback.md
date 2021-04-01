---
title: Mensaje EM_SETOLECALLBACK (RichEdit. h)
description: Proporciona un control de edición enriquecido a un objeto IRichEditOleCallback que el control usa para obtener recursos e información relacionados con OLE del cliente.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996561"
---
# <a name="em_setolecallback-message"></a>\_Mensaje SETOLECALLBACK em

Proporciona un control de edición enriquecido a un objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que el control usa para obtener recursos e información relacionados con OLE del cliente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) . El control llama al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para el objeto antes de devolver.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

