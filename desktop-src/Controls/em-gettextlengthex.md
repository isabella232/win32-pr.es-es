---
title: Mensaje EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcula la longitud del texto de varias maneras. Normalmente se llama a antes de crear un búfer para recibir el texto del control.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905198"
---
# <a name="em_gettextlengthex-message"></a>\_Mensaje GETTEXTLENGTHEX em

Calcula la longitud del texto de varias maneras. Normalmente se llama a antes de crear un búfer para recibir el texto del control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) que recibe la información de longitud del texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve el número de **TCHAR** en el control de edición, dependiendo de la configuración de las marcas de la estructura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) . Si se establecieron marcas incompatibles en el miembro **Flags** , el mensaje devuelve E \_ INVALIDARG.

## <a name="remarks"></a>Observaciones

Este mensaje es una manera rápida y sencilla de determinar el número de caracteres de la versión Unicode del control Rich Edit. Sin embargo, en el caso de una página de códigos de destino no Unicode, se convertirá en una combinación de caracteres de un solo byte y de doble byte.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





