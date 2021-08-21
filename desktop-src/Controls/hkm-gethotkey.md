---
title: HKM_GETHOTKEY mensaje (Commctrl.h)
description: Obtiene el código de clave virtual y las marcas modificadoras de una tecla de acceso remoto de un control de tecla de acceso.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY controles de Windows mensaje
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
ms.openlocfilehash: 79bfbad1eb5e9a6679a1b3e419a0877e61cd90247ef0cf91b0a30c655f755a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672273"
---
# <a name="hkm_gethotkey-message"></a>Mensaje GETHOTKEY de HKM \_

Obtiene el código de clave virtual y las marcas modificadoras de una tecla de acceso remoto de un control de tecla de acceso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el código de clave virtual y las marcas modificadoras. El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de clave virtual de la tecla de acceso. El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que especifica las claves que definen una combinación de teclas de acceso rápido. Las marcas modificadoras pueden ser una combinación de los valores siguientes.



| Value            | Significado      |
|------------------|--------------|
| HOTKEYF \_ ALT     | tecla ALT      |
| HOTKEYF \_ (CONTROL) | Tecla CONTROL  |
| HOTKEYF \_ EXT     | Clave extendida |
| HOTKEYF \_ MAYÚS   | Tecla MAYÚS    |



 

## <a name="remarks"></a>Observaciones

El valor de 16 bits devuelto por este mensaje se puede usar como parámetro *wParam* en el [**mensaje \_ SETHOTKEY de WM.**](/windows/desktop/inputdev/wm-sethotkey)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

