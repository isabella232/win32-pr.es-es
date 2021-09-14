---
title: LVM_SETCOLUMNWIDTH mensaje (Commctrl.h)
description: Cambia el ancho de una columna en modo de vista de informe o el ancho de todas las columnas en modo de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro SetColumnWidth de ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974068"
---
# <a name="lvm_setcolumnwidth-message"></a>Mensaje \_ SETCOLUMNWIDTH de LVM

Cambia el ancho de una columna en modo de vista de informe o el ancho de todas las columnas en modo de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetColumnWidth de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de una columna válida. Para el modo de vista de lista, este parámetro debe establecerse en cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo ancho de la columna, en píxeles. Para el modo de vista de informe, se admiten los siguientes valores especiales:



| Value                                                                                                                                                                                           | Significado                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**LVSCW \_ AUTOSIZE**</dt> </dl>                                | Ajusta automáticamente el tamaño de la columna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | Ajusta automáticamente el tamaño de la columna para que se ajuste al texto del encabezado. Si usa este valor con la última columna, su ancho se establece para rellenar el ancho restante del control de vista de lista.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Supongamos que tiene un control list-view de 2 columnas con un ancho de 500 píxeles. Si el ancho de la columna cero se establece en 200 píxeles y envía este mensaje con *wParam* = 1 y *lParam* = LVSCW AUTOSIZE USEHEADER, la segunda (y la última) columna tendrá \_ \_ 300 píxeles de ancho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





