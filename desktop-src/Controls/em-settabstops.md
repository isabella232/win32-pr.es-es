---
title: EM_SETTABSTOPS mensaje (Winuser.h)
description: El mensaje \_ EM SETTABSTOPS establece que la pestaña se detiene en un control de edición multilínea.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8285bbc8830f784b6cf2cf6671634bf4339a418c163bc3962150d6cb6674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048085"
---
# <a name="em_settabstops-message"></a>Mensaje \_ DE EM SETTABSTOPS

El **mensaje \_ EM SETTABSTOPS establece** que la pestaña se detiene en un control de edición multilínea. Cuando se copia texto en el control , cualquier carácter de tabulación del texto hace que se genere espacio hasta la siguiente detenerse.

Este mensaje solo se procesa mediante controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de tabulaciones contenidas en la matriz. Si este parámetro es cero, se omite el parámetro *lParam* y las tabulaciones predeterminadas se establecen en cada 32 unidades de plantilla de cuadro de diálogo. Si este parámetro es 1, las tabulaciones se establecen en cada *n* unidades de plantilla de diálogo, donde *n* es la distancia a la que apunta el *parámetro lParam.* Si este parámetro es mayor que 1, *lParam* es un puntero a una matriz de tabulaciones.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros sin signo que especifica las tabulaciones, en unidades de plantilla de cuadro de diálogo. Si el *parámetro wParam* es 1, este parámetro es un puntero a un entero sin signo que contiene la distancia entre todas las tabulaciones, en unidades de plantilla de cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se establecen todas las pestañas, el valor devuelto es **TRUE.**

Si no se establecen todas las pestañas, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

El **mensaje \_ EM SETTABSTOPS** no vuelve a dibujar automáticamente la ventana de control de edición. Si la aplicación cambia las tabulaciones para el texto que ya está en el control de edición, debe llamar a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para volver a dibujar la ventana de control de edición.

Los valores especificados en la matriz están en unidades de plantilla de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo. Para convertir medidas de unidades de plantilla de diálogo en unidades de pantalla (píxeles), use la [**función MapDialogRect.**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)

**Edición enriquecte:** Compatible con Microsoft Rich Edit 3.0 y versiones posteriores. Un control de edición enriquecido puede tener el número máximo de tabulaciones especificadas por MAX \_ TAB \_ STOPS. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

