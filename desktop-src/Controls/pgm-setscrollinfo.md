---
title: PGM_SETSCROLLINFO mensaje (Commctrl.h)
description: Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro Pager \_ SetScrollInfo.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167673"
---
# <a name="pgm_setscrollinfo-message"></a>Mensaje \_ SETCROLLINFO de PGM

\[Destinado a uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro [**Pager \_ SetScrollInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

UINT **que** especifica el valor de tiempo de espera para el desplazamiento, en milisegundos.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **UINT** que especifica el número de líneas que se desplazarán por tiempo de espera. [**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **UINT** que especifica el número de píxeles por línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="security-considerations"></a>Consideraciones de seguridad

El uso de este mensaje puede poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

El valor de tiempo de espera *wParam* controla la velocidad a la que el control de paginación genera eventos de desplazamiento cuando el control ha capturado la entrada del mouse y se presiona el botón izquierdo del mouse. Los valores más pequeños darán lugar a un desplazamiento más rápido; Los valores mayores tienen como resultado un desplazamiento más lento. El valor predeterminado es un octavo del tiempo de doble clic. Para obtener más información, [**vea GetDoubleClickTime.**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime)

De forma predeterminada, con cada evento de desplazamiento, el control de paginación desplaza una cantidad igual a todo el ancho o alto del control, en función de si el control de paginación tiene una orientación horizontal o vertical. Los valores de *lParam* se usan para invalidar la cantidad de desplazamiento predeterminada. Si se proporcionan valores distintos de cero, la cantidad de desplazamiento es el producto de los dos valores (LOWORD(*lParam*) \* HIWORD(*lParam*)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Pager \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

