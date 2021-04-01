---
title: Mensaje EM_FORMATRANGE (RichEdit. h)
description: Da formato a un intervalo de texto en un control Rich Edit para un dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905314"
---
# <a name="em_formatrange-message"></a>\_Mensaje FORMATRANGE em

Da formato a un intervalo de texto en un control Rich Edit para un dispositivo específico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se va a representar el texto. Si este parámetro no es cero, se representa el texto. De lo contrario, el texto se mide simplemente.

</dd> <dt>

*lParam* 
</dt> <dd>

Una estructura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que contiene información sobre el dispositivo de salida o **null** para liberar información almacenada en memoria caché por el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el índice del último carácter que cabe en la región, más 1.

## <a name="remarks"></a>Observaciones

Este mensaje se usa normalmente para dar formato al contenido de un control Rich Edit para un dispositivo de salida, como una impresora.

Después de usar este mensaje para dar formato a un intervalo de texto, es importante que libere información en caché enviando **\_ FORMATRANGE de EM** de nuevo, pero con *lParam* establecido en **null**; de lo contrario, se producirá una fuga de memoria. Además, después de usar este mensaje para un dispositivo, debe liberar la información almacenada en caché antes de utilizarla de nuevo para un dispositivo diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_DISPLAYBAND em**](em-displayband.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Imprimir controles Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

 





