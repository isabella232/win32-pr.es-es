---
title: Mensaje EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Devuelve el estado actual de las opciones tipográficas de un control Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150761"
---
# <a name="em_gettypographyoptions-message"></a>\_Mensaje GETTYPOGRAPHYOPTIONS em

Devuelve el estado actual de las opciones tipográficas de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las opciones de tipografía actuales. Para obtener una lista de opciones, consulte [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).

## <a name="remarks"></a>Observaciones

Puede activar el salto de línea avanzado enviando el mensaje [**\_ SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md) . El control Rich Edit también puede activar el salto de línea avanzado y normal automáticamente si es necesario para determinados idiomas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de los controles Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





