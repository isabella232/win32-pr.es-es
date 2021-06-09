---
description: Habilita el modo de baja latencia en un códec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826909"
---
# <a name="codecapi_avlowlatencymode-property"></a>Propiedad CODECAPI \_ AVLowLatencyMode

Habilita el modo de baja latencia en un códec.

## <a name="data-type"></a>Tipo de datos

**ULONG** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Valor de propiedad

Si el valor es distinto de cero, se habilita el modo de baja latencia. Si el valor es cero, el modo de baja latencia está deshabilitado.

## <a name="remarks"></a>Comentarios

Esta propiedad se aplica tanto a los codificadores como a los descodificadores.

El modo de baja latencia es útil para las comunicaciones en tiempo real o la captura en vivo, cuando se debe minimizar la latencia. Sin embargo, el modo de baja latencia también puede reducir la calidad de la codificación o la codificación.

Se espera que el codificador no agregue ningún retraso de muestra debido a la reordenación de fotogramas en el proceso de codificación y que una muestra de entrada produzca una muestra de salida. Los segmentos o fotogramas B pueden estar presentes siempre y cuando no introduzcan ninguna reordenación de fotogramas en el codificador.

> [!WARNING] 
> En la implementación actual, el descodificador Media Foundation H.264 usa el tipo **VT_UI4** para esta propiedad. Todas las demás implementaciones, incluido el codificador H.264, usan el tipo **VT_BOOL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 aplicaciones \[ de escritorio \| para aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Aplicaciones de escritorio de Windows Server 2012 \[ \| aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

