---
title: LVM_SETINFOTIP mensaje (Commctrl.h)
description: Establece el texto de la información sobre herramientas en respuesta retrasada a la \_ notificación GETINFOTIP de LVN.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362710"
---
# <a name="lvm_setinfotip-message"></a>Mensaje \_ SETINFOTIP de LVM

Establece el texto de la información sobre herramientas en respuesta retrasada a [la \_ notificación GETINFOTIP de LVN.](lvn-getinfotip.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">estructura LVSETINFOTIP</a> que contiene la información que se debe establecer.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el texto de la información sobre herramientas se establece correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El **mensaje LVM \_ SETINFOTIP permite** que una aplicación calcule información sobre información en segundo plano mediante los pasos siguientes:

1.  En respuesta a la [notificación \_ LVN GETINFOTIP,](lvn-getinfotip.md) establezca el miembro **pszText** de la estructura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) en una cadena vacía y devuelva 0.
2.  En segundo plano, calcule la información.
3.  Después de calcular la información, envíe el mensaje **LVM \_ SETINFOTIP** y establezca el miembro **pszText** de la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) en la información y los miembros **iItem** e **iSubItem** al elemento y subelemento al que se aplica la información.

El texto que se pasa al mensaje **\_ SETINFOTIP** de LVM solo aparece si el elemento y el sub item descritos por la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) siguen en un estado que requiere información

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





