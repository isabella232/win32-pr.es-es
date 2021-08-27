---
title: SB_GETTEXTLENGTH mensaje (Commctrl.h)
description: Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c203862b2a17352924f3df07560034c9f52784c84676d924d78524b05be1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084965"
---
# <a name="sb_gettextlength-message"></a>Mensaje \_ SB GETTEXTLENGTH

Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento del que se va a recuperar texto.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que consta de dos valores de 16 bits. La palabra baja especifica la longitud, en caracteres, del texto. La palabra alta especifica el tipo de operación que se usa para dibujar el texto. El tipo puede ser uno de los siguientes valores:



| Código devuelto                                                                                    | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | El texto se dibuja con un borde para que aparezca más bajo que el plano de la ventana.<br/>          |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | El texto se dibuja sin bordes.<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | La ventana primaria dibuja el texto.<br/>                                                |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | El texto se dibuja con un borde que aparece más arriba que el plano de la ventana.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | El texto se mostrará en la dirección opuesta al texto de la ventana primaria.<br/> |



 

## <a name="remarks"></a>Comentarios

Las ventanas normales muestran texto de izquierda a derecha (LTR). Windows se puede reflejar *para* mostrar idiomas como hebreo o árabe que leen de derecha a izquierda (RTL). Si se establece SBT RTLREADING, el texto de la ventana de estado especificado leerá en la dirección opuesta del texto \_ de la ventana primaria.

Este mensaje devuelve una longitud máxima de cadena de 65 535 caracteres. Si la cadena de texto real es mayor que eso, el [**mensaje \_ SB GETTEXT**](sb-gettext.md) la trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) y **SB \_ GETTEXTLENGLG (ANSI)**<br/>         |



 

 





