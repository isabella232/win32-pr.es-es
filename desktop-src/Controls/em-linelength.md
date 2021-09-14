---
title: EM_LINELENGTH mensaje (Winuser.h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062159"
---
# <a name="em_linelength-message"></a>Mensaje \_ EM LINELENGTH

Recupera la longitud, en caracteres, de una línea en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de caracteres de un carácter de la línea cuya longitud se va a recuperar. Si este parámetro es mayor que el número de caracteres del control, el valor devuelto es cero.

Este parámetro puede ser -1. En este caso, el mensaje devuelve el número de caracteres no seleccionados en las líneas que contienen los caracteres seleccionados. Por ejemplo, si la selección se extiende desde el cuarto carácter de una línea hasta el octavo carácter desde el final de la línea siguiente, el valor devuelto sería 10 (tres caracteres en la primera línea y siete en la siguiente).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR,** de la línea especificada por el *parámetro wParam.* Para el texto ANSI, este es el número de bytes; Para el texto Unicode, este es el número de caracteres. No incluye el carácter de retorno de carro al final de la línea.

Para los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR,** del texto del control de edición.

Si *wParam es* mayor que el número de caracteres del control, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Use el [**mensaje EM \_ LINEINDEX para**](em-lineindex.md) recuperar un índice de caracteres para un número de línea determinado dentro de un control de edición multilínea.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





