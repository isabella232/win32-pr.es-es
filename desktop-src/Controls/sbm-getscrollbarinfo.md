---
title: SBM_GETSCROLLBARINFO mensaje (Winuser.h)
description: Enviado por una aplicación para recuperar información sobre la barra de desplazamiento especificada.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f779f237d0ad04fe3e3d8f3348c51c195470280c9b0c20d12c1e245d04a089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503985"
---
# <a name="sbm_getscrollbarinfo-message"></a>Mensaje \_ SBM GETSCROLLBARINFO

Enviado por una aplicación para recuperar información sobre la barra de desplazamiento especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) que recibe la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero en caso contrario.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

