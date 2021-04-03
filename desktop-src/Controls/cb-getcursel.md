---
title: Mensaje de CB_GETCURSEL (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETCURSEL para recuperar el índice del elemento seleccionado actualmente, si existe, en el cuadro de lista de un cuadro combinado.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905707"
---
# <a name="cb_getcursel-message"></a>\_Mensaje GETCURSEL CB

Una aplicación envía un mensaje **CB \_ GETCURSEL** para recuperar el índice del elemento seleccionado actualmente, si existe, en el cuadro de lista de un cuadro combinado.

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

El valor devuelto es el índice de base cero del elemento actualmente seleccionado. Si no hay ningún elemento seleccionado, se trata de un \_ error CB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> </dl>

 

 





