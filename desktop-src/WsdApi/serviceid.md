---
description: URI que representa el identificador del servicio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707256"
---
# <a name="serviceid-element"></a>Elemento ServiceID

URI que representa el identificador del servicio.

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
| [**organizar**](host.md)<br/>     | Define los elementos **ServiceID** y [**Types**](types.md) para el host de servicio. Si no se proporciona explícitamente, WSDAPI no proporcionará datos predeterminados en respuesta a las solicitudes de metadatos.<br/> <br/>                                                                                                                     |
| [**ubicada**](hosted.md)<br/> | Define los elementos **ServiceID** y [**Types**](types.md) para los servicios proporcionados por este host de servicio. Cada servicio proporcionado por este host de servicio debe tener su propia información de elemento [**hospedado**](hosted.md) para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




