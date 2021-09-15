---
description: Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor utilizado para almacenar el contenido comprimido.
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: MFPKEY_ASFOVERHEADPERFRAME (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 208acf55871b18bb029279a27abd36a33ea8c79c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468654"
---
# <a name="mfpkey_asfoverheadperframe-property"></a>Propiedad \_ ASFOVERHEADPERFRAME de MFPKEY

Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor utilizado para almacenar el contenido comprimido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVPacketOverhead

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

17

## <a name="remarks"></a>Observaciones

Si usa la estructura de archivos de formato de sistemas avanzados (ASF), no cambie este valor de su valor predeterminado. Si no almacena los datos en un archivo ASF, debe establecer este valor en 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




