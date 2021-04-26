---
description: URI que representa el identificador de servicio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995112"
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



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




