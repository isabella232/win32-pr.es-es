---
title: EM_FILELINELENGTH mensaje (CommCtrl.h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cb05b0e2acbfb5049eddefab1dad42ecd7b6db234fa4a3c34d4877ed52b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915545"
---
# <a name="em_filelinelength-message"></a>Mensaje \_ EM FILELINELENGTH

Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.

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

Para los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR,** de la línea especificada por el parámetro *wParam,* independientemente de cómo se muestren las líneas en la pantalla. No incluye el carácter de retorno de carro o de retorno de línea al final de la línea.

Para los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR,** del texto del control de edición.

Si *wParam es* mayor que el número de caracteres del control, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Use el [**mensaje EM \_ FILELINEINDEX**](em-lineindex.md) para recuperar un índice de caracteres para un número de línea determinado dentro de un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





