---
title: LB_GETLOCALE mensaje (Winuser.h)
description: Obtiene la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo SORT de LBS) y del texto agregado por el mensaje \_ \_ ADDSTRING de LB.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544525"
---
# <a name="lb_getlocale-message"></a>Mensaje \_ GETLOCALE de LB

Obtiene la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo [**\_ SORT de LBS)**](list-box-styles.md) y del texto agregado por el mensaje [**\_ ADDSTRING de LB.**](lb-addstring.md)

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

El valor devuelto especifica la configuración regional actual del cuadro de lista. HIWORD [**contiene el**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) código de país o región y [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de idioma.

## <a name="remarks"></a>Comentarios

El identificador de idioma consta de un identificador de sublenguaje y un identificador de idioma principal. Use la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) para extraer el identificador de idioma principal del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valor devuelto y la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) para extraer el identificador de subidioma.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

