---
title: Mensaje de CB_LIMITTEXT (Winuser. h)
description: Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079359"
---
# <a name="cb_limittext-message"></a>\_Mensaje LIMITTEXT CB

Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de **TCHARs** que puede escribir el usuario, sin incluir el carácter nulo de terminación. Si este parámetro es cero, la longitud del texto se limita a caracteres 0x7FFFFFFE.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **true**.

## <a name="remarks"></a>Observaciones

Si el cuadro combinado no tiene el estilo [**\_ AUTOHSCROLL de CBS**](combo-box-styles.md) , establecer el límite de texto en un valor mayor que el tamaño del control de edición no tiene ningún efecto.

El mensaje **CB \_ LIMITTEXT** limita solo el texto que el usuario puede escribir. No tiene ningún efecto en ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición cuando se selecciona una cadena en el cuadro de lista.

El límite predeterminado para el texto que un usuario puede escribir en el control de edición es 30.000 **TCHARs**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





