---
title: Estilos de control SysLink (CommCtrl.h)
description: Las siguientes constantes de estilo se usan al crear controles SysLink.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166953"
---
# <a name="syslink-control-styles"></a>Estilos de control SysLink

Las siguientes constantes de estilo se usan al crear controles SysLink.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**LWS \_ TRANSPARENTE**</dt> </dl>             | El modo de combinación de fondo es transparente. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_ IGNORERETURN**</dt> </dl>       | Cuando el vínculo tiene el foco del teclado y el usuario presiona Entrar, el control omite la pulsación de tecla y se pasa al cuadro de diálogo host.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**LWS \_ NOPREFIX**</dt> </dl>                      | **Windows Vista**. Si el texto contiene una yand, se trata como un carácter literal en lugar del prefijo de una tecla de método abreviado.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_ USEVISUALSTYLE**</dt> </dl> | **Windows Vista**. El vínculo se muestra en el estilo visual actual.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**LWS \_ USECUSTOMTEXT**</dt> </dl>       | **Windows Vista**. Cuando se dibuja el control, se envía una notificación [ \_ NM CUSTOMTEXT](nm-customtext.md) para que la aplicación pueda proporcionar texto dinámicamente.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ RIGHT**</dt> </dl>                               | **Windows Vista**. El texto se justifica a la derecha.<br/>                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





