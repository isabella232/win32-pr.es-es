---
title: LVM_SETITEMCOUNT mensaje (Commctrl.h)
description: Hace que el control de vista de lista asigne memoria para el número especificado de elementos o establece el número virtual de elementos en un control de vista de lista virtual.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362694"
---
# <a name="lvm_setitemcount-message"></a>Mensaje \_ SETITEMCOUNT de LVM

Hace que el control list-view asigne memoria para el número especificado de elementos o establece el número virtual de elementos en un [control de vista de lista virtual](list-view-controls-overview.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que el control de vista de lista contendrá en última instancia.

</dd> <dt>

*lParam* 
</dt> <dd>

[Versión 4.70.](common-control-versions.md) Valores que especifican el comportamiento del control list-view después de restablecer el recuento de elementos. Este valor puede ser una combinación de lo siguiente:



| Value                                                                                                                                                                                    | Significado                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | El control list-view no se volverá a dibujar a menos que los elementos afectados estén actualmente en la vista.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOSCROLL**</dt> </dl>                      | El control list-view no cambiará la posición de desplazamiento cuando cambie el recuento de elementos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

La forma en que se asigna la memoria depende de cómo se haya creado el control list-view. Puede enviar este mensaje explícitamente o usar las macros [**\_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**ListView \_ SetItemCountEx de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) Para obtener más información, vea [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).

Si el control de vista de lista se creó sin el estilo [**LVS \_ OWNERDATA,**](list-view-window-styles.md) el envío de este mensaje hace que el control asigne sus estructuras de datos internas para el número especificado de elementos. Esto evita que el control tenga que asignar las estructuras de datos cada vez que se agrega un elemento.

Si el control list-view se creó con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) (una vista de lista virtual), el envío de este mensaje establece el número virtual de elementos que contiene el control.

El *parámetro lParam* está pensado solo para controles de vista de lista que usan los estilos [**LVS \_ OWNERDATA**](list-view-window-styles.md) y [**LVS \_ REPORT**](list-view-window-styles.md) o [**LVS \_ LIST.**](list-view-window-styles.md)

Cuando la vista de lista de control común es una vista de lista virtualizada [**(LVS \_ OWNERDATA),**](list-view-window-styles.md)hay un límite de 100 000 000 elementos en la vista de lista. En este escenario, **LVM \_ SETITEMCOUNT** devolverá FALSE cuando tenga un *wParam* de 100 000 001.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

