---
description: Puede evitar que usuarios no autorizados reciban eventos a los que no deben tener acceso.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Proporcionar eventos de forma segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249333"
---
# <a name="providing-events-securely"></a>Proporcionar eventos de forma segura

Puede evitar que usuarios no autorizados reciban eventos a los que no deben tener acceso. El proveedor de eventos puede proporcionar instancias de [](/previous-versions/windows/desktop/regprov/system-registry-provider) sus propias clases de eventos, al igual que el proveedor del Registro del sistema proporciona clases como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). El proveedor de eventos también puede entregar eventos intrínsecos, [**\_ \_ como InstanceCreationEvent.**](--instancecreationevent.md) Para obtener más información, vea [Escribir un proveedor de eventos.](writing-an-event-provider.md)

Un proveedor de eventos puede controlar el acceso a los destinatarios de eventos de las maneras siguientes:

-   El uso del control de acceso mediante [**la implementación de IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) es la manera más eficaz.

    El proveedor determina si el consumidor tiene privilegios para recibir un evento solicitado. Si el consumidor no tiene privilegios suficientes para registrarse, WMI devuelve un error de acceso denegado. Use este modo cuando el proveedor pueda tomar la decisión sobre quién puede recibir eventos. Por ejemplo, un proveedor puede proporcionar eventos relacionados con la seguridad y puede requerir que el consumidor tenga privilegios de administrador con el privilegio **SeSecurityPrivilege** habilitado.

-   La implementación [**de IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) en el receptor utilizado para generar eventos permite establecer un descriptor de seguridad (SD) en un receptor para todos los eventos que pasan.

    WMI realiza comprobaciones de acceso basadas en la SD. Use este modo cuando el proveedor no pueda tomar la decisión sobre quién puede consumir sus eventos, pero puede decidir una SD para un receptor específico. Por ejemplo, use [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) si el proveedor de eventos obtuvo varios receptores mediante llamadas a [**IWbemEventSink::GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) y desea un descriptor de seguridad para cada receptor.

-   Establecer la **propiedad \_ DESCRIPTOR DE** SEGURIDAD de un evento permite establecer una SD para cada evento.

    Use este enfoque cuando cada evento entregado al receptor pueda tener descriptores de seguridad diferentes. Para usar este enfoque, derive cualquiera de las clases de eventos extrínsecos definidas por el proveedor de [**\_ \_ Event**](--event.md) o [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) para que la clase contenga la propiedad **DESCRIPTOR DE \_ SEGURIDAD.** Por ejemplo, el proveedor de eventos puede publicar eventos seguros y normales a través de un receptor. En este caso, use el descriptor de seguridad de la cuenta administradores para eventos seguros y un descriptor de seguridad **NULL** para los eventos normales que puede recibir cualquier persona.

## <a name="securing-events-by-decoupled-event-providers"></a>Proteger eventos mediante proveedores de eventos desacoplados

Los proveedores de eventos desacoplados difieren de los proveedores de eventos no desacoplados en la forma en que se registran con WMI. La llamada a [**IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) para eventos de un proveedor desacoplado nunca propaga el token de acceso de cliente. WMI controla el control de acceso de la misma manera que para los proveedores de eventos no desacoplados. Para obtener más información sobre cómo escribir un proveedor desacoplado, vea [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

Solo los administradores con el privilegio FULL  **\_ WRITE** establecido en el control **WMI** de la Panel de control pueden generar eventos para un espacio de nombres. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 
