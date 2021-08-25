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
ms.openlocfilehash: dd8d07b636a14624632d0e41ebcf6db66f420b9df4f8ca852e55ab2f3e1578e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656205"
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

## <a name="remarks"></a>Comentarios

A continuación se encuentran los valores de las vistas.

-   DETALLES \_ DE LA VISTA DE \_ LV
-   ICONO \_ DE VISTA DE \_ LV
-   LV \_ VIEW \_ LIST
-   LV \_ VIEW \_ SMALLICON
-   ICONO \_ LV VIEW \_

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





