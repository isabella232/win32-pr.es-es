---
title: Mensaje de SBM_SETRANGE (Winuser. h)
description: El \_ mensaje SBM SetRange se envía para establecer los valores de posición mínimo y máximo del control de barra de desplazamiento.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905554"
---
# <a name="sbm_setrange-message"></a>\_Mensaje SBM SetRange

El mensaje **SBM \_ SetRange** se envía para establecer los valores de posición mínimo y máximo del control de barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollRange** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la posición de desplazamiento mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la posición de desplazamiento máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**ComCtl32.dll versión 5,0**: Si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento. de lo contrario, es cero.

**ComCtl32.dll versión 6,0**: la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.

## <a name="remarks"></a>Observaciones

Los valores de posición mínimo y máximo predeterminados son cero. La diferencia entre los valores especificados por los parámetros *wParam* e *lParam* no debe ser mayor que MAXLONG.

Si los valores de posición mínimo y máximo son iguales, el control de barra de desplazamiento se oculta y, en efecto, se deshabilita.

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

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

