---
title: Mensaje EM_SHOWSCROLLBAR (RichEdit. h)
description: Muestra u oculta una de las barras de desplazamiento en la ventana host de un control Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996289"
---
# <a name="em_showscrollbar-message"></a>\_Mensaje SHOWSCROLLBAR em

Muestra u oculta una de las barras de desplazamiento en la ventana host de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identifica la barra de desplazamiento que se va a mostrar: horizontal o vertical. Este parámetro debe ser **SB \_ Vert** o **SB \_ horizontal**.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si se muestra o se oculta la barra de desplazamiento. Especifique **true** para mostrar la barra de desplazamiento y **false** para ocultarla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método solo es válido cuando el control está activo en contexto. Puede producirse un error en las llamadas realizadas mientras el control está inactivo.

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

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> <dt>

[**\_SETSCROLLPOS em**](em-setscrollpos.md)
</dt> </dl>

 

 





