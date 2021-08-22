---
description: Especifica el QP máximo admitido por el codificador.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606325"
---
# <a name="codecapi_avencvideomaxqp-property"></a>Propiedad CODECAPI \_ AVEncVideoMaxQP

Especifica el QP máximo admitido por el codificador.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Comentarios

**Codificadores H.264/AVC:**

El codificador debe admitir [**GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.

El valor predeterminado debe ser el QP máximo permitido por el estándar de codificación correspondiente. Por ejemplo, los codificadores H.264 deben tener un valor predeterminado de 51.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

