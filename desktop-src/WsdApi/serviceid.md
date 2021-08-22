---
description: URI que representa el identificador de servicio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc6ac1da57109f4f5671caf16a49b3a6174e7bfb63335d5ba15a548d7135990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756745"
---
# <a name="serviceid-element"></a>Elemento ServiceID

URI que representa el identificador de servicio.

## <a name="usage"></a>Uso

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                             | Descripción                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Host**](host.md)<br/>     | Define los **elementos ServiceID** y [**Types**](types.md) para el host de servicio. Si no se proporciona explícitamente, WSDAPI no suministrará ningún dato predeterminado en respuesta a las solicitudes de metadatos.<br/> <br/>                                                                                                                     |
| [**Alojados**](hosted.md)<br/> | Define los **elementos ServiceID** y [**Types**](types.md) para los servicios proporcionados por este host de servicio. Cada servicio proporcionado por este host [](hosted.md) de servicio debe tener su propia información de elemento hospedado para asegurarse de que el servicio se publica correctamente en respuestas a solicitudes de metadatos.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




