---
title: Mensaje de LVM_SETCOLUMNWIDTH (commctrl. h)
description: Cambia el ancho de una columna en el modo de vista de informe o el ancho de todas las columnas en el modo de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetColumnWidth de ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149899"
---
# <a name="lvm_setcolumnwidth-message"></a>\_Mensaje SETCOLUMNWIDTH LVM

Cambia el ancho de una columna en el modo de vista de informe o el ancho de todas las columnas en el modo de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetColumnWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de una columna válida. En el modo de vista de lista, este parámetro debe establecerse en cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo ancho de la columna, en píxeles. En el modo de vista de informe, se admiten los siguientes valores especiales:



| Value                                                                                                                                                                                           | Significado                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**AutoSize de LVSCW \_**</dt> </dl>                                | Ajusta automáticamente el tamaño de la columna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AutoSize \_ USEHEADER**</dt> </dl> | Ajusta el tamaño de la columna automáticamente para que quepa el texto del encabezado. Si usa este valor con la última columna, su ancho se establece para rellenar el ancho restante del control de vista de lista.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Suponga que tiene un control de vista de lista de 2 columnas con un ancho de 500 píxeles. Si el ancho de la columna cero se establece en 200 píxeles y se envía este mensaje con *wParam* = 1 y *lParam* = LVSCW \_ AutoSize \_ USEHEADER, la segunda columna (y la última) será de 300 píxeles de ancho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





