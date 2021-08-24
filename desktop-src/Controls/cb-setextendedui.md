---
title: CB_SETEXTENDEDUI mensaje (Winuser.h)
description: Una aplicación envía un mensaje CB SETEXTENDEDUI para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo CBS DROPDOWN o \_ \_ CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI controles de Windows mensaje
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
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414227"
---
# <a name="cb_setextendedui-message"></a>Mensaje \_ DE CB SETEXTENDEDUI

Una aplicación envía un mensaje **CB \_ SETEXTENDEDUI** para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **BOOL** que especifica si el cuadro combinado usa la interfaz de usuario extendida (**TRUE**) o la interfaz de usuario predeterminada (**FALSE**).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es CB \_ OKAY. Si se produce un error, es CB \_ ERR.

## <a name="remarks"></a>Comentarios

De forma predeterminada, la tecla F4 abre o cierra la lista y la FLECHA ABAJO cambia la selección actual. En la interfaz de usuario extendida, la tecla F4 está deshabilitada y la tecla FLECHA ABAJO abre la lista desplegable. La rueda del mouse, que normalmente se desplaza por los elementos de la lista, no tiene ningún efecto cuando se establece la interfaz de usuario extendida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





