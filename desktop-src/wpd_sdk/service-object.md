---
description: Objeto de servicio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572044"
---
# <a name="service-object"></a>Objeto de servicio

El objeto de servicio debe admitir las siguientes propiedades.



| Nombre de la propiedad                                                                                                                      | Obligatorio u opcional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Necesario. .                                                                           |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Necesario.                                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Necesario.                                                                             |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Necesario.                                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto de servicio no debe mostrarse al usuario.                       |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obligatorio si el objeto es un objeto del sistema (por ejemplo, representa un archivo del sistema). |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Necesario. Representa el tipo de Servicio de dispositivo, como Contactos de SERVICIO.          |
| [VERSIÓN DEL \_ SERVICIO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Necesario.                                                                             |
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

 

 
