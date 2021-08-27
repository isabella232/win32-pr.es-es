---
title: Elemento Body (showMessageType)
description: Contiene el texto que se mostrará en el cuerpo del cuadro de mensaje.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Cuerpo del elemento Programador de tareas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010875"
---
# <a name="body-showmessagetype-element"></a>Elemento Body (showMessageType)

Contiene el texto que se mostrará en el cuerpo del cuadro de mensaje.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

El tipo complejo [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) define el elemento **Body.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                               | Descripción                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Representa una acción que muestra un cuadro de mensaje.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad MessageBody de IShowMessageAction.**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody)

Para el desarrollo de scripts, [**vea ShowMessageAction.MessageBody.**](showmessageaction-messagebody.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





