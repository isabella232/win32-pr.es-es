---
title: LVM_SETVIEW mensaje (Commctrl.h)
description: Establece la vista de un control list-view.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362647"
---
# <a name="lvm_setview-message"></a>Mensaje \_ SETVIEW de LVM

Establece la vista de un control list-view.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** que especifica la vista.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente o -1 en caso contrario. Por ejemplo, se devuelve -1 si la vista no es válida.

## <a name="remarks"></a>Observaciones

A continuación se encuentran los valores de las vistas.

-   DETALLES \_ DE LA VISTA DE \_ LV
-   ICONO \_ DE VISTA DE \_ LV
-   LV \_ VIEW \_ LIST
-   LV \_ VIEW \_ SMALLICON
-   ICONO \_ LV VIEW \_

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





