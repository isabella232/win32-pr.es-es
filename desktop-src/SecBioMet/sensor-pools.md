---
title: Grupos de sensores
description: Describe tres posibles sistemas de grupos de sensores, privados y sin firma.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071186"
---
# <a name="sensor-pools"></a>Grupos de sensores

Para admitir tanto Windows de autenticación como la autenticación definida por el proveedor, el servicio Windows Biometric organiza las unidades biométricas en tres posibles grupos de sensores:

-   **Grupo privado** una colección de unidades biométricas asignadas para uso exclusivo por una aplicación cliente. Los grupos privados pueden admitir escenarios de autenticación que no están basados en Windows y hacen posible que una aplicación acceda al hardware de una unidad biométrica de forma definida por el proveedor. Puede haber tantos grupos de sensores privados en el sistema como unidades biométricas.
-   **El sensor del sistema agrupa** una colección de unidades biométricas compartibles que proporcionan acceso a Windows servicios de autenticación. Winlogon, UAC y cualquier otro cliente que asocie un SID a una plantilla biométrica específica usan este grupo. Cada proveedor de servicios biométricos tiene un grupo de sensores del sistema.
-   **El grupo sin asignar** contiene una colección (posiblemente vacía) de unidades biométricas que no están asignadas al grupo del sistema o al grupo privado.

Las aplicaciones pueden usar el grupo de sistemas compartidos o pueden crear un grupo privado que se conste de unidades biométricas quitadas del sistema o grupos sinsignar. Cuando una aplicación libera su grupo privado, las unidades biométricas se reconfiguran y se devuelven a sus grupos originales. Para evitar ataques por denegación de servicio, solo los usuarios con privilegios pueden quitar el último sensor del grupo del sistema. Para obtener más información, vea los temas siguientes:

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Grupo de sensores privado](private-sensor-pool.md)<br/>   | Colección de unidades biométricas reservadas para uso exclusivo por una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente acceda a una unidad biométrica mediante comandos de control especificados por el proveedor.<br/> |
| [Grupo de sensores del sistema](system-sensor-pool.md)<br/>     | Colección de unidades biométricas compartibles que proporcionan acceso a Windows servicios de autenticación. Winlogon, UAC y cualquier otro cliente que asocie un SID a una plantilla biométrica específica usan este grupo.<br/>                                 |
| [Comportamiento del grupo de sistemas](system-pool-behavior.md)<br/> | Explicación sobre las acciones realizadas por el grupo del sistema cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows Biometric Framework API](./biometric-service-api-portal.md)
</dt> </dl>

 

