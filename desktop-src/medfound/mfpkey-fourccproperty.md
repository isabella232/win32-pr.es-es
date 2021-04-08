---
description: Especifica el FOURCC que identifica el codificador que se desea utilizar.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Propiedad MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001632"
---
# <a name="mfpkey_fourcc-property"></a>MFPKEY \_ FourCC (propiedad)

Especifica el FOURCC que identifica el codificador que se desea utilizar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCFOURCC

## <a name="data-type"></a>Tipo de datos

VT \_ I4 (valor FourCC)

## <a name="remarks"></a>Observaciones

Debe establecer este valor antes de recuperar los valores de las siguientes propiedades mediante **IPropertyBag** o **IPropertyStore**:

-   [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

Debe usar [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar los valores de las propiedades dependientes de FourCC mencionadas anteriormente. Cuando se usa **GetCodecProp**, no es necesario establecer **MFPKEY \_ FourCC**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




