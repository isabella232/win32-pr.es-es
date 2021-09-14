---
title: Elemento Title (showMessageType)
description: Contiene el título del cuadro de mensaje.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento Title Programador de tareas
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968604"
---
# <a name="title-showmessagetype-element"></a>Elemento Title (showMessageType)

Contiene el título del cuadro de mensaje.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

El tipo complejo [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) define el elemento **Title.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                               | Descripción                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Representa una acción que muestra un cuadro de mensaje.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea Propiedad Title de IShowMessageAction.**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title)

Para el desarrollo de scripts, [**vea ShowMessageAction.Title**](showmessageaction-title.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





