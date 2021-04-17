---
description: El entorno AppContainer es un entorno de ejecución de procesos restrictivo que se puede usar para que las aplicaciones heredadas proporcionen seguridad de los recursos.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer para aplicaciones heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b25ea292bdb8935375e50f669d17deb7efaef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653071"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer para aplicaciones heredadas

El entorno AppContainer es un entorno de ejecución de procesos restrictivo que se puede usar para que las aplicaciones heredadas proporcionen seguridad de los recursos. Una aplicación que se ejecuta en un AppContainer solo puede tener acceso a los recursos que se le conceden específicamente. Como resultado, las aplicaciones implementadas en un AppContainer no se pueden atacar para permitir acciones malintencionadas fuera de los recursos asignados limitados.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Ventajas del uso de un entorno AppContainer

El entorno AppContainer proporciona un espacio aislado seguro de aplicaciones. Esto aísla la aplicación del acceso al hardware, los archivos, el registro, otras aplicaciones, la conectividad de red y los recursos de red sin permiso específico. Los recursos individuales se pueden destinar sin exponer otros recursos. Además, la identidad del usuario se protege mediante el uso de una identidad única que es una concatenación del usuario, y la aplicación y los recursos se conceden mediante un modelo con privilegios mínimos. Esto protege aún más en una aplicación que suplanta al usuario para obtener acceso a otros recursos.

Para obtener más información sobre el uso de AppContainer para aplicaciones heredadas, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aislamiento de AppContainer](appcontainer-isolation.md)<br/>             | El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer. Al aislar una aplicación de recursos innecesarios y otras aplicaciones, se minimizan las oportunidades de manipulación malintencionada. Conceder acceso basado en privilegios mínimos evita que las aplicaciones y los usuarios tengan acceso a recursos más allá de sus derechos. Controlar el acceso a los recursos protege el proceso, el dispositivo y la red.<br/> |
| [Implementar un AppContainer](implementing-an-appcontainer.md)<br/> | Un AppContainer se implementa agregando nueva información al token de proceso, cambiando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos los objetos de la lista de control de acceso (ACL) heredados y no modificados bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada, y vuelva a crear los objetos de ACL que deben estar disponibles para AppContainers.<br/>                                                                                        |



 

 

