---
title: Elemento HeaderFields (sendEmailType)
description: Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Programador de tareas del elemento HeaderFields
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534576"
---
# <a name="headerfields-sendemailtype-element"></a>Elemento HeaderFields (sendEmailType)

Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

El elemento **HeaderFields** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                                       | Descripción                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Contiene un campo para un encabezado en un mensaje de correo electrónico. <br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Para el desarrollo de scripts, vea [**EmailAction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





