---
title: EM_GETTEXTRANGE mensaje (Richedit.h)
description: Recupera un intervalo especificado de caracteres de un control de edición enriquecido.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12282b970c38164e5b28a31ed778a3320f88bbdf16b6d182586e492e5e699eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006580"
---
# <a name="em_gettextrange-message"></a>Mensaje \_ EM GETTEXTRANGE

Recupera un intervalo especificado de caracteres de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) que especifica el intervalo de caracteres que se van a recuperar y un búfer en el que copiar los caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve el número de caracteres copiados, sin incluir el carácter nulo final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Textrange**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





