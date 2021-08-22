---
description: Obtiene o establece la velocidad de la decodificación de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propiedad AVDecVideoFastDecodeMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36cd765754e73924caae401495e597ec69828ed62f08466884b10365517d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503145"
---
# <a name="avdecvideofastdecodemode-property"></a>Propiedad AVDecVideoFastDecodeMode

Obtiene o establece la velocidad de la decodificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad puede oscilar entre 0 y 32, donde 0 indica lacodización normal y 32 es el modo decodización más rápido. El comportamiento exacto depende de la implementación del descodificador. No todos los incrementos entre 1 y 32 definen necesariamente un modo distinto.

La [**enumeración eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene algunos modos predefinidos para esta propiedad.

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

 

 




