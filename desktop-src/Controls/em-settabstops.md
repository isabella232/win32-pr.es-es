---
title: Mensaje de EM_SETTABSTOPS (Winuser. h)
description: El \_ mensaje SETTABSTOPS em establece las tabulaciones en un control de edición multilínea.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS controles de mensajes de Windows
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
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150463"
---
# <a name="em_settabstops-message"></a>\_Mensaje SETTABSTOPS em

El **mensaje \_ SETTABSTOPS em** establece las tabulaciones en un control de edición multilínea. Cuando se copia texto en el control, cualquier carácter de tabulación del texto hace que se genere espacio hasta la siguiente tabulación.

Este mensaje solo lo procesan los controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de tabulaciones contenidas en la matriz. Si este parámetro es cero, el parámetro *lParam* se omite y las tabulaciones predeterminadas se establecen en cada unidad de plantilla de cuadro de diálogo 32. Si este parámetro es 1, las tabulaciones se establecen en cada *n* unidades de plantilla de cuadro de diálogo, donde *n* es la distancia a la que apunta el parámetro *lParam* . Si este parámetro es mayor que 1, *lParam* es un puntero a una matriz de puntos de tabulación.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros sin signo que especifican las tabulaciones, en unidades de plantilla de cuadro de diálogo. Si el parámetro *wParam* es 1, este parámetro es un puntero a un entero sin signo que contiene la distancia entre todas las tabulaciones, en unidades de plantilla de cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se establecen todas las pestañas, el valor devuelto es **true**.

Si no se establecen todas las pestañas, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

El **mensaje \_ SETTABSTOPS em** no vuelve a dibujar automáticamente la ventana de control de edición. Si la aplicación está cambiando las tabulaciones del texto que ya está en el control de edición, debe llamar a la función [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para volver a dibujar la ventana de control de edición.

Los valores especificados en la matriz se encuentran en unidades de plantilla de cuadro de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo. Para convertir las medidas de las unidades de plantilla de cuadro de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 3,0 y versiones posteriores. Un control Rich Edit puede tener el número máximo de tabulaciones especificado por las tabulaciones MAX \_ \_ . Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

