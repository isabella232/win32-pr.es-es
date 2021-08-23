---
description: Especifica los fotogramas de referencia máximos admitidos por el codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606425"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>Propiedad CODECAPI \_ AVEncVideoMaxNumRefFrame

Especifica los fotogramas de referencia máximos admitidos por el codificador.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Comentarios

Para H.264, esto se asigna a la variable Set de parámetros de secuencia **max \_ num ref \_ \_ frames** tal como se define en la especificación H.264.

**Codificadores H.264/AVC:**

Los codificadores pueden usar menos fotogramas de referencia para cumplir el nivel especificado en la secuencia de bits.

Los codificadores deben [**admitir GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRangee.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.

El valor predeterminado recomendado es 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

