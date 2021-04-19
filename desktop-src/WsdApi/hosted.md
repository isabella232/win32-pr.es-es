---
description: Define los elementos ServiceID, Types, PnPXHardwareId y PnPXCompatibleId para los servicios definidos por el host de servicio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento hospedado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706975"
---
# <a name="hosted-element"></a>elemento hospedado

Define los elementos [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)y [**PnPXCompatibleId**](pnpxcompatibleid.md) para los servicios definidos por el host de servicio.

## <a name="usage"></a>Uso

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                 | Descripción                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | Especifica el identificador compatible con PnP-X del servicio.<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | Especifica el identificador de hardware PnP-X del servicio.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Define un identificador de servicio para el host de servicio.<br/> <br/>        |
| [**Tipos**](types.md)<br/>                       | Define una lista de nombres completos de XSD.<br/> <br/>                    |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                         | Descripción                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Los metadatos de hospedaje para el dispositivo que se va a implementar.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Cada servicio proporcionado por un host de servicio debe tener su propia información de elemento **hospedado** para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.

Los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) son opcionales, pero cuando se usan, deben usarse juntos. Si existe uno, el otro también debe estar presente.

Si hay un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , al menos un elemento **hospedado** debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) . Del mismo modo, si los elementos **PnPXHardwareId** y **PnPXCompatibleId** están presentes en un elemento **hospedado** , al menos un elemento **PnPXDeviceCategory** debe estar presente dentro del elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




