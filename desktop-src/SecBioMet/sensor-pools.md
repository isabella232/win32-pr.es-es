---
title: Grupos de sensores
description: 'Describe tres posibles grupos de sensores: sistema, privado y sin asignar.'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420950"
---
# <a name="sensor-pools"></a>Grupos de sensores

Para admitir escenarios de autenticación de Windows y la autenticación definida por el proveedor, el servicio biométrico de Windows organiza las unidades biométricas en tres grupos de sensores posibles:

-   **Grupo privado** : colección de unidades biométricas asignadas para uso exclusivo por parte de una aplicación cliente. Los grupos privados pueden admitir escenarios de autenticación que no están basados en Windows y permiten que una aplicación tenga acceso al hardware de una unidad biométrica en un modo definido por el proveedor. Puede haber tantos grupos de sensores privados en el sistema como unidades biométricas.
-   **Grupo de sensores del sistema** : colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows. Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo. Cada proveedor de servicios biométricos tiene un grupo de sensores del sistema.
-   El **grupo sin asignar** contiene una colección (posiblemente vacía) de unidades biométricas que no están asignadas al grupo de sistema o al grupo privado.

Las aplicaciones pueden usar el grupo de sistema compartido o pueden crear un grupo privado compuesto por unidades biométricas quitadas del sistema o de grupos sin asignar. Cuando una aplicación libera su grupo privado, las unidades biométricas se reconfiguran y se devuelven a sus grupos originales. Para evitar ataques de denegación de servicio, solo los usuarios con privilegios pueden quitar el último sensor del grupo del sistema. Para obtener más información, vea los siguientes temas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Grupo de sensores privados](private-sensor-pool.md)<br/>   | Colección de unidades biométricas reservadas para uso exclusivo de una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente tenga acceso a una unidad biométrica mediante los comandos de control especificados por el proveedor.<br/> |
| [Grupo de sensores del sistema](system-sensor-pool.md)<br/>     | Colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows. Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo.<br/>                                 |
| [Comportamiento del grupo de sistemas](system-pool-behavior.md)<br/> | Debate sobre las acciones realizadas por el grupo del sistema cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de Plataforma de biometría de Windows](./biometric-service-api-portal.md)
</dt> </dl>

 

