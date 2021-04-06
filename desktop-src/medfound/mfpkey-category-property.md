---
description: Contiene el GUID de categoría de una transformación de Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Propiedad MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910194"
---
# <a name="mfpkey_category-property"></a>\_Propiedad de categoría MFPKEY

Contiene el GUID de categoría de una transformación de Media Foundation (MFT).



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**GUID** (**CLSID** \* )

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un GUID que identifica la categoría MFT. Para obtener una lista de categorías, consulte la [**\_ categoría MFT**](mft-category.md).

Esta propiedad es opcional y solo es meramente informativo. Una MFT puede usar esta propiedad para informar de la categoría en la que se registra. Para obtener esta propiedad, consulte la MFT para la interfaz **IPropertyStore** .

Para enumerar una categoría MFT, llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) . No hay ningún vínculo directo entre la función **MFTEnum** y esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




