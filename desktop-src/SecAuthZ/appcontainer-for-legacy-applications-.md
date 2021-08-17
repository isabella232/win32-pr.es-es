---
description: El entorno AppContainer es un entorno de ejecución de procesos restrictivo que se puede usar para que las aplicaciones heredadas proporcionen seguridad de recursos.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: AppContainer para aplicaciones heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e0cdf21fc4008f1da0d55edb17abaf71978f4a5384843ecff60793b3d5b19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784738"
---
# <a name="appcontainer-for-legacy-applications"></a>AppContainer para aplicaciones heredadas

El entorno AppContainer es un entorno de ejecución de procesos restrictivo que se puede usar para que las aplicaciones heredadas proporcionen seguridad de recursos. Una aplicación que se ejecuta en un AppContainer solo puede acceder a los recursos que se le conceden específicamente. Como resultado, las aplicaciones implementadas en appContainer no se pueden piratear para permitir acciones malintencionadas fuera de los recursos asignados limitados.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Ventajas de usar un entorno de AppContainer

El entorno AppContainer proporciona un espacio aislado seguro de las aplicaciones. Esto aísla la aplicación del acceso a hardware, archivos, registro, otras aplicaciones, conectividad de red y recursos de red sin permiso específico. Los recursos individuales pueden tener como destino sin exponer otros recursos. Además, la identidad del usuario se protege mediante una identidad única que es una concatenación del usuario y la aplicación y los recursos se conceden mediante un modelo con privilegios mínimos. Esto protege aún más contra una aplicación que suplanta al usuario para obtener acceso a otros recursos.

Para obtener más información sobre el uso de AppContainer para aplicaciones heredadas, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aislamiento de AppContainer](appcontainer-isolation.md)<br/>             | El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer. Al aislar una aplicación de recursos innecesarios y otras aplicaciones, se minimizan las oportunidades de manipulación malintencionada. La concesión de acceso basada en privilegios mínimos impide que las aplicaciones y los usuarios accedan a recursos más allá de sus derechos. El control del acceso a los recursos protege el proceso, el dispositivo y la red.<br/> |
| [Implementación de un elemento AppContainer](implementing-an-appcontainer.md)<br/> | Un Elemento AppContainer se implementa agregando nueva información al token de proceso, cambiando [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos los objetos heredados de la lista de control de acceso (ACL) sin modificar bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada y los objetos de acl de nuevo que deben estar disponibles para AppContainers.<br/>                                                                                        |



 

 

