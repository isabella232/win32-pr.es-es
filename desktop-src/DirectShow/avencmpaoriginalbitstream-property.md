---
description: Especifica el valor predeterminado para el bit original en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propiedad AVEncMPAOriginalBitstream (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161859"
---
# <a name="avencmpaoriginalbitstream-property"></a>Propiedad AVEncMPAOriginalBitstream

Especifica el valor predeterminado para el bit original en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción          |
|----------------|----------------------|
| VARIANT \_ FALSE | El bit original está desactivado. |
| VARIANT \_ TRUE  | El bit original está en.  |



 

## <a name="remarks"></a>Observaciones

El codificador podría invalidar esta configuración, en función del contenido del flujo de entrada.

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

 

 




