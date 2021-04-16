---
title: Estilos de control SysLink (CommCtrl. h)
description: Al crear controles SysLink, se usan las constantes de estilo siguientes.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649770"
---
# <a name="syslink-control-styles"></a>Estilos del control SysLink

Al crear controles SysLink, se usan las constantes de estilo siguientes.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**\_transparente LWS**</dt> </dl>             | El modo de combinación en segundo plano es transparente. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_ IGNORERETURN**</dt> </dl>       | Cuando el vínculo tiene el foco de teclado y el usuario presiona entrar, el control omite la pulsación de tecla y se pasa al cuadro de diálogo host.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**LWS \_ NOprefix**</dt> </dl>                      | **Windows Vista**. Si el texto contiene una y comercial, se trata como un carácter literal en lugar del prefijo de una tecla de método abreviado.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_ USEVISUALSTYLE**</dt> </dl> | **Windows Vista**. El vínculo se muestra en el estilo visual actual.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**LWS \_ USECUSTOMTEXT**</dt> </dl>       | **Windows Vista**. Cuando se dibuja el control, se envía una notificación de [ \_ CUSTOMTEXT nm](nm-customtext.md) para que la aplicación pueda proporcionar texto de forma dinámica.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ derecha**</dt> </dl>                               | **Windows Vista**. El texto está justificado a la derecha.<br/>                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





