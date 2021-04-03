---
description: Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Propiedad MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810994"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>\_Propiedad de \_ representación de licencia de MFNETSOURCE DRMNET \_

Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Matriz de bytes (**BLOB**)

BLOB de VT \_

**BLOB**



## <a name="remarks"></a>Observaciones

La **representación de \_ \_ licencia \_ Constant MFNETSOURCE DRMNET** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para obtener el valor de propiedad de la secuencia de bytes de red, llame a **IPropertyStore:: GetValue** y pase la estructura **PROPERTYKEY** en el parámetro *key* . El miembro **fmtid** de **PROPERTYKEY** debe establecerse en el GUID de la propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




