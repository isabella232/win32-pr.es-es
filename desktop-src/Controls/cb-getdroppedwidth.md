---
title: CB_GETDROPPEDWIDTH mensaje (Winuser.h)
description: Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el estilo DROPDOWN o \_ \_ CBS DROPDOWNLIST de CBS.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062549"
---
# <a name="cb_getdroppedwidth-message"></a>Mensaje \_ CB GETDROPPEDWIDTH

Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el estilo DROPDOWN o [**\_ CBS DROPDOWNLIST de CBS.**](combo-box-styles.md) [**\_**](combo-box-styles.md)

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

Si el mensaje se realiza correctamente, el valor devuelto es el ancho, en píxeles.

Si se produce un error en el mensaje, el valor devuelto es CB \_ ERR.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el ancho mínimo permitido del cuadro de lista desplegable es cero. El ancho del cuadro de lista es el ancho mínimo permitido o el ancho del cuadro combinado, el que sea mayor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





