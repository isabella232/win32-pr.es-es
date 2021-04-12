---
title: Mensaje de HKM_GETHOTKEY (commctrl. h)
description: Obtiene el código de tecla virtual y los marcadores modificadores de una tecla de acceso rápido de un control de tecla de acceso rápido.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490211"
---
# <a name="hkm_gethotkey-message"></a>HKM \_ GETHOTKEY

Obtiene el código de tecla virtual y los marcadores modificadores de una tecla de acceso rápido de un control de tecla de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el código de tecla virtual y los marcadores de modificador. El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de tecla virtual de la tecla de acceso rápido. El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que especifica las teclas que definen una combinación de teclas de acceso rápido. Las marcas modificadoras pueden ser una combinación de los valores siguientes.



| Value            | Significado      |
|------------------|--------------|
| HOTKEYF \_ Alt     | tecla ALT      |
| \_control HOTKEYF | Tecla CONTROL  |
| \_ext HOTKEYF     | Clave extendida |
| HOTKEYF \_ Shift   | Tecla Mayús    |



 

## <a name="remarks"></a>Observaciones

El valor de 16 bits devuelto por este mensaje se puede usar como parámetro *wParam* en el mensaje de [**\_ SETHOTKEY de WM**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

