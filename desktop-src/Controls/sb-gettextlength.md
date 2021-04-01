---
title: Mensaje de SB_GETTEXTLENGTH (commctrl. h)
description: Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH controles de mensajes de Windows
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
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996812"
---
# <a name="sb_gettextlength-message"></a>\_Mensaje GETTEXTLENGTH de SB

Recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento del que se va a recuperar el texto.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que consta de valores de 2 16 bits. La palabra baja especifica la longitud, en caracteres, del texto. La palabra alta especifica el tipo de operación que se usa para dibujar el texto. El tipo puede ser uno de los siguientes valores:



| Código devuelto                                                                                    | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0,1**</dt> </dl>               | El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.<br/>          |
| <dl> <dt>**SBT \_ NOborders**</dt> </dl>  | El texto se dibuja sin bordes.<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | El texto se dibuja mediante la ventana primaria.<br/>                                                |
| <dl> <dt>**SBT \_ emergente**</dt> </dl>     | El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | El texto se mostrará en la dirección opuesta al texto de la ventana primaria.<br/> |



 

## <a name="remarks"></a>Observaciones

Texto normal de la pantalla de Windows de izquierda a derecha (LTR). Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL). Si \_ se establece SBT RTLREADING, el texto de la ventana de estado especificada se leerá en la dirección opuesta a la del texto de la ventana primaria.

Este mensaje devuelve una longitud máxima de cadena de 65.535 caracteres. Si la cadena de texto real es más larga que esa, el mensaje [**\_ GETTEXT de SB**](sb-gettext.md) lo trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) y **SB \_ GETTEXTLENGTHA** (ANSI)<br/>         |



 

 





