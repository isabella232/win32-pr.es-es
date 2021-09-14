---
description: Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propiedad AVEncMPACopyright (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161872"
---
# <a name="avencmpacopyright-property"></a>AvEncMPACopyright, propiedad

Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción           |
|----------------|-----------------------|
| VARIANT \_ FALSE | El bit de copyright está desactivado. |
| VARIANT \_ TRUE  | El bit de copyright está en.  |



 

## <a name="remarks"></a>Observaciones

El codificador puede invalidar esta configuración, en función del contenido de la secuencia de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




