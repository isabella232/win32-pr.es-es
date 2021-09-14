---
description: Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propiedad AVEncMPAEnableRedundancyProtection (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161869"
---
# <a name="avencmpaenableredundancyprotection-property"></a>AvEncMPAEnableRedundancyProtection, propiedad

Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción                |
|----------------|----------------------------|
| VARIANT \_ FALSE | No agregue una suma de comprobación CRC. |
| VARIANT \_ TRUE  | Agregue una suma de comprobación de CRC.        |



 

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

 

 




