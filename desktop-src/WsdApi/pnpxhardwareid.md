---
description: Especifica el identificador de hardware PnP-X del servicio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696903"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Especifica el identificador de hardware PnP-X del servicio. PnP coincide con este elemento con las descripciones de hardware proporcionadas en la \[ \] sección PnpxDevice del archivo INF del dispositivo. En función de esta información, el servicio PnP selecciona y carga el controlador de dispositivo más adecuado.

## <a name="usage"></a>Uso

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                             | Descripción                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**ubicada**](hosted.md)<br/> | Define los elementos para los servicios definidos por el host de servicio. <br/> <br/> |



## <a name="remarks"></a>Observaciones

Para especificar más de un identificador de hardware, separe los identificadores con un carácter de espacio, por ejemplo, "PnPX SampleService de juegos de software \_ \_ \_ 1 PnPX SampleService de hardware \_ \_ \_ 2 PnPX \_ SampleService1 de \_ hardware \_ 3".

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




