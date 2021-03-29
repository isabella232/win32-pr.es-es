---
title: Mensaje de PGM_SETSCROLLINFO (commctrl. h)
description: Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro SetScrollInfo de buscapersonas \_ .
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905171"
---
# <a name="pgm_setscrollinfo-message"></a>\_Mensaje SETSCROLLINFO PGM

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que este mensaje no se admita en versiones futuras de Windows.\]

Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollInfo de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Uint** que especifica el valor de tiempo de espera para el desplazamiento, en milisegundos.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **uint** que especifica el número de líneas que se va a desplazar por tiempo de espera. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **uint** que especifica el número de píxeles por línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

El valor de tiempo de espera de *wParam* controla la velocidad a la que el control de paginación genera eventos de desplazamiento cuando el control ha capturado la entrada del mouse y se presiona el botón primario del mouse. Los valores más pequeños dan como resultado un desplazamiento más rápido; los valores más grandes producen un desplazamiento más lento. El valor predeterminado es un octavo de la hora de doble clic. Para obtener más información, vea [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).

De forma predeterminada, con cada evento de desplazamiento, el control de paginación desplaza una cantidad igual a todo el ancho o alto del control, en función de si el control de paginación tiene una orientación horizontal o vertical. Los valores de *lParam* se utilizan para invalidar la cantidad de desplazamiento predeterminada. Si se proporcionan valores distintos de cero, la cantidad de desplazamiento es el producto de los dos valores (LOWORD (*lParam*) \* HIWORD (*lParam*)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Buscapersonas \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

