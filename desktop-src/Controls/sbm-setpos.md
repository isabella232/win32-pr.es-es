---
title: Mensaje de SBM_SETPOS (Winuser. h)
description: El \_ mensaje SBM SETPOS se envía para establecer la posición del cuadro de desplazamiento (Thumb) y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493048"
---
# <a name="sbm_setpos-message"></a>\_Mensaje SETPOS SBM

El mensaje **SBM \_ SETPOS** se envía para establecer la posición del cuadro de desplazamiento (Thumb) y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollPos** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la nueva posición del cuadro de desplazamiento. Debe encontrarse dentro del intervalo de desplazamiento. Si este parámetro está fuera del intervalo de desplazamiento, el valor se redondea hacia arriba o hacia abajo al valor válido más próximo.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si la barra de desplazamiento debe volver a dibujarse para reflejar la nueva posición del cuadro de desplazamiento. Si este parámetro es **true**, se vuelve a dibujar la barra de desplazamiento. Si es **false**, la barra de desplazamiento no se vuelve a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**ComCtl32.dll versión 5,0**: Si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento. de lo contrario, es cero.

**ComCtl32.dll versión 6,0**: la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.

## <a name="remarks"></a>Observaciones

Si el control de barra de desplazamiento se vuelve a dibujar mediante una llamada subsiguiente a otra función, resulta útil establecer el parámetro *lParam* en **false** .

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

[**SBM \_ SetRange**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

