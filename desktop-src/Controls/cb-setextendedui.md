---
title: Mensaje de CB_SETEXTENDEDUI (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETEXTENDEDUI para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo de la \_ lista desplegable CBS o CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490528"
---
# <a name="cb_setextendedui-message"></a>\_Mensaje SETEXTENDEDUI CB

Una aplicación envía un mensaje **CB \_ SETEXTENDEDUI** para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo de la [**\_ lista desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un valor **booleano** que especifica si el cuadro combinado usa la interfaz de usuario extendida (**true**) o la interfaz de usuario predeterminada (**false**).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es CB de \_ acuerdo. Si se produce un error, es CB \_ error.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la tecla F4 abre o cierra la lista y la flecha hacia abajo cambia la selección actual. En la interfaz de usuario extendida, la tecla F4 está deshabilitada y la tecla flecha abajo abre la lista desplegable. La rueda del mouse, que normalmente se desplaza por los elementos de la lista, no tiene ningún efecto cuando se establece la interfaz de usuario extendida.

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

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





