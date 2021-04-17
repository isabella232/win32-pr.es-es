---
description: Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propiedad AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659279"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Propiedad AVEncMPAEnableRedundancyProtection

Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción                |
|----------------|----------------------------|
| VARIANTE \_ false | No agregue una suma de comprobación CRC. |
| VARIANTE \_ true  | Agregue una suma de comprobación CRC.        |



 

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

 

 




