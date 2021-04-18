---
description: Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectado por el origen de red.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Propiedad MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720470"
---
# <a name="mfnetsource_ppbandwidth-property"></a>\_Propiedad PPBANDWIDTH de MFNETSOURCE

Especifica el ancho de banda del par de paquetes y el ancho de banda en tiempo de ejecución detectado por el origen de red. El valor de la propiedad es una matriz de dos valores:

-   Ancho de banda de pares de paquetes, en bits por segundo.
-   Ancho de banda en tiempo de ejecución, en bits por segundo.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Matriz de valores **ULong** (**caul**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PPBANDWIDTH** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Esta propiedad es de solo lectura. Para recuperar esta propiedad, consulte el origen de red para la interfaz **IPropertyStore** y llame a **IPropertyStore:: GetValue**.

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

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




