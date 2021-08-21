---
title: Escritorio remoto interfaces de virtualización
description: La API Escritorio remoto Virtualization admite las interfaces siguientes.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4627b29bcb5fba6518d89a4d92eca48e2665a6bda98f724a0219de5fca884f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118851851"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Escritorio remoto interfaces de virtualización

La API Escritorio remoto Virtualization admite las interfaces siguientes.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Expone métodos que informan del estado y los mensajes de error a Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Expone métodos y propiedades que almacenan información de estado sobre una solicitud de conexión entrante desde un cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Se puede usar para definir propiedades personalizadas de una conexión de cliente según corresponda.

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Expone métodos y propiedades que contienen información sobre el entorno que hospeda el equipo de destino. Esta interfaz se puede usar para almacenar información sobre un servidor físico que hospeda máquinas virtuales.

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Se puede usar para definir propiedades personalizadas de un entorno que hospeda equipos de destino según corresponda.

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Filtrar almacén de complementos

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Expone métodos que informan de la finalización a y obtiene el tiempo de espera del Agente de conexión a Escritorio remoto.

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Expone métodos que consultan equipos de destino, sesiones, entornos y granjas de servidores que se han agregado al almacén del Agente de conexión a Escritorio remoto.

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Expone métodos y propiedades que almacenan el nombre de destino devuelto por un algoritmo de equilibrio de carga.

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Expone métodos que puede usar para proporcionar un algoritmo de equilibrio de carga personalizado.

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Expone métodos que devuelven el resultado de un algoritmo de equilibrio de carga al Agente de conexión a Escritorio remoto.

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Expone los métodos que usa el Agente de conexión a Escritorio remoto para asegurarse de que el destino está listo antes de que se le redirija un cliente.

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Expone métodos que devuelven un [**objeto ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) al Agente de conexión a Escritorio remoto después de que el destino se haya preparado correctamente para una conexión.

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Expone métodos que preparan el entorno (el equipo que hospeda la máquina virtual).

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Expone métodos que devuelven información sobre los entornos al Agente de conexión a Escritorio remoto.

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Expone métodos que inicializan y finalizan complementos.

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Expone métodos que notifican al Agente de conexión a Escritorio remoto la inicialización o finalización de un complemento.

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Se puede usar para definir propiedades de complemento personalizadas según corresponda.

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Se puede usar para definir propiedades personalizadas según corresponda.

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Expone métodos que crean implementaciones predeterminadas de objetos que se usan en Escritorio remoto Virtualización.

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Expone métodos que crean y mantienen máquinas virtuales.

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Expone métodos que notifican al Agente de conexión a Escritorio remoto sobre el aprovisionamiento de máquinas virtuales.

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Expone los métodos que usa el Agente de conexión a Escritorio remoto para notificar a los complementos los cambios de estado que se producen en los objetos de conexión de sesión, destino y cliente.

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Expone los métodos que usa el Agente de conexión a Escritorio remoto para notificar a los complementos los cambios de estado que se producen en los objetos de conexión de sesión, destino y cliente.

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Expone métodos que amplían las funciones del Agente de conexión a Escritorio remoto.

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

Expone los métodos que usa el Agente de conexión a Escritorio remoto para notificar a los complementos los cambios de estado que se producen en el propio Agente de conexión a Escritorio remoto.

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

Expone las propiedades que usa Conexión a Escritorio remoto Broker para establecer la cola de un complemento.

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Expone métodos que actualizan la cola de tareas para Conexión a Escritorio remoto complementos de Broker.

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Expone métodos que informan del estado y los mensajes de error sobre las tareas al Agente de conexión a Escritorio remoto.

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Se usa para ampliar las funcionalidades del Agente de sesión de Terminal Services (TS Session Broker). Implemente esta interfaz cuando desee proporcionar un complemento que invalide la lógica de redireccionamiento del Agente de sesión de TS.

</dd> </dl>

 

 