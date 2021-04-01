---
title: Mensaje EM_SETBKGNDCOLOR (RichEdit. h)
description: El \_ mensaje SETBKGNDCOLOR em establece el color de fondo de un control Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905524"
---
# <a name="em_setbkgndcolor-message"></a>\_Mensaje SETBKGNDCOLOR em

El **mensaje \_ SETBKGNDCOLOR em** establece el color de fondo de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se va a utilizar el color del sistema. Si este parámetro es un valor distinto de cero, el fondo se establece en el color del sistema de fondo de la ventana. De lo contrario, el fondo se establece en el color especificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el color si *wParam* es cero. Para generar un **COLORREF**, use la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el color de fondo original.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

