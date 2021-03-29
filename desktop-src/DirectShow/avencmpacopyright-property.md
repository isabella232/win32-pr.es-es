---
description: Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propiedad AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423027"
---
# <a name="avencmpacopyright-property"></a>Propiedad AVEncMPACopyright

Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción           |
|----------------|-----------------------|
| VARIANTE \_ false | El bit de copyright está desactivado. |
| VARIANTE \_ true  | El bit de copyright está activado.  |



 

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

 

 




