---
description: Obtiene o establece la velocidad de descodificación de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propiedad AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152584"
---
# <a name="avdecvideofastdecodemode-property"></a>Propiedad AVDecVideoFastDecodeMode

Obtiene o establece la velocidad de descodificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad puede oscilar entre 0 y 32, donde 0 indica descodificación normal y 32 es el modo de descodificación más rápido. El comportamiento exacto depende de la implementación del descodificador. No todos los incrementos entre 1 y 32 que define necesariamente es un modo distinto.

La enumeración [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene algunos modos predefinidos para esta propiedad.

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

 

 




