---
description: Especifica la información de marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689678"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>\_Atributo LongTermReferenceFrameInfo de MFSampleExtension

Especifica la información de marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

Los codificadores devolverán este atributo en el ejemplo de salida cuando la aplicación controle Marcos LTR, que se especifica mediante [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

MFSampleExtension \_ LongTermReferenceFrameInfo devuelve hasta dos campos.

El primer campo, bits \[ 0.. 15 \] , se *LongTermFrameIdx* asociado con el fotograma de salida si está marcado como marco LTR. El primer valor es 0xFFFF, si este fotograma de salida es un marco de referencia a corto plazo o un fotograma sin referencia.

El segundo campo, bits \[ 16... 31 \] , es un mapa de bits que se compone de *MaxNumLTRFrames* muchos bits que indican qué Marcos LTR se usaron para codificar este fotograma de salida, empezando por el bit 16. El resto de bits se establecerá en 0. El segundo valor es 0 si este fotograma de salida no se codifica con ningún marco LTR. *MaxNumLTRFrames* es el número máximo de Marcos LTR establecidos a través de [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




