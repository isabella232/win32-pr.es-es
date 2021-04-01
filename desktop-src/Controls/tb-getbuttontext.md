---
title: Mensaje de TB_GETBUTTONTEXT (commctrl. h)
description: Recupera el texto para mostrar de un botón de una barra de herramientas.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150453"
---
# <a name="tb_getbuttontext-message"></a>\_Mensaje GETBUTTONTEXT TB

Recupera el texto para mostrar de un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón cuyo texto se va a recuperar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que recibe el texto del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la longitud, en caracteres, de la cadena a la que señala *lParam*. La longitud no incluye el carácter nulo de terminación. Si no se realiza correctamente, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, llame primero al mensaje que pasa **null** en *lParam*; esto devuelve el número de caracteres, excluidos los **valores NULL** necesarios. A continuación, llame al mensaje una segunda vez para recuperar la cadena. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

La cadena devuelta corresponde al texto que se muestra actualmente en el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ GETBUTTONTEXTW** (Unicode) y **TB \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**GETSTRING de TB \_**](tb-getstring.md)
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





