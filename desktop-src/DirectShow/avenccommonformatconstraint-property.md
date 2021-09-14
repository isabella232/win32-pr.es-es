---
description: Especifica el formato de destino para un codificador.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Propiedad AVEncCommonFormatConstraint (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162026"
---
# <a name="avenccommonformatconstraint-property"></a>AvEncCommonFormatConstraint, propiedad

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
| CODECAPI \_ GUID \_ AVEncCommonFormatDVB         | Televisión de cable DE LAN.           |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ PlusVR | DVD+VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMAT     | HighMAT                         |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMPV     | No se documenta en esta versión. |
| CODECAPI \_ GUID \_ AVEncCommonFormatMP3         | MPEG Audio Layer-3 (MP3)        |
| CODECAPI \_ GUID \_ AVEncCommonFormatSVCD        | Super Video CD (SVCD)           |
| CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified | Formato no especificado.             |
| CODECAPI \_ GUID \_ AVEncCommonFormatVCD         | CD de vídeo (VCD)                  |



 

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para especificar el formato de destino. Los codificadores también pueden devolver esta propiedad como una funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




