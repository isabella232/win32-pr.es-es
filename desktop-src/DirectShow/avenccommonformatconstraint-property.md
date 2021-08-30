---
description: Especifica el formato de destino para un codificador.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Propiedad AVEncCommonFormatConstraint (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2108255ca6f42596fe707c66b02e0e4dd38baa5b0f788073adff8cdb4677dd16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108694"
---
# <a name="avenccommonformatconstraint-property"></a>Propiedad AVEncCommonFormatConstraint

Especifica el formato de destino para un codificador.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un **BSTR** que contiene la representación de cadena de un GUID. Se definen los GUID siguientes.



| GUID                                         | Descripción                     |
|----------------------------------------------|---------------------------------|
| CODECAPI \_ GUID \_ AVEncCommonFormatATSC        | Televisión por cable atsc.          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVB         | Televisión por cable DE LA MARCA.           |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ PlusVR | DVD+VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMAT     | HighMAT                         |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMPV     | No se documenta en esta versión. |
| CODECAPI \_ GUID \_ AVEncCommonFormatMP3         | Mpeg Audio Layer-3 (MP3)        |
| GUID de CODECAPI \_ \_ AVEncCommonFormatSVCD        | Super Video CD (SVCD)           |
| CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified | Formato no especificado.             |
| CODECAPI \_ GUID \_ AVEncCommonFormatVCD         | CD de vídeo (VCD)                  |



 

## <a name="remarks"></a>Comentarios

Las aplicaciones pueden establecer esta propiedad para especificar el formato de destino. Los codificadores también pueden devolver esta propiedad como una funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




