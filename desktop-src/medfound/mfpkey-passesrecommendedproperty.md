---
description: Especifica el número máximo de pases admitidos por el codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af869c6acca584547083b3de245913a35680306b47feabaf2a602a3c1c15e87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826365"
---
# <a name="mfpkey_passesrecommended-property"></a>Propiedad \_ MFPKEY PASSESRECOMMENDED

Especifica el número máximo de pases admitidos por el codificador. Solo lectura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Puede obtener el valor de esta propiedad que llama a [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si usa **IPropertyBag**, primero debe establecer el valor FOURCC del formato comprimido deseado mediante la [propiedad \_ MFPKEY FOURCC.](mfpkey-fourccproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




