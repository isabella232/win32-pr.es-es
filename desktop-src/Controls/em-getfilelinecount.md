---
title: Mensaje de EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtiene el número de líneas de un control de edición de varias líneas, independientemente de cómo se muestran las líneas en la pantalla.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150670"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>Mensaje de EM_GETFILELINECOUNT (CommCtrl. h)

Obtiene el número de líneas de un control de edición de varias líneas, independientemente de cómo se muestran las líneas en la pantalla.

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

El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición de varias líneas, independientemente de cómo se muestren las líneas en la pantalla. Si el control no tiene texto, el valor devuelto es 1. El valor devuelto nunca será menor que 1.

## <a name="remarks"></a>Observaciones

El **mensaje \_ GETFILELINECOUNT em** recupera el número total de líneas de texto, independientemente de cómo se muestren las líneas en la pantalla, no solo el número de líneas que están visibles actualmente.

El ajuste automático de línea no cambia el número de líneas que devuelve este mensaje, ya que este mensaje funciona independientemente del modo en que se muestran las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETFILELINE em**](em-getfileline.md)
</dt> <dt>

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





