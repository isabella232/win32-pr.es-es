---
title: Jerarquía del modelo de objetos
description: Los objetos del modelo de objetos SDO se organizan en una jerarquía. Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f63b5692571bab49580251d6ef879adde8ae9a57af4c541404aabc48538e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063354"
---
# <a name="object-model-hierarchy"></a>Jerarquía del modelo de objetos

Los objetos del modelo de objetos SDO se organizan en una jerarquía. Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.

Los objetos proporcionan acceso a otros objetos de dos maneras. Una manera es que el objeto exponga una interfaz que proporciona métodos para recuperar otros objetos. Un ejemplo de este enfoque es el objeto Machine. El objeto Machine expone la [**interfaz ISdoMachine.**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) El [**método ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un objeto Service. El [**método ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un objeto User.

![objeto de máquina que expone la interfaz isdomachine](images/sdo01.png)

Para obtener más información, consulte [Obtención de SLO de servicio y usuario.](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos)

La segunda manera en que los objetos proporcionan acceso a otros objetos es que una colección de objetos se representa como una propiedad del objeto que la contiene. Para recuperar una colección de objetos, llame [**a ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) en la propiedad de un objeto que representa la colección. Por ejemplo, para recuperar la colección Policies, llame a **ISdo::GetProperty** en la [**interfaz ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) expuesta por el objeto NPS.

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008.

 

![recuperar la colección de directivas](images/sdo02.png)

Para obtener código de ejemplo que recupera la colección Policies, vea [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).

El [**objeto de datos del servidor NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) tiene las siguientes propiedades que representan colecciones:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditores
</dt> <dd>

El único auditor de la colección Auditors es el registro [**de eventos NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Políticas
</dt> <dd>

Cada [**objeto de**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) directiva tiene una propiedad que representa una colección de condiciones.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Perfiles
</dt> <dd>

Cada [**objeto de perfil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) de las colecciones Profiles tiene una propiedad que representa una colección de atributos. Consulte [Atributos admitidos por SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) para obtener una lista de los atributos admitidos por SDO.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolos
</dt> <dd>

La colección de protocolos contiene el objeto de protocolo RADIUS, que contiene una colección de clientes que representa clientes RADIUS. Vea [Agregar un cliente para](/windows/desktop/Nps/sdo-adding-a-client) obtener código de ejemplo que muestra cómo recuperar la colección de cliente.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Directivas de proxy
</dt> <dd>

Esta colección contiene las directivas de acceso a la red que se usan para el procesamiento de solicitudes de conexión.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Perfiles de proxy
</dt> <dd>

Esta colección contiene perfiles usados para el procesamiento de solicitudes de conexión.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Grupos de servidores RADIUS
</dt> <dd>

Cada [**grupo de servidores RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) de la colección Grupos de servidores RADIUS tiene una propiedad que representa la colección de servidores de ese grupo de servidores.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Controladores de solicitudes
</dt> <dd>

Esta colección contiene la colección "Evaluador de dominios de Microsoft". Las opciones "Autenticación SAM de Microsoft NT" y "Cuentas de Microsoft" también están disponibles en esta colección.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos y propiedades de SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Atributos admitidos por SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 