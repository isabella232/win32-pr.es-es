---
title: EM_FORMATRANGE mensaje (Richedit.h)
description: Da formato a un intervalo de texto en un control de edición enriquecido para un dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE controles de Windows mensaje
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
ms.openlocfilehash: 941aceb8c8f91657c7f78aba3d83a627fc413ed20d71217c933c6fba9b6f39e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049355"
---
# <a name="em_formatrange-message"></a>Mensaje \_ EM FORMATRANGE

Da formato a un intervalo de texto en un control de edición enriquecido para un dispositivo específico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se va a representar el texto. Si este parámetro no es cero, se representa el texto. De lo contrario, el texto solo se mide.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FORMATRANGE que**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contiene información sobre el dispositivo de salida o **NULL** para liberar información almacenada en caché por el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el índice del último carácter que cabe en la región, más 1.

## <a name="remarks"></a>Comentarios

Este mensaje se usa normalmente para dar formato al contenido del control de edición enriquecido para un dispositivo de salida, como una impresora.

Después de usar este mensaje para dar formato a un intervalo de texto, es importante liberar información almacenada en caché mediante el envío de **EM \_ FORMATRANGE** de nuevo, pero con *lParam* establecido en **NULL;** de lo contrario, se producirá una pérdida de memoria. Además, después de usar este mensaje para un dispositivo, debe liberar información almacenada en caché antes de volver a usarlo para otro dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Imprimir controles rich edit](printing-rich-edit-controls.md)
</dt> </dl>

 

 





