---
title: EM_GETOLEINTERFACE mensaje (Richedit.h)
description: Recupera un objeto IRichEditOle que un cliente puede usar para acceder a la funcionalidad del Modelo de objetos componentes (COM) de un control de edición enriquecido.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e1799039081ed8250cb062aa3d1348a2fe8a8dbdcfa768fab74855d18d8e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831676"
---
# <a name="em_getoleinterface-message"></a>Mensaje \_ EM GETOLEINTERFACE

Recupera un objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que un cliente puede usar para acceder a la funcionalidad del Modelo de objetos componentes (COM) de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un puntero que recibe el [**objeto IRichEditOle.**](/windows/desktop/api/Richole/nn-richole-iricheditole) El control llama al [**método AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para el objeto antes de devolverlo, por lo que la aplicación que realiza la llamada debe llamar al [**método Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando se realiza con el objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

