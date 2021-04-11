---
title: Mensaje de CB_GETLOCALE (Winuser. h)
description: Obtiene la configuración regional actual del cuadro combinado. La configuración regional se usa para determinar el criterio de ordenación correcto del texto que se muestra en los cuadros combinados con el \_ estilo de ordenación CBS y el texto agregado mediante el \_ mensaje CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE controles de mensajes de Windows
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
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079363"
---
# <a name="cb_getlocale-message"></a>Mensaje de error de CB. \_

Obtiene la configuración regional actual del cuadro combinado. La configuración regional se usa para determinar el criterio de ordenación correcto del texto que se muestra en los cuadros combinados con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) y el texto agregado mediante el mensaje [**CB \_ ADDSTRING**](cb-addstring.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la configuración regional actual del cuadro combinado. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el código de país o región y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de idioma.

## <a name="remarks"></a>Observaciones

El identificador de idioma se compone de un identificador de subidioma y un identificador de idioma principal. La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) obtiene el identificador de idioma principal y la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) obtiene el identificador de subidioma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

