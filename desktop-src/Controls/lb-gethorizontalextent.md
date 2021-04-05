---
title: Mensaje de LB_GETHORIZONTALEXTENT (Winuser. h)
description: Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997030"
---
# <a name="lb_gethorizontalextent-message"></a>\_Mensaje lb GETHORIZONTALEXTENT

Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.

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

El valor devuelto es el ancho desplazable, en píxeles, del cuadro de lista.

## <a name="remarks"></a>Observaciones

Para responder al mensaje de **lb \_ GETHORIZONTALEXTENT** , el cuadro de lista se debe haber definido con el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Si la aplicación no establece la extensión horizontal del cuadro de lista (con [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), la extensión horizontal predeterminada es cero. Tenga en cuenta que el cuadro de lista no actualiza dinámicamente su extensión horizontal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

