---
title: Mensaje de EM_LINELENGTH (Winuser. h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905480"
---
# <a name="em_linelength-message"></a>\_Mensaje LINELENGTH em

Recupera la longitud, en caracteres, de una línea en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de carácter de un carácter de la línea cuya longitud se va a recuperar. Si este parámetro es mayor que el número de caracteres del control, el valor devuelto es cero.

Este parámetro puede ser-1. En este caso, el mensaje devuelve el número de caracteres no seleccionados en líneas que contienen los caracteres seleccionados. Por ejemplo, si la selección se extiende desde el cuarto carácter de una línea hasta el octavo carácter desde el final de la línea siguiente, el valor devuelto sería 10 (tres caracteres en la primera línea y siete en el siguiente).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En el caso de los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR** s, de la línea especificada por el parámetro *wParam* . Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres. No incluye el carácter de retorno de carro al final de la línea.

En el caso de los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR** s, del texto del control de edición.

Si *wParam* es mayor que el número de caracteres del control, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Use el [**mensaje \_ LINEINDEX em**](em-lineindex.md) para recuperar un índice de carácter para un número de línea determinado dentro de un control de edición multilínea.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





