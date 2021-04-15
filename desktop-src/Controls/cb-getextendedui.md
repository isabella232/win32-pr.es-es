---
title: Mensaje de CB_GETEXTENDEDUI (Winuser. h)
description: Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490547"
---
# <a name="cb_getextendedui-message"></a>\_Mensaje GETEXTENDEDUI CB

Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.

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

Si el cuadro combinado tiene la interfaz de usuario extendida, el valor devuelto es **true**; de lo contrario, es **false**.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la tecla F4 abre o cierra la lista y la flecha hacia abajo cambia la selección actual. En un cuadro combinado con la interfaz de usuario extendida, la tecla F4 está deshabilitada y, al presionar la tecla flecha abajo, se abre la lista desplegable.

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

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





