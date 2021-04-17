---
description: Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: Propiedad MFPKEY_ASFOVERHEADPERFRAME (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 208acf55871b18bb029279a27abd36a33ea8c79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697701"
---
# <a name="mfpkey_asfoverheadperframe-property"></a>\_Propiedad ASFOVERHEADPERFRAME de MFPKEY

Especifica la sobrecarga, en bytes por paquete, necesaria para el contenedor que se usa para almacenar el contenido comprimido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVPacketOverhead

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

17

## <a name="remarks"></a>Observaciones

Si usa la estructura de archivos de formato de sistema avanzado (ASF), no cambie el valor predeterminado. Si no almacena los datos en un archivo ASF, debe establecer este valor en 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




