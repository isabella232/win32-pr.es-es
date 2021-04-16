---
description: Habilita el modo de baja latencia en un códec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Propiedad CODECAPI_AVLowLatencyMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696167"
---
# <a name="codecapi_avlowlatencymode-property"></a>\_Propiedad AVLowLatencyMode de CODECAPI

Habilita el modo de baja latencia en un códec.

## <a name="data-type"></a>Tipo de datos

**ULong** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valor de propiedad

Si el valor es distinto de cero, el modo de latencia baja está habilitado. Si el valor es cero, el modo de latencia baja está deshabilitado.

## <a name="remarks"></a>Observaciones

Esta propiedad se aplica a ambos codificadores y descodificadores.

El modo de baja latencia es útil para las comunicaciones en tiempo real o la captura en directo, cuando se debe minimizar la latencia. Sin embargo, el modo de latencia baja también puede reducir la descodificación o la calidad de la codificación.

Se espera que el codificador no agregue ningún retraso de muestra debido a la reordenación de fotogramas en el proceso de codificación y una muestra de entrada generará un ejemplo de salida. Los segmentos y fotogramas B pueden estar presentes siempre y cuando no presenten ninguna reordenación de fotogramas en el codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

