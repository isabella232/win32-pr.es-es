---
description: Especifica el tipo de vínculo al rastrear o indizar.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumeración LINKTYPE
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
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463048"
---
# <a name="linktype-enumeration"></a>Enumeración LINKTYPE

\[La **enumeración LINKTYPE** solo se admite en Windows XP y Windows Server 2003, y ya no se debe usar.\]

Especifica el tipo de vínculo al rastrear o indizar.

## <a name="syntax"></a>Syntax


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**DIRECCIÓN URL DE LINKTYPE \_**
</dt> <dd>

Especifica si se debe indexar el tipo de vínculo de direcciones URL.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**CONTENIDO DE \_ LINKTYPE**
</dt> <dd>

Especifica si se debe indexar el contenido del vínculo.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ RELACIONADO**
</dt> <dd>

Especifica un vínculo relacionado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar las marcas **LINKTYPE** y las siguientes otras API: los métodos [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) y la estructura [**LINKINFO.**](-search-linkinfo.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 




