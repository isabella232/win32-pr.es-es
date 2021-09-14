---
description: Especifica el FOURCC que identifica el codificador que desea usar.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: MFPKEY_FOURCC propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363835"
---
# <a name="mfpkey_fourcc-property"></a>Propiedad FOURCC de MFPKEY \_

Especifica el FOURCC que identifica el codificador que desea usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCFOURCC

## <a name="data-type"></a>Tipo de datos

VT \_ I4 (valor FOURCC)

## <a name="remarks"></a>Observaciones

Debe establecer este valor antes de recuperar los valores de las siguientes propiedades mediante **IPropertyBag** **o IPropertyStore**:

-   [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

Debe usar [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar los valores de las propiedades dependientes de FOURCC enumeradas anteriormente. Al usar **GetCodecProp**, no es necesario establecer **MFPKEY \_ FOURCC**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




