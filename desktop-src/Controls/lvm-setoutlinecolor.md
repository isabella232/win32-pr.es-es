---
title: LVM_SETOUTLINECOLOR mensaje (Commctrl.h)
description: Establece el color del borde de un control de vista de lista si se establece el estilo de ventana extendida LVS \_ EX \_ BORDERSELECT.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362675"
---
# <a name="lvm_setoutlinecolor-message"></a>Mensaje \_ SETOUTLINECOLOR de LVM

Establece el color del borde de un control de vista de lista si se establece el estilo de ventana extendida [**LVS \_ EX \_ BORDERSELECT.**](extended-list-view-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>**Estructura COLORREF** que especifica el color para establecer el borde.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **la estructura COLORREF** que contiene el color del contorno.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





