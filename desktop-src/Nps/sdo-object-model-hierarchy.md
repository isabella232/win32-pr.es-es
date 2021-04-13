---
title: Jerarquía del modelo de objetos
description: Los objetos del modelo de objetos SDO están organizados en una jerarquía. Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420994"
---
# <a name="object-model-hierarchy"></a>Jerarquía del modelo de objetos

Los objetos del modelo de objetos SDO están organizados en una jerarquía. Esto significa que los objetos de SDO proporcionan acceso a otros objetos en SDO.

Los objetos proporcionan acceso a otros objetos de dos maneras. Una manera es que el objeto exponga una interfaz que proporciona métodos para recuperar otros objetos. Un ejemplo de este enfoque es el objeto de equipo. El objeto de equipo expone la interfaz [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) . El método [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un objeto de servicio. El método [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un objeto de usuario.

![objeto de equipo que expone la interfaz isdomachine](images/sdo01.png)

Para obtener más información, vea [obtener el servicio y el usuario SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

La segunda manera en que los objetos proporcionan acceso a otros objetos es que una colección de objetos se representa como una propiedad del objeto que lo contiene. Para recuperar una colección de objetos, llame a [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) en la propiedad de un objeto que representa la colección. Por ejemplo, para recuperar la colección de directivas, llame a **ISdo:: GetProperty** en la interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) expuesta por el objeto NPS.

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.

 

![recuperación de la colección de directivas](images/sdo02.png)

Para obtener el código de ejemplo que recupera la colección de directivas, consulte [recuperar una colección](/windows/desktop/Nps/sdo-retrieving-a-collection).

El [**objeto de datos del servidor NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) tiene las siguientes propiedades que representan colecciones:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditores
</dt> <dd>

El único Auditor de la colección de auditores es el [**registro de eventos de NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Políticas
</dt> <dd>

Cada [**objeto de directiva**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) tiene una propiedad que representa una colección de condiciones.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>File
</dt> <dd>

Cada [**objeto de perfil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) de las colecciones de perfiles tiene una propiedad que representa una colección de atributos. Vea [atributos compatibles con SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) para obtener una lista de los atributos admitidos por SDO.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolos
</dt> <dd>

La colección Protocols contiene el objeto de protocolo RADIUS, que contiene una colección de clientes que representa clientes RADIUS. Consulte [Agregar un cliente](/windows/desktop/Nps/sdo-adding-a-client) para ver el código de ejemplo que muestra cómo recuperar la colección de clientes.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Directivas de proxy
</dt> <dd>

Esta colección contiene las directivas de acceso a redes utilizadas para el procesamiento de solicitudes de conexión.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Perfiles de proxy
</dt> <dd>

Esta colección contiene perfiles usados para el procesamiento de solicitudes de conexión.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Grupos de servidores RADIUS
</dt> <dd>

Cada [**grupo de servidores RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) de la colección de grupos de servidores RADIUS tiene una propiedad que representa la colección de servidores de ese grupo de servidores.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Controladores de solicitud
</dt> <dd>

Esta colección contiene la colección "Microsoft Realms Evaluator". La configuración de "autenticación de Microsoft NT SAM" y "cuentas de Microsoft" también está disponible en esta colección.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos SDO y propiedades](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Atributos compatibles con SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 