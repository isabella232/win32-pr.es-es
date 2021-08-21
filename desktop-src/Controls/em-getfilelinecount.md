---
title: EM_GETFILELINECOUNT mensaje (CommCtrl.h)
description: Obtiene el número de líneas de un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT controles de Windows mensaje
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
ms.openlocfilehash: 28539af32212a699e12d2cf1d1787fa2e7aaa224f374eb6a63717279fcad16b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019683"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>EM_GETFILELINECOUNT mensaje (CommCtrl.h)

Obtiene el número de líneas de un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla. Si el control no tiene texto, el valor devuelto es 1. El valor devuelto nunca será menor que 1.

## <a name="remarks"></a>Comentarios

El **mensaje EM \_ GETFILELINECOUNT** recupera el número total de líneas de texto, independientemente de cómo se muestren las líneas en la pantalla, no solo el número de líneas que están visibles actualmente.

El ajuste de línea no cambia el número de líneas que devuelve este mensaje, ya que este mensaje funciona independientemente de cómo se muestran las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETFILELINE**](em-getfileline.md)
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





