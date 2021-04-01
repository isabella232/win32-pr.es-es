---
title: Mensaje EM_SETTEXTMODE (RichEdit. h)
description: Establece el modo de texto o el nivel de deshacer de un control Rich Edit. Se produce un error en el mensaje si el control contiene texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE controles de mensajes de Windows
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
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996559"
---
# <a name="em_settextmode-message"></a>\_Mensaje SETTEXTMODE em

Establece el modo de texto o el nivel de deshacer de un control Rich Edit. Se produce un error en el mensaje si el control contiene texto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o más valores del tipo de enumeración [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) . Los valores especifican los nuevos valores para el modo de texto y los parámetros de nivel de deshacer del control.

Especifique uno de los siguientes valores para establecer el parámetro de modo de texto. Si no especifica un valor en modo de texto, el modo de texto permanece en su configuración actual. 

| Value                                          | Significado                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_texto sin formato de TM**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica el modo de texto sin formato, en el que el control es similar a un control de edición estándar. Para obtener más información sobre el modo de texto sin formato, vea la sección Comentarios siguiente. |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica el modo de texto enriquecido, en el que el control tiene una funcionalidad estándar de edición enriquecida. El modo de texto enriquecido es el valor predeterminado.                                           |



 

Especifique uno de los siguientes valores para establecer el parámetro de nivel de deshacer. Si no especifica un valor de nivel de deshacer, el nivel de deshacer se mantiene en su configuración actual. 

| Value                                                      | Significado                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | El control permite al usuario deshacer solo la última acción que se puede deshacer.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | El control admite varias operaciones de deshacer. Esta es la configuración predeterminada. Use el [**mensaje \_ SETUNDOLIMIT em**](em-setundolimit.md) para establecer el número máximo de acciones de deshacer. |



 

Especifique uno de los siguientes valores para establecer el parámetro de página de códigos. Si no especifica un valor de página de códigos, la página de códigos permanece en su configuración actual. 

| Value                                                    | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | El control solo permite el teclado inglés y un teclado correspondientes al Juego de caracteres predeterminado. Por ejemplo, podría tener griego e inglés. Tenga en cuenta que esto evita que el texto Unicode entre en el control. Por ejemplo, use este valor si un control Rich Edit debe estar restringido a texto ANSI. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | El control permite varias páginas de códigos y texto Unicode en el control. Esta es la configuración predeterminada.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero.

## <a name="remarks"></a>Observaciones

En el modo de texto enriquecido, un control Rich Edit tiene una funcionalidad estándar de edición enriquecida. Sin embargo, en modo de texto sin formato, el control es similar a un control de edición estándar:

-   El texto de un control de texto sin formato solo puede tener un formato (por ejemplo, negrita, 10 PTO y Arial).
-   El usuario no puede pegar formatos de texto enriquecido, como el formato de texto enriquecido (RTF) o los objetos incrustados en un control de texto sin formato.
-   Los controles de modo de texto enriquecido siempre tienen un marcador de fin de documento o un retorno de carro predeterminados para dar formato a los párrafos. Los controles de texto sin formato, por otro lado, no necesitan el marcador de fin de documento predeterminado, por lo que se omite.

El control no debe contener texto cuando recibe el mensaje **\_ SETTEXTMODE em** . Para asegurarse de que no hay texto, envíe un mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) con una cadena vacía ("").

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTEXTMODE em**](em-gettextmode.md)
</dt> <dt>

[**\_SETUNDOLIMIT em**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

