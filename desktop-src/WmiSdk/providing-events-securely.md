---
description: Puede impedir que usuarios no autorizados reciban eventos a los que no deberían tener acceso.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Proporcionar eventos de forma segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278206"
---
# <a name="providing-events-securely"></a>Proporcionar eventos de forma segura

Puede impedir que usuarios no autorizados reciban eventos a los que no deberían tener acceso. El proveedor de eventos puede proporcionar instancias de sus propias clases de eventos, del mismo modo que el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) proporciona clases como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). El proveedor de eventos también puede ofrecer eventos intrínsecos como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md). Para obtener más información, consulte [escribir un proveedor de eventos](writing-an-event-provider.md).

Un proveedor de eventos puede controlar el acceso a los destinatarios de eventos de las siguientes maneras:

-   El uso del control de acceso mediante la implementación de [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) es la manera más eficaz.

    El proveedor determina si el consumidor tiene privilegios para recibir un evento solicitado. Si el consumidor no tiene suficientes privilegios para registrarse, WMI devuelve un error de acceso denegado. Utilice este modo cuando el proveedor pueda tomar la decisión sobre quién puede recibir eventos. Por ejemplo, un proveedor puede proporcionar eventos relacionados con la seguridad y puede requerir que el consumidor tenga privilegios de administrador con el privilegio **SeSecurityPrivilege** habilitado.

-   La implementación de [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) en el receptor usado para generar eventos permite configurar un descriptor de seguridad (SD) en un receptor para todos los eventos que pasan a través.

    WMI realiza comprobaciones de acceso basadas en SD. Utilice este modo cuando el proveedor no pueda tomar la decisión con respecto a quién tiene permiso para consumir sus eventos, pero puede decidir en un SD para un receptor específico. Por ejemplo, use [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) si el proveedor de eventos obtuvo varios receptores mediante llamadas a [**IWbemEventSink:: GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) y desea un descriptor de seguridad para cada receptor.

-   El establecimiento de la propiedad **\_ descriptor de seguridad** de un evento permite la configuración de un SD para cada evento.

    Utilice este enfoque cuando cada evento entregado al receptor puede tener distintos descriptores de seguridad. Para usar este enfoque, derive cualquiera de las clases de eventos extrínsecos definidas por el proveedor de [**\_ \_ Event**](--event.md) o [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) , de modo que la clase contenga la propiedad del **\_ descriptor de seguridad** . Por ejemplo, el proveedor de eventos puede publicar eventos seguros y normales a través de un receptor. En este caso, utilice el descriptor de seguridad de la cuenta de administradores para eventos seguros y un descriptor de seguridad **null** para los eventos normales que puede recibir cualquier usuario.

## <a name="securing-events-by-decoupled-event-providers"></a>Protección de eventos por parte de proveedores de eventos desacoplados

Los proveedores de eventos desacoplados difieren de los proveedores de eventos nondecoupled en la forma en que se registran en WMI. La llamada a [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) para eventos de un proveedor desacoplado nunca propaga el token de acceso de cliente. WMI controla el control de acceso de la misma manera que para los proveedores de eventos nondecoupled. Para obtener más información sobre cómo escribir un proveedor desacoplado, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

Solo los administradores con el privilegio de **\_ escritura completo** establecido en el **control WMI** del **Panel de control** pueden generar eventos para un espacio de nombres. Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 
