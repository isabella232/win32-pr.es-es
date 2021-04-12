---
description: Se establece como un atributo para un objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276225"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>\_Atributo de mejor esfuerzo de MFPROTECTIONATTRIBUTE \_

Se establece como un atributo para un objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) . Si este atributo está presente, se omite un error al intentar aplicar la protección. Si el valor del atributo asociado es **true**, se debe aplicar el esquema de protección con el atributo de [conmutación por \_ error \_ de MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) .

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Si **es true**, aplique el esquema de protección con el atributo de [ \_ conmutación \_ por error de MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) si se produce un error al establecer esta protección.

Se establece como un atributo para un objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones para UWP de Windows 8\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones para UWP de Windows Server 2012\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




