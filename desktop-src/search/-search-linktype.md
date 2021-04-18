---
description: Especifica el tipo de vínculo durante el rastreo o la indexación.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumeración de LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705490"
---
# <a name="linktype-enumeration"></a>Enumeración de LINKTYPE

\[La enumeración **LINKTYPE** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.\]

Especifica el tipo de vínculo durante el rastreo o la indexación.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**URL de LINKTYPE \_**
</dt> <dd>

Especifica si se debe indizar el tipo de vínculo URL.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**contenido de LINKTYPE \_**
</dt> <dd>

Especifica si se debe indizar el contenido del vínculo.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**\_relacionado con LINKTYPE**
</dt> <dd>

Especifica un vínculo relacionado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en los equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar las marcas de **LINKTYPE** y las siguientes API: los métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) y [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) y la estructura [**LINKINFO**](-search-linkinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




