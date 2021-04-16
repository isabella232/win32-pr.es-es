---
description: Especifica el tamaño máximo de QP compatible con el codificador.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Propiedad CODECAPI_AVEncVideoMaxQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696172"
---
# <a name="codecapi_avencvideomaxqp-property"></a>\_Propiedad AVEncVideoMaxQP de CODECAPI

Especifica el tamaño máximo de QP compatible con el codificador.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

El codificador debe admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.

El valor predeterminado será el máximo de QP permitido por el estándar de codificación correspondiente. Por ejemplo, los codificadores H. 264 deben tener un valor predeterminado de 51.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

