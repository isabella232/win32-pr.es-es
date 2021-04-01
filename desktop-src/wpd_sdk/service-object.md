---
description: Objeto de servicio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913289"
---
# <a name="service-object"></a>Objeto de servicio

El objeto de servicio debe admitir las siguientes propiedades.



| Nombre de la propiedad                                                                                                                      | Obligatorio u opcional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obligatorio. .                                                                           |
| [\_ \_ ID. primario del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obligatorio.                                                                             |
| [\_nombre del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obligatorio.                                                                             |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obligatorio.                                                                             |
| [\_objeto WPD \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto de servicio no se debe mostrar al usuario.                       |
| [\_objeto WPD \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto es un objeto del sistema (por ejemplo, representa un archivo del sistema). |
| [\_categoría de \_ objeto \_ funcional de WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obligatorio. Representa el tipo de servicio de dispositivo, como los contactos de servicio.          |
| [\_versión del servicio WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio.                                                                             |
| [\_tipo de almacenamiento de WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Obligatorio si el servicio se utiliza para almacenar objetos.                                     |
| [\_capacidad de almacenamiento de WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Obligatorio si el servicio se utiliza para almacenar objetos.                                     |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="typical-formats"></a>Formatos típicos

En la siguiente lista se identifican los formatos típicos utilizados por el objeto de servicio. Sin embargo, este objeto no se limita a estos formatos.

-   formato de objeto WPD no \_ \_ \_ especificado

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 
