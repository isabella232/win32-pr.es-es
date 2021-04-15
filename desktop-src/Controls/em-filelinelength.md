---
title: Mensaje de EM_FILELINELENGTH (CommCtrl. h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH controles de mensajes de Windows
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
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534371"
---
# <a name="em_filelinelength-message"></a>\_Mensaje FILELINELENGTH em

Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.

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

En el caso de los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR** s, de la línea especificada por el parámetro *wParam* , independientemente de cómo se muestren las líneas en la pantalla. No incluye el carácter de retorno de carro o avance de línea al final de la línea.

En el caso de los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR** s, del texto del control de edición.

Si *wParam* es mayor que el número de caracteres del control, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Use el [**mensaje \_ FILELINEINDEX em**](em-lineindex.md) para recuperar un índice de carácter para un número de línea determinado dentro de un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_FILELINEINDEX em**](em-filelineindex.md)
</dt> </dl>

 

 





