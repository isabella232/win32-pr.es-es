---
title: CB_LIMITTEXT mensaje (Winuser.h)
description: Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT controles de Windows mensaje
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
ms.openlocfilehash: 3e94cdb1bedfb1c0aa3efb401649524782183ced7728304951596c9383efaa0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089085"
---
# <a name="cb_limittext-message"></a>Mensaje \_ LIMITTEXT de CB

Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de **TCHAR que** el usuario puede especificar, sin incluir el carácter nulo de terminación. Si este parámetro es cero, la longitud del texto se limita a 0x7FFFFFFE caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **TRUE.**

## <a name="remarks"></a>Comentarios

Si el cuadro combinado no tiene el estilo [**CBS \_ AUTOHSCROLL,**](combo-box-styles.md) establecer el límite de texto para que sea mayor que el tamaño del control de edición no tiene ningún efecto.

El **mensaje \_ LIMITTEXT de CB** limita solo el texto que el usuario puede escribir. No tiene ningún efecto en ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición cuando se selecciona una cadena en el cuadro de lista.

El límite predeterminado para el texto que un usuario puede escribir en el control de edición es de 30 000 **TCHAR.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





