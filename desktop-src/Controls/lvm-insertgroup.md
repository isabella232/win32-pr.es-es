---
title: Mensaje de LVM_INSERTGROUP (commctrl. h)
description: Inserta un grupo en un control de vista de lista.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658332"
---
# <a name="lvm_insertgroup-message"></a>\_Mensaje INSERTGROUP LVM

Inserta un grupo en un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Índice en el que se va a agregar el grupo. Si es-1, el grupo se agrega al final de la lista.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que contiene el grupo que se va a agregar.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento al que se agregó el grupo o-1 si se produjo un error en la operación.

## <a name="remarks"></a>Observaciones

Para activar el modo de grupo, llame a [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

No se puede insertar un grupo en un control de vista de lista vacío.

Asegúrese de establecer el valor de **iGroupId** en los elementos a los que se agregó el grupo. De lo contrario, después del procesamiento de mensajes [**\_ ENABLEGROUPVIEW LVM**](lvm-enablegroupview.md) con **true** , el control ListView no mostrará ningún elemento.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique la versión 6,0 de Comclt32. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





