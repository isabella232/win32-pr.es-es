---
title: Elemento title (showMessageType)
description: Contiene el título del cuadro de mensaje.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento title Programador de tareas
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150008"
---
# <a name="title-showmessagetype-element"></a>Elemento title (showMessageType)

Contiene el título del cuadro de mensaje.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

El elemento de **título** se define mediante el tipo complejo de [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                               | Descripción                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Representa una acción que muestra un cuadro de mensaje.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Para el desarrollo de scripts, vea [**ShowMessageAction. title**](showmessageaction-title.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





