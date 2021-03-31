---
title: Mensaje de LVM_SETITEMCOUNT (commctrl. h)
description: Hace que el control de vista de lista asigne memoria para el número de elementos especificado o establece el número virtual de elementos en un control de vista de lista virtual.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150067"
---
# <a name="lvm_setitemcount-message"></a>\_Mensaje SETITEMCOUNT LVM

Hace que el control de vista de lista asigne memoria para el número de elementos especificado o establece el número virtual de elementos en un [control de vista de lista virtual](list-view-controls-overview.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que el control de vista de lista va a contener en última instancia.

</dd> <dt>

*lParam* 
</dt> <dd>

[Versión 4,70](common-control-versions.md). Valores que especifican el comportamiento del control de vista de lista después de restablecer el recuento de elementos. Este valor puede ser una combinación de lo siguiente:



| Value                                                                                                                                                                                    | Significado                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | El control de vista de lista no volverá a dibujar a menos que los elementos afectados estén actualmente en la vista.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOscroll**</dt> </dl>                      | El control de vista de lista no cambiará la posición de desplazamiento cuando cambie el número de elementos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

La forma en que se asigna la memoria depende de cómo se creó el control de vista de lista. Puede enviar este mensaje explícitamente o usar las macros [**\_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) de ListView. Para obtener más información, consulte [estilo de List-View virtual](/windows/desktop/Controls/list-view-controls-overview).

Si el control de vista de lista se creó sin el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , el envío de este mensaje hace que el control asigne sus estructuras de datos internas para el número de elementos especificado. Esto evita que el control tenga que asignar las estructuras de datos cada vez que se agrega un elemento.

Si el control de vista de lista se creó con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) (una vista de lista virtual), al enviar este mensaje se establece el número virtual de elementos que contiene el control.

El parámetro *lParam* solo está pensado para los controles de vista de lista que usan los estilos [**LVS \_ OWNERDATA**](list-view-window-styles.md) y [**LVS \_**](list-view-window-styles.md) o [**LVS \_ List**](list-view-window-styles.md) .

Cuando la vista de lista de controles comunes es una vista de lista virtualizada ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), hay un límite de 100 millones elementos en la vista de lista. En este escenario, **el \_ SETITEMCOUNT de LVM** devolverá FALSE cuando tenga un valor de *wParam* de 100.000.001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

