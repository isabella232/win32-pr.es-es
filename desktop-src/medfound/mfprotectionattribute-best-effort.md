---
description: Se establece como un atributo para un objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f462c5a897f0913fa33ae330fe80d7b29470d23b41b8e0abed4ac96aa7e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689053"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>Atributo MFPROTECTIONATTRIBUTE \_ BEST \_ EFFORT

Se establece como un atributo para [**un objeto IMFOutputSchema.**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) Si este atributo está presente, se omite un intento fallido de aplicar la protección. Si el valor del atributo asociado es **TRUE,** se debe aplicar el esquema de protección con el atributo [MFPROTECTIONATTRIBUTE \_ FAIL \_ OVER.](mfprotectionattribute-fail-over.md)

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Si **es TRUE,** aplique el esquema de protección con el atributo [MFPROTECTIONATTRIBUTE \_ FAIL \_ OVER](mfprotectionattribute-fail-over.md) si se produce un error al establecer esta protección.

Se establece como un atributo para [**un objeto IMFOutputSchema.**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 Solo aplicaciones para UWP\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 Solo aplicaciones para UWP\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




