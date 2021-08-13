---
title: HKM_SETHOTKEY mensaje (Commctrl.h)
description: Establece la combinación de teclas de acceso automático para un control de tecla de acceso.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY controles de Windows mensaje
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae397e3034e917eec85a6b56397cbac8b14a59af03aca6ebee08fec89cf6b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672263"
---
# <a name="hkm_sethotkey-message"></a>Mensaje SETHOTKEY de HKM \_

Establece la combinación de teclas de acceso automático para un control de tecla de acceso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de clave virtual de la tecla de acceso. El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que indica las claves que definen una combinación de teclas de acceso rápido. Para obtener una lista de valores de marca modificadoras, vea la descripción del [**mensaje \_ GETHOTKEY de HKM.**](hkm-gethotkey.md)

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

