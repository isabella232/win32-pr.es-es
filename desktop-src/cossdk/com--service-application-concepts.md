---
description: Conceptos de la aplicación de servicio COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Conceptos de la aplicación de servicio COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973524"
---
# <a name="com-service-application-concepts"></a>Conceptos de la aplicación de servicio COM+

Puede usar la herramienta administrativa Servicios de componentes para configurar una aplicación de servidor COM+ como una aplicación de servicio. La ejecución de una aplicación de servidor COM+ como servicio ofrece las siguientes ventajas:

-   Si la aplicación siempre necesita ejecutarse, servicios de componentes puede hacer que el servidor se inicie automáticamente y también puede reiniciar el servidor si se agota el tiempo de espera. Por ejemplo, si se reinicia un equipo que ejecuta componentes de escucha de componentes en cola, los agentes de escucha de componentes en cola se pueden iniciar automáticamente si están configurados como un servicio.
-   Si la aplicación necesita realizar operaciones con privilegios, la aplicación puede ejecutarse como la cuenta del sistema local. Solo los servicios NT pueden ejecutarse con este nivel de seguridad. La aplicación será compatible con la aplicación Windows Servicio de clúster, que administra los servicios durante la conmutación por error del sistema.
-   Si otros servicios deben marcarse como dependientes, Servicios de componentes proporciona esa opción. Por ejemplo, si la aplicación usa la funcionalidad proporcionada por otro servicio, el servicio marcado como dependiente se iniciará antes de que se inicie la aplicación.

## <a name="starting-an-application-automatically"></a>Iniciar una aplicación automáticamente

Cuando la aplicación de servidor COM+ se inicia automáticamente, actúa como un servicio, lo que requiere que el desarrollador administre el servidor mediante la herramienta administrativa Servicios.

> [!Note]  
> Para acceder a la herramienta administrativa Servicios, inicie la herramienta administrativa Servicios de componentes y, a continuación, haga clic **en Servicios (local).**

 

## <a name="starting-an-application-manually"></a>Iniciar una aplicación manualmente

Cuando la aplicación de servidor COM+ se inicia manualmente, actúa como un host DLL con la configuración de seguridad de un servicio. El servicio se iniciará manualmente cuando se active y se apague automáticamente cuando se haya pasado el tiempo de espera.

## <a name="service-configurations"></a>Configuraciones de servicio

Independientemente del tipo de inicio, la aplicación se puede configurar para ejecutarse como una cuenta de sistema local o asignarse a una cuenta de usuario. El sistema local y la cuenta de usuario se pueden configurar en el momento de crear el servicio. Para configurar las opciones de seguridad, se tendrá que usar la herramienta administrativa Servicios. También se pueden establecer dependencias para el servicio.

La aplicación también se puede iniciar en cualquier orden concreto seleccionando dependencias de una lista de otros servicios del sistema. Por ejemplo, los servicios del sistema se pueden marcar como dependientes y no iniciarán la aplicación hasta que los servicios del sistema se hayan iniciado en el orden especificado. Esto inicializará correctamente la aplicación de servicio antes de que se utilice.

Para obtener instrucciones paso a paso sobre cómo configurar una aplicación COM+ para que se ejecute como servicio, consulte Configuración de una aplicación de servidor [COM+ como una aplicación de servicio.](configuring-a-com--server-application-as-a-service-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de aplicación de servicio COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



