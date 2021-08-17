---
title: SB_GETTEXT mensaje (Commctrl.h)
description: Recupera el texto de la parte especificada de una ventana de estado.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05967d41d86ad039e39259c8179a9e768e8fbbf76e5112b531048ac0ed7b56bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168740"
---
# <a name="sb_gettext-message"></a>Mensaje \_ SB GETTEXT

Recupera el texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento del que se va a recuperar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe el texto como una cadena terminada en NULL. Use el [**mensaje SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para determinar el tamaño necesario del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que consta de dos valores de 16 bits. La palabra baja especifica la longitud, en caracteres, del texto. La palabra alta especifica el tipo de operación que se usa para dibujar el texto. El tipo puede ser uno de los siguientes valores.



| Código devuelto                                                                                    | Descripción                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | El texto se dibuja con un borde para que aparezca más bajo que el plano de la ventana.<br/>  |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | El texto se dibuja sin bordes.<br/>                                             |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | El texto se dibuja con un borde que aparece más arriba que el plano de la ventana.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | El texto se muestra en la dirección opuesta del texto en la ventana primaria.<br/>  |



 

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso incorrecto de este mensaje puede poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, llame primero a [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el número de caracteres necesarios y, a continuación, llame al mensaje para recuperar la cadena. Si espera antes de llamar a **SB \_ GETTEXT,** el texto podría cambiar, invalidando así el valor devuelto **de SB \_ GETTEXTLENGTH**. Debe revisar consideraciones [de seguridad: Microsoft Windows antes](sec-comctls.md) de continuar.

Este mensaje devuelve un máximo de 65 535 caracteres. Si la cadena de texto es mayor que eso, se trunca.

Si el texto tiene el tipo de dibujo SBT OWNERDRAW, este mensaje devuelve el valor de 32 bits asociado al texto en lugar de la longitud y el tipo \_ de operación.

Las ventanas normales muestran texto de izquierda a derecha (LTR). Windows se puede reflejar *para* mostrar idiomas como hebreo o árabe que leen de derecha a izquierda (RTL). Si se establece SBT \_ RTLREADING, la cadena *lParam* lee en la dirección opuesta del texto de la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) y **SB \_ GETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SB \_ SETTEXT**](sb-settext.md)
</dt> </dl>

 

 





