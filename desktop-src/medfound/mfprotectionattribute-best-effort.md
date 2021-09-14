---
description: Se establece como un atributo para un objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361134"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>Atributo MFPROTECTIONATTRIBUTE \_ BEST \_ EFFORT

Se establece como un atributo para [**un objeto IMFOutputSchema.**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) Si este atributo está presente, se omite un intento fallido de aplicar la protección. Si el valor del atributo asociado es **TRUE**, se debe aplicar el esquema de protección con el atributo [MFPROTECTIONATTRIBUTE \_ FAIL \_ OVER.](mfprotectionattribute-fail-over.md)

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Observaciones

Si **es TRUE,** aplique el esquema de protección con el atributo [MFPROTECTIONATTRIBUTE \_ FAIL \_ OVER](mfprotectionattribute-fail-over.md) si se produce un error al establecer esta protección.

Se establece como un atributo para [**un objeto IMFOutputSchema.**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 Solo aplicaciones para UWP\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 Solo aplicaciones para UWP\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




