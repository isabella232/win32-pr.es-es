---
description: Especifica el esquema de codificación.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Propiedad AVEncCodecType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162041"
---
# <a name="avenccodectype-property"></a>Propiedad AVEncCodecType

Especifica el esquema de codificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un **BSTR** que contiene la representación de cadena de un GUID. Se definen los GUID siguientes.



| GUID                                      | Descripción                                        |
|-------------------------------------------|----------------------------------------------------|
| CODECAPI \_ GUID \_ AVEncDolbyDigitalConsumer | Audio de Dolby Digital Consumer                       |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPlus     | Audio de Dolby Digital Plus                           |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPro      | Dolby Digital Pro audio                            |
| CODECAPI \_ GUID \_ AVEncDTS                  | Audio DTS                                          |
| CODECAPI \_ GUID \_ AVEncDTSHD                | Audio DTS-HD                                       |
| CODECAPI \_ GUID \_ AVEncDV                   | Vídeo DV                                           |
| CODECAPI \_ GUID \_ AVEncH264Video            | Vídeo de H.264                                        |
| CODECAPI \_ GUID \_ AVEncMLP                  | Audio de Empaquetado sin pérdida de meridiano (MLP)              |
| CODECAPI \_ GUID \_ AVEncMPEG1Audio           | Audio MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG1Video           | Vídeo MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Audio           | Audio MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Video           | Vídeo MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncPCM                  | Audio de PCM                                          |
| CODECAPI \_ GUID \_ AVEncSDDS                 | Audio de Sonido digital dinámico (SDDS) de Sonar            |
| CODECAPI \_ GUID \_ AVEncWMALossless          | Windows Audio multimedia 9 Audio sin pérdida               |
| CODECAPI \_ GUID \_ AVEncWMAPro               | Windows Audio multimedia 9 Professional audio (WMA Pro) |
| CODECAPI \_ GUID \_ AVEncWMAVoice             | Windows Audio multimedia 9 Audio de voz                  |
| CODECAPI \_ GUID \_ AVEncWMV                  | Windows Vídeo multimedia                                |
| CODECAPI \_ GUID \_ AVEndMPEG4Video           | Vídeo MPEG-4                                       |



 

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para especificar qué esquema de codificación se va a usar. Los códecs también pueden devolver esta propiedad como una funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




