---
title: Interfaces de virtualización Escritorio remoto
description: La API de virtualización de Escritorio remoto admite las siguientes interfaces.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359175"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Interfaces de virtualización Escritorio remoto

La API de virtualización de Escritorio remoto admite las siguientes interfaces.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Expone métodos que notifican el estado y los mensajes de error a Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Expone métodos y propiedades que almacenan información de estado sobre una solicitud de conexión entrante desde un cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Se puede usar para definir las propiedades personalizadas de una conexión de cliente según corresponda.

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Expone métodos y propiedades que contienen información sobre el entorno que hospeda el equipo de destino. Esta interfaz se puede usar para almacenar información sobre un servidor físico que hospeda máquinas virtuales.

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Se puede usar para definir las propiedades personalizadas de un entorno que hospede los equipos de destino según corresponda.

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Filtrar el almacén de complementos

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Expone métodos que notifican la finalización de y obtiene el tiempo de espera del agente de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Expone métodos que consultan los equipos de destino, las sesiones, los entornos y las granjas de servidores que se han agregado al almacén de agentes de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Expone métodos y propiedades que almacenan el nombre de destino devuelto por un algoritmo de equilibrio de carga.

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Expone métodos que se pueden usar para proporcionar un algoritmo de equilibrio de carga personalizado.

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Expone métodos que devuelven el resultado de un algoritmo de equilibrio de carga al agente de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Expone los métodos que usa el agente de conexión a escritorio remoto para asegurarse de que el destino está listo antes de que un cliente se redirija a él.

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Expone métodos que devuelven un objeto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) al agente de conexión a escritorio remoto después de preparar correctamente el destino para una conexión.

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Expone métodos que preparan el entorno (el equipo que hospeda la máquina virtual).

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Expone métodos que devuelven información acerca de los entornos al agente de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Expone métodos que inicializan y terminan complementos.

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Expone métodos que envían una notificación al agente de conexión a escritorio remoto sobre la inicialización o terminación de un complemento.

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Se puede usar para definir las propiedades del complemento personalizado según corresponda.

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Se puede usar para definir las propiedades personalizadas según corresponda.

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Expone métodos que crean implementaciones predeterminadas de objetos que se usan en Escritorio remoto virtualización.

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Expone métodos que crean y mantienen máquinas virtuales.

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Expone métodos que notifican al agente de conexión a escritorio remoto sobre el aprovisionamiento de máquinas virtuales.

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Expone métodos que el agente de conexión a escritorio remoto usa para notificar complementos de cualquier cambio de estado que se produzca en los objetos de conexión de cliente, destino y sesión.

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Expone métodos que el agente de conexión a escritorio remoto usa para notificar complementos de cualquier cambio de estado que se produzca en los objetos de conexión de cliente, destino y sesión.

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Expone métodos que amplían las capacidades del agente de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.

</dd> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> <dd>

Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.

</dd> <dt>

[**ITsSbServiceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

Expone los métodos que usa el agente de conexión a escritorio remoto para notificar los complementos de los cambios de estado que se producen en el propio agente de conexión a escritorio remoto.

</dd> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

Expone propiedades que almacenan información sobre una sesión de usuario.

</dd> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

Expone propiedades que almacenan información de configuración y estado sobre un destino.

</dd> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dd>

Expone propiedades que almacenan información de configuración y estado sobre un destino.

</dd> <dt>

[**ITsSbTargetPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

Derive de esta interfaz para definir un conjunto de propiedades de destino personalizado.

</dd> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

Expone propiedades que el agente de Conexión a Escritorio remoto usa para establecer la cola de un complemento.

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Expone métodos que actualizan la cola de tareas para los complementos de Conexión a Escritorio remoto Broker.

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Expone métodos que notifican el estado y los mensajes de error sobre las tareas del agente de conexión a escritorio remoto.

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Se usa para ampliar las capacidades de Terminal Services agente de sesiones (agente de sesiones de TS). Implemente esta interfaz cuando desee proporcionar un complemento que invalide la lógica de redirección del agente de sesiones de TS.

</dd> </dl>

 

 