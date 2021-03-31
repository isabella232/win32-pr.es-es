---
title: Mensaje de CB_GETDROPPEDWIDTH (Winuser. h)
description: Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con la lista \_ desplegable CBS o el estilo de DROPDOWNLIST de CBS \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079370"
---
# <a name="cb_getdroppedwidth-message"></a>\_Mensaje GETDROPPEDWIDTH CB

Obtiene el ancho mínimo permitido, en píxeles, del cuadro de lista de un cuadro combinado con la lista [**\_ desplegable CBS**](combo-box-styles.md) o el estilo de [**\_ DROPDOWNLIST de CBS**](combo-box-styles.md) .

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

Si el mensaje se realiza correctamente, el valor devuelto es el ancho, en píxeles.

Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el ancho mínimo permitido del cuadro de lista desplegable es cero. El ancho del cuadro de lista es el ancho mínimo permitido o el ancho del cuadro combinado, el que sea mayor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





