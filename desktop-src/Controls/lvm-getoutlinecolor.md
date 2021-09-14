---
title: LVM_GETOUTLINECOLOR mensaje (Commctrl.h)
description: Recupera el color del borde de un control de vista de lista si se establece el estilo de ventana extendida LVS \_ EX \_ BORDERSELECT.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- LVM_GETOUTLINECOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974084"
---
# <a name="lvm_getoutlinecolor-message"></a>Mensaje \_ LVM GETOUTLINECOLOR

Recupera el color del borde de un control de vista de lista si se establece el estilo de ventana extendida [**LVS \_ EX \_ BORDERSELECT.**](extended-list-view-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una **estructura COLORREF** que contiene el color del borde de un control de vista de lista.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





