---
description: Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción estéreo, o bien una reducción no estándar.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propiedad AVDecAACDownmixMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162162"
---
# <a name="avdecaacdownmixmode-property"></a>Propiedad AVDecAACDownmixMode

Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción estéreo, o bien una reducción no estándar.

Un ejemplo de una mezcla anterior no estándar es la definida por el documento STD-B21 de ARIB, versión 4.4.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecAACDownmixMode.**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio aplicaciones para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

