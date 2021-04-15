---
description: Especifica el formato de salida para el descodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propiedad AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538013"
---
# <a name="avdeccommonoutputformat-property"></a>Propiedad AVDecCommonOutputFormat

Especifica el formato de salida para el descodificador.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valor de propiedad



| GUID                                                               | Descripción                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Audio PCM, con cualquier número de canales                                                                                                                                                                             |
| \_Auriculares CODECAPI GUID \_ AVDecAudioOutputFormat \_ PCM \_            | Audio PCM estéreo, con el downmix de solo izquierda/solo hacia la derecha (lo/ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ auto          | Audio PCM estéreo mediante la selección automática del modo downmix estéreo (lo/ro o LT/RT). Puede usar este valor para los formatos de audio en los que el flujo de entrada define el modo de downmix preferido, como Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ MatrixEncoded | Audio PCM estéreo con codificación de matriz codificada downmix (LT/RT)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ fragmentada           | S/PDIF (formato de interfaz digital de Sony/Philips) comprimido fragmentada, tal como se define en IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ \_ PCM SPDIF                 | Estéreo S/PDIF PCM, tal como se define en IEC-60958                                                                                                                                                                          |



 

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

 

 




