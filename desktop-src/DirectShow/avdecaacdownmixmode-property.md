---
description: Especifica si un descodificador AAC usa ecuaciones downmix de estéreo estándar MPEG-2/MPEG-4, o usa un downmix no estándar.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propiedad AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686382"
---
# <a name="avdecaacdownmixmode-property"></a>Propiedad AVDecAACDownmixMode

Especifica si un descodificador AAC usa ecuaciones downmix de estéreo estándar MPEG-2/MPEG-4, o usa un downmix no estándar.

Un ejemplo de downmix no estándar es el que se define en el documento ARIB STD-B21, versión 4,4.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .

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

 

