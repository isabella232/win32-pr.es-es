---
description: Especifica el número máximo de fotogramas de referencia que admite el codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Propiedad CODECAPI_AVEncVideoMaxNumRefFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157008"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>\_Propiedad AVEncVideoMaxNumRefFrame de CODECAPI

Especifica el número máximo de fotogramas de referencia que admite el codificador.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Observaciones

Para H. 264, se asigna a la variable de conjunto de parámetros de secuencia set **Max \_ NUM \_ \_ frames** , tal y como se define en la especificación H. 264.

**Codificadores H. 264/AVC:**

Los codificadores pueden usar menos fotogramas de referencia para obedecer el nivel especificado en el fragmentada.

Los codificadores deben admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.

El valor predeterminado recomendado es 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

