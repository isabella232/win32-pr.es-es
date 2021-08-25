---
description: Especifica la información del marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642c246adf0e5e1c10249085201fba3dc430b6547516b79fe4929e9de4b998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848125"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>Atributo MFSampleExtension \_ LongTermReferenceFrameInfo

Especifica la información del marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

**Codificadores H.264/AVC:**

Los codificadores devolverán este atributo en el ejemplo de salida cuando la aplicación controla fotogramas LTR, que se especifica mediante [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

MFSampleExtension \_ LongTermReferenceFrameInfo devuelve hasta dos campos.

El primer campo, bits \[ 0..15 , es \] *LongTermFrameIdx* asociado al marco de salida si está marcado como marco LTR. El primer valor es 0xffff, si este marco de salida es un marco de referencia a corto plazo o un marco que no es de referencia.

El segundo campo, bits 16..31, es un mapa de bits que consta de \[ \] muchos bits *MaxNumLTRFrames* que indican qué fotogramas LTR se usaron para codificar este marco de salida, empezando por el bit 16. El resto de bits se establecerá en 0. El segundo valor es 0 si este marco de salida no está codificado con ningún fotograma LTR. *MaxNumLTRFrames es* el número máximo de fotogramas LTR establecidos a través de [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




