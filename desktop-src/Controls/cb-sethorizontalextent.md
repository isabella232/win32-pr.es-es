---
title: CB_SETHORIZONTALEXTENT mensaje (Winuser.h)
description: Una aplicación envía el mensaje CB SETHORIZONTALEXTENT para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar \_ horizontalmente (el ancho desplazable).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT controles de Windows mensaje
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
ms.openlocfilehash: c8aac1fc0d10a38b292a4f37b3b170060d7e76ef5c8d303f39180b3f5063ffee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089025"
---
# <a name="cb_sethorizontalextent-message"></a>Mensaje \_ CB SETHORIZONTALEXTENT

Una aplicación envía el mensaje **\_ CB SETHORIZONTALEXTENT** para establecer el ancho, en píxeles, por el que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable). Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal desplaza horizontalmente los elementos del cuadro de lista. Si el ancho del cuadro de lista es igual o mayor que este valor, la barra de desplazamiento horizontal está oculta o, si el cuadro combinado tiene el estilo [**\_ DISABLENOSCROLL de CBS,**](combo-box-styles.md) deshabilitado.

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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ GETHORIZONTALEXTENT**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





