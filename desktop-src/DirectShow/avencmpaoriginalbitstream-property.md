---
description: Especifica el valor predeterminado para el bit original en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propiedad AVEncMPAOriginalBitstream (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906731"
---
# <a name="avencmpaoriginalbitstream-property"></a>Propiedad AVEncMPAOriginalBitstream

Especifica el valor predeterminado para el bit original en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción          |
|----------------|----------------------|
| VARIANTE \_ false | El bit original está desactivado. |
| VARIANTE \_ true  | El bit original está activado.  |



 

## <a name="remarks"></a>Observaciones

El codificador podría invalidar esta configuración, en función del contenido del flujo de entrada.

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

 

 




