---
description: Especifica el identificador de hardware PnP-X del servicio.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996532"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Especifica el identificador de hardware PnP-X del servicio. PnP coincide con este elemento con las descripciones de hardware proporcionadas en la \[ sección PnpxDevice \] del archivo INF del dispositivo. En función de esta información, el servicio PnP selecciona y carga el controlador de dispositivo más adecuado.

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



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




