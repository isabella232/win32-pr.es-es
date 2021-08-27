---
title: CB_GETCOMBOBOXINFO mensaje (Winuser.h)
description: Obtiene información sobre el cuadro combinado especificado.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ce6227df0031c01b15892daa14eea9cc8d25bd2c7eede68af275063d7201505
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089295"
---
# <a name="cb_getcomboboxinfo-message"></a>Mensaje \_ CB GETCOMBOBOXINFO

Obtiene información sobre el cuadro combinado especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Puntero a una [**estructura COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) que recibe la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Este mensaje es equivalente a [**GetComboBoxInfo.**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)

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

[**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

