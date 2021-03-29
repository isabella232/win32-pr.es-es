---
description: Especifica el formato de destino de un codificador.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Propiedad AVEncCommonFormatConstraint (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666139"
---
# <a name="avenccommonformatconstraint-property"></a>Propiedad AVEncCommonFormatConstraint

Especifica el formato de destino de un codificador.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un **BSTR** que contiene la representación de cadena de un GUID. Se definen los siguientes GUID.



| GUID                                         | Descripción                     |
|----------------------------------------------|---------------------------------|
| CODECAPI \_ GUID \_ AVEncCommonFormatATSC        | Televisión por cable de ATSC.          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVB         | Televisión por cable DVB.           |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ PlusVR | DVD + VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMAT     | HighMAT                         |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMPV     | No documentado en esta versión. |
| CODECAPI \_ GUID \_ AVEncCommonFormatMP3         | Capa de audio MPEG-3 (MP3)        |
| CODECAPI \_ GUID \_ AVEncCommonFormatSVCD        | CD de super video (SVCD)           |
| CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified | Formato no especificado.             |
| CODECAPI \_ GUID \_ AVEncCommonFormatVCD         | CD de vídeo (VCD)                  |



 

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para especificar el formato de destino. Los codificadores también pueden devolver esta propiedad como una capacidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




