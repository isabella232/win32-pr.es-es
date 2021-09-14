---
title: Elemento ShowMessage (actionGroup)
description: Representa una acción que muestra un cuadro de mensaje.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Elemento ShowMessage Programador de tareas
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886436"
---
# <a name="showmessage-actiongroup-element"></a>Elemento ShowMessage (actionGroup)

Representa una acción que muestra un cuadro de mensaje.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

El **elemento ShowMessage** se define mediante [**actionGroup.**](taskschedulerschema-actiongroup-group.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                    | Derivado de                                                       | Descripción                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                            | Tipo           | Descripción                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Cuerpo**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Especifica el texto que se mostrará en el cuerpo del cuadro de mensaje. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Especifica el título del cuadro de mensaje. <br/>                       |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, se especifica una acción de cuadro de mensaje mediante el [**objeto ShowMessageAction.**](showmessageaction.md)

Para el desarrollo de C++, se especifica una acción de cuadro de mensaje mediante la [**interfaz IShowMessageAction.**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)

**Windows 8 y Windows Server 2012:** Este elemento se ha quitado. Puede usar IExecAction con la función Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar un mensaje en la sesión de usuario.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa una acción de cuadro de mensaje, vea Ejemplo de cuadro de mensaje [(XML).](/previous-versions//aa381917(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                    |



 

