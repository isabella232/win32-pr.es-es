---
title: Mensaje de SB_GETTEXT (commctrl. h)
description: Recupera el texto de la parte especificada de una ventana de estado.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT controles de mensajes de Windows
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
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079609"
---
# <a name="sb_gettext-message"></a>\_Mensaje GETTEXT de SB

Recupera el texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento del que se va a recuperar el texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe el texto como una cadena terminada en NULL. Use el [**mensaje \_ GETTEXTLENGTH de SB**](sb-gettextlength.md) para determinar el tamaño requerido del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que consta de valores de 2 16 bits. La palabra baja especifica la longitud, en caracteres, del texto. La palabra alta especifica el tipo de operación que se usa para dibujar el texto. El tipo puede ser uno de los valores siguientes.



| Código devuelto                                                                                    | Descripción                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0,1**</dt> </dl>               | El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.<br/>  |
| <dl> <dt>**SBT \_ NOborders**</dt> </dl>  | El texto se dibuja sin bordes.<br/>                                             |
| <dl> <dt>**SBT \_ emergente**</dt> </dl>     | El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | El texto se muestra en la dirección opuesta del texto de la ventana primaria.<br/>  |



 

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje puede poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, llame primero a [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el número de caracteres necesarios y, a continuación, llame al mensaje para recuperar la cadena. Si espera antes de llamar a la **\_ GETTEXT de SB** , el texto podría cambiar, invalidando de este modo el valor devuelto de **SB \_ GETTEXTLENGTH**. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

Este mensaje devuelve un máximo de 65.535 caracteres. Si la cadena de texto es más larga, se trunca.

Si el texto tiene el \_ tipo de dibujo OWNERDRAW SBT, este mensaje devuelve el valor de 32 bits asociado al texto en lugar de la longitud y el tipo de operación.

Texto normal de la pantalla de Windows de izquierda a derecha (LTR). Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL). Si \_ se establece SBT RTLREADING, la cadena *lParam* lee en la dirección opuesta del texto de la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) y **\_ gettext gettexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SETTEXT de SB \_**](sb-settext.md)
</dt> </dl>

 

 





