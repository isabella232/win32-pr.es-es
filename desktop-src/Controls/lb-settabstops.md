---
title: LB_SETTABSTOPS mensaje (Winuser.h)
description: Establece las posiciones de tabulación en un cuadro de lista.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d842b0c7e2cdcc792227ecb390fa3bc2a4c9d210b7c028b266c867a0c473808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085325"
---
# <a name="lb_settabstops-message"></a>Mensaje \_ DE LB SETTABSTOPS

Establece las posiciones de tabulación en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número de tabulaciones.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al primer miembro de una matriz de enteros que contiene las tabulaciones. Los enteros representan el número de trimestres del ancho medio de caracteres de la fuente seleccionada en el cuadro de lista. Por ejemplo, un detente de tabulación de 4 se coloca en 1,0 unidades de caracteres y un tabulador de 6 se coloca en 1,5 unidades de carácter promedio. Sin embargo, si el cuadro de lista forma parte de un cuadro de diálogo, los enteros se encuentran en unidades de plantilla de diálogo. Las tabulaciones deben ordenarse en orden ascendente; no se permiten las pestañas anteriores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se establecen todas las pestañas especificadas, el valor devuelto es **TRUE**; de lo contrario, es **FALSE.**

## <a name="remarks"></a>Comentarios

Para responder al mensaje **\_ LB SETTABSTOPS,** el cuadro de lista debe haber sido creado con el estilo [**\_ USETABSTOPS de LB.**](list-box-styles.md)

Si *wParam es* 0 y *lParam* **es NULL,** la tabulación predeterminada es dos unidades de plantilla de diálogo. Si *wParam* es 1, el cuadro de lista tendrá tabulaciones separadas por la distancia especificada por *lParam.*

Si *lParam* apunta a más de un valor único, se establecerá una tabulación para cada valor de *lParam,* hasta el número especificado por *wParam*.

Los valores especificados por *lParam* se encuentran en unidades de plantilla de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo. Para convertir medidas de unidades de plantilla de diálogo en unidades de pantalla (píxeles), use la [**función MapDialogRect.**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)

Windows 95/Windows 98/Windows Edition (Windows Me): el búfer al que apunta *lParam* debe residir en memoria grabable, aunque el mensaje no modifique la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

