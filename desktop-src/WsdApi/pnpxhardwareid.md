---
description: Especifica el identificador de hardware PnP-X del servicio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d032974486d4bd43f0a699eba6b8f6b75598c49858eeedb09bae5d3e79b11e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311520"
---
# <a name="pnpxhardwareid-element"></a>PnPXHardwareId, elemento

Especifica el identificador de hardware PnP-X del servicio. PnP coincide con este elemento con las descripciones de hardware proporcionadas en la \[ sección PnpxDevice del archivo INF del \] dispositivo. En función de esta información, el servicio PnP selecciona y carga el controlador de dispositivo más adecuado.

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
| [**Alojados**](hosted.md)<br/> | Define elementos para los servicios definidos por el host de servicio. <br/> <br/> |



## <a name="remarks"></a>Comentarios

Para especificar más de un identificador de hardware, separe los identificadores con un carácter de espacio, por ejemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




