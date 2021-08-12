---
title: EM_SETTEXTMODE (Richedit.h)
description: Establece el modo de texto o el nivel de deshacer de un control de edición enriquecido. Se produce un error en el mensaje si el control contiene texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ea489dcdb60908cac8600188d40b9aae4b7e3e531c713094bb180e84ee24bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672374"
---
# <a name="em_settextmode-message"></a>Mensaje \_ EM SETTEXTMODE

Establece el modo de texto o el nivel de deshacer de un control de edición enriquecido. Se produce un error en el mensaje si el control contiene texto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o varios valores del tipo [**de enumeración TEXTMODE.**](/windows/win32/api/richedit/ne-richedit-textmode) Los valores especifican la nueva configuración para el modo de texto del control y los parámetros de nivel de deshacer.

Especifique uno de los siguientes valores para establecer el parámetro de modo de texto. Si no especifica un valor de modo de texto, el modo de texto permanece en su configuración actual. 

| Value                                          | Significado                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ PLAINTEXT**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica el modo de texto sin formato, en el que el control es similar a un control de edición estándar. Para obtener más información sobre el modo de texto sin formato, vea la sección Comentarios siguiente. |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica el modo de texto enriquecido, en el que el control tiene la funcionalidad de edición enriquecida estándar. El modo de texto enriquecido es la configuración predeterminada.                                           |



 

Especifique uno de los siguientes valores para establecer el parámetro de nivel de deshacer. Si no especifica un valor de nivel de deshacer, el nivel de deshacer permanece en su configuración actual. 

| Value                                                      | Significado                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | El control permite al usuario deshacer solo la última acción que se puede deshacer.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | El control admite varias operaciones de deshacer. Esta es la configuración predeterminada. Use el [**mensaje EM \_ SETUNDOLIMIT**](em-setundolimit.md) para establecer el número máximo de acciones de deshacer. |



 

Especifique uno de los siguientes valores para establecer el parámetro de página de códigos. Si no especifica un valor de página de códigos, la página de códigos permanece en su configuración actual. 

| Value                                                    | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | El control solo permite el teclado en inglés y un teclado correspondiente al juego de caracteres predeterminado. Por ejemplo, podría tener griego e inglés. Tenga en cuenta que esto impide que el texto Unicode entre en el control . Por ejemplo, use este valor si un control Rich Edit debe estar restringido al texto ANSI. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | El control permite varias páginas de códigos y texto Unicode en el control . Esta es la configuración predeterminada.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero.

## <a name="remarks"></a>Observaciones

En el modo de texto enriquecido, un control de edición enriquecido tiene la funcionalidad de edición enriquección estándar. Sin embargo, en modo de texto sin formato, el control es similar a un control de edición estándar:

-   El texto de un control de texto sin formato solo puede tener un formato (por ejemplo, Negrita, 10pt Arial).
-   El usuario no puede pegar formatos de texto enriquecido, como formato de texto enriquecido (RTF) ni objetos incrustados en un control de texto sin formato.
-   Los controles de modo de texto enriquecido siempre tienen un marcador de fin de documento predeterminado o retorno de carro para dar formato a párrafos. Por otro lado, los controles de texto sin formato no necesitan el marcador de fin de documento predeterminado, por lo que se omite.

El control no debe contener texto cuando recibe el **mensaje EM \_ SETTEXTMODE.** Para asegurarse de que no hay texto, envíe un [**mensaje \_ WM SETTEXT**](/windows/desktop/winmsg/wm-settext) con una cadena vacía ("").

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETTEXTMODE**](em-gettextmode.md)
</dt> <dt>

[**EM \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

