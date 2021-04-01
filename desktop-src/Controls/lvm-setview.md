---
title: Mensaje de LVM_SETVIEW (commctrl. h)
description: Establece la vista de un control de vista de lista.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150880"
---
# <a name="lvm_setview-message"></a>\_Mensaje SETVIEW LVM

Establece la vista de un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** que especifica la vista.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente, o-1 en caso contrario. Por ejemplo, se devuelve-1 si la vista no es válida.

## <a name="remarks"></a>Observaciones

A continuación se muestran los valores de las vistas.

-   detalles de la \_ vista LV \_
-   \_icono de vista de LV \_
-   \_lista de vistas de LV \_
-   visualización de la vista de LV \_ \_
-   \_icono de vista de LV \_

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





