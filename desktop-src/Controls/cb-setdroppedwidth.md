---
title: CB_SETDROPPEDWIDTH mensaje (Winuser.h)
description: Una aplicación envía el mensaje CB SETDROPPEDWIDTH para establecer el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el estilo DROPDOWN o \_ \_ CBS DROPDOWNLIST de \_ CBS.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062233"
---
# <a name="cb_setdroppedwidth-message"></a>Mensaje \_ CB SETDROPPEDWIDTH

Una aplicación envía el mensaje **\_ CB SETDROPPEDWIDTH** para establecer el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con el estilo DROPDOWN o [**\_ CBS DROPDOWNLIST**](combo-box-styles.md) de [**CBS. \_**](combo-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ancho mínimo permitido del cuadro de lista, en píxeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el nuevo ancho del cuadro de lista.

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

[**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





