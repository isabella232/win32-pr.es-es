---
description: Especifica el número máximo de pasos admitidos por el codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Propiedad MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276311"
---
# <a name="mfpkey_passesrecommended-property"></a>\_Propiedad PASSESRECOMMENDED de MFPKEY

Especifica el número máximo de pasos admitidos por el codificador. Solo lectura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede obtener el valor de esta propiedad llamando a [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si usa **IPropertyBag**, primero debe establecer el valor de FourCC del formato comprimido deseado mediante la propiedad [ \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .

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

 

 




