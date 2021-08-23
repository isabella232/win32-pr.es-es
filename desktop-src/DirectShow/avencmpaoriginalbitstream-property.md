---
description: Especifica el valor predeterminado para el bit original en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propiedad AVEncMPAOriginalBitstream (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d39b34339e25d08b138fd1c55a64e8a84d6cf4b4db302cbab1e5f50b8ccebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689745"
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



| Valor          | Descripción          |
|----------------|----------------------|
| VARIANT \_ FALSE | El bit original está desactivado. |
| VARIANT \_ TRUE  | El bit original está en.  |



 

## <a name="remarks"></a>Comentarios

El codificador podría invalidar esta configuración, en función del contenido del flujo de entrada.

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

 

 




