---
title: Mensaje de CB_SETHORIZONTALEXTENT (Winuser. h)
description: Una aplicación envía el \_ mensaje CB SETHORIZONTALEXTENT para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490522"
---
# <a name="cb_sethorizontalextent-message"></a>\_Mensaje SETHORIZONTALEXTENT CB

Una aplicación envía el mensaje **CB \_ SETHORIZONTALEXTENT** para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable). Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal se desplaza horizontalmente por los elementos del cuadro de lista. Si el ancho del cuadro de lista es igual o mayor que este valor, la barra de desplazamiento horizontal está oculta o, si el cuadro combinado tiene el [**estilo \_ DISABLENOSCROLL de CBS**](combo-box-styles.md) , deshabilitado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el ancho desplazable del cuadro de lista, en píxeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ GETHORIZONTALEXTENT**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





