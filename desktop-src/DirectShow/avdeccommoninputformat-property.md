---
description: Especifica el formato de entrada actual para el descodificador.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propiedad AVDecCommonInputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187e923be9c53cebbb55663d55ec6351be38f84c33f8c03277f587d61a4db719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079495"
---
# <a name="avdeccommoninputformat-property"></a>Propiedad AVDecCommonInputFormat

Especifica el formato de entrada actual para el descodificador.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un **BSTR** que contiene la representación de cadena de un GUID. Se definen los GUID siguientes.



| **GUID**                                            | Descripción                                    |
|-----------------------------------------------------|------------------------------------------------|
| **CODECAPI \_ GUID \_ AVDecAudioInputAAC**              | Codificación de audio avanzada (AAC)                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus** | Audio de Dolby Digital Plus                       |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolby**            | Audio Dolby                                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDTS**              | Audio DTS                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**            | High-Efficiency codificación de audio avanzada (HE-AAC) |
| **CODECAPI \_ GUID \_ AVDecAudioInputMPEG**             | Audio MPEG                                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputPCM**              | Audio de PCM                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMA**              | Windows Media Audio                            |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Media Audio 9 Professional (WMA Pro)   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




