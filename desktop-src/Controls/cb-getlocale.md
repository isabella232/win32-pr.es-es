---
title: CB_GETLOCALE mensaje (Winuser.h)
description: Obtiene la configuración regional actual del cuadro combinado. La configuración regional se usa para determinar el criterio de ordenación correcto del texto mostrado para los cuadros combinados con el estilo SORT de CBS y el texto agregados mediante el mensaje \_ \_ ADDSTRING de CB.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e2a5ff4de25739f9c5d5eac75868cf2d506c4d8a280744d1b1056f8de49e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006779"
---
# <a name="cb_getlocale-message"></a>Mensaje \_ GETLOCALE de CB

Obtiene la configuración regional actual del cuadro combinado. La configuración regional se usa para determinar el criterio de ordenación correcto del texto mostrado para los cuadros combinados con el estilo SORT de [**CBS \_**](combo-box-styles.md) y el texto agregados mediante el mensaje [**\_ ADDSTRING de CB.**](cb-addstring.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la configuración regional actual del cuadro combinado. HIWORD [**contiene el**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) código de país o región y [**loWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de idioma.

## <a name="remarks"></a>Comentarios

El identificador de idioma se forma de un identificador de sublenguaje y un identificador de idioma principal. La [**macro PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) obtiene el identificador de idioma principal y la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) obtiene el identificador de subidioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ SETLOCALE**](cb-setlocale.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

