---
description: Objeto de servicio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445594"
---
# <a name="service-object"></a>Objeto de servicio

El objeto de servicio debe admitir las siguientes propiedades.



| Nombre de la propiedad                                                                                                                      | Obligatorio u opcional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obligatorio. .                                                                           |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obligatorio.                                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obligatorio.                                                                             |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obligatorio.                                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto de servicio no debe mostrarse al usuario.                       |
| [WPD \_ OBJECT \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto es un objeto del sistema (por ejemplo, representa un archivo del sistema). |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obligatorio. Representa el tipo de Servicio de dispositivo, como Contactos de SERVICIO.          |
| [VERSIÓN DEL SERVICIO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio.                                                                             |
| [TIPO DE \_ ALMACENAMIENTO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Obligatorio si el servicio se usa para almacenar objetos.                                     |
| [CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Obligatorio si el servicio se usa para almacenar objetos.                                     |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="typical-formats"></a>Formatos típicos

En la lista siguiente se identifican los formatos típicos usados por el objeto Service. Sin embargo, este objeto no se limita a estos formatos.

-   FORMATO DE \_ OBJETO \_ WPD \_ SIN ESPECIFICAR

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 
