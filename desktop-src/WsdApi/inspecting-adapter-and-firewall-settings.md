---
description: Un firewall mal configurado puede provocar errores en las aplicaciones WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Inspeccionando la configuración del adaptador y del firewall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360574"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Inspeccionando la configuración del adaptador y del firewall

Un firewall mal configurado puede provocar errores en las aplicaciones WSD. En este tema se proporcionan algunos procedimientos de solución de problemas para usar cuando los hosts y los hosts WSD no se pueden ver entre sí en la red. La configuración del firewall debe inspeccionarse antes de usar cualquier otro procedimiento de solución de problemas de la aplicación.

**Para inspeccionar la configuración del adaptador y del firewall**

1.  Compruebe que la excepción **detección de redes** está habilitada.
2.  Compruebe que no hay ninguna regla de Firewall específica de la aplicación que bloquee la aplicación.
3.  Habilite explícitamente los puertos utilizados para la detección y el intercambio de metadatos.
4.  Deshabilite el firewall y pruebe de nuevamente la aplicación.
    > [!Note]  
    > El Firewall se debe volver a habilitar después de completar este paso.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Comprobando que la excepción de detección de redes está habilitada

Si se están ejecutando aplicaciones WS-Discovery, se debe permitir la excepción de Firewall de **detección de redes** .

**Para habilitar la excepción de Firewall de detección de redes**

1.  Haga clic en **Inicio**, haga clic en **Ejecutar** y, a continuación, escriba **firewall.cpl**. Se abrirá el applet **Panel de control del firewall de Windows** .
2.  Elija **permitir un programa a través de Firewall de Windows**.
3.  En la pestaña **excepciones** , active la casilla **detección de redes** .
4.  Haga clic en **Aceptar** para cerrar el applet de Firewall.

Pruebe a probar el programa después de cambiar este firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos para la solución de problemas. En caso contrario, vaya al paso siguiente.

## <a name="checking-for-application-specific-firewall-rules"></a>Comprobando las reglas de Firewall específicas de la aplicación

La configuración avanzada del firewall de Windows puede tener lugar en un complemento de Microsoft Management Control (MMC) denominado **firewall de Windows con seguridad avanzada**. Este complemento se puede usar para solucionar problemas de Firewall sospechosos.

Los desarrolladores pueden usar las API de [firewall de Windows con seguridad avanzada](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) para crear reglas de firewall que se aplican a sus aplicaciones WSD. En concreto, el método [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) de la interfaz [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) se puede usar para agregar una nueva regla de Firewall. Si las reglas de Firewall se crean de forma incorrecta, es posible que los clientes y los hosts no se puedan ver entre sí en la red.

**Para comprobar las reglas de Firewall específicas de la aplicación**

1.  Haga clic en **Inicio**, haga clic en **Ejecutar** y, a continuación, escriba **WF. msc**.
2.  Busque reglas específicas de la aplicación que puedan estar bloqueando el tráfico. Para obtener más información, consulte [firewall de Windows con seguridad avanzada: herramientas de diagnóstico y solución de problemas](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Quite las reglas específicas de la aplicación.

Si no se encuentra ninguna regla específica de la aplicación, vaya al paso siguiente. Si se ha encontrado y quitado una regla específica de la aplicación, pruebe a probar el programa después de cambiar el firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos para la solución de problemas. En caso contrario, vaya al paso siguiente.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Habilitación de los puertos utilizados para la detección y el intercambio de metadatos

WS-Discovery usa el puerto UDP 3702 para el intercambio de mensajes. Además, los puertos TCP 5357 y 5358 a veces se usan para el intercambio de metadatos. Estos puertos se pueden abrir explícitamente en el Firewall mediante los procedimientos descritos en [abrir un puerto en firewall de Windows](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).

Pruebe a probar el programa después de cambiar este firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos para la solución de problemas. En caso contrario, vaya al paso siguiente.

## <a name="disabling-the-firewall"></a>Deshabilitar el Firewall

El Firewall de Windows se puede deshabilitar para ayudar a solucionar problemas sospechosos. Otros firewalls aplicables (como el Firewall de un enrutador) también se pueden deshabilitar para solucionar problemas. Para obtener información acerca de cómo habilitar y deshabilitar el Firewall de Windows, consulte [activar o desactivar Firewall de Windows](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx).

Pruebe de nuevamente la aplicación después de deshabilitar los firewalls aplicables. Si el programa funciona ahora correctamente, el Firewall estaba bloqueando el tráfico. Hay algunas causas posibles del tráfico bloqueado.

-   Las excepciones específicas de la aplicación bloquean el tráfico. Compruebe las reglas de Firewall específicas de la aplicación como se ha descrito anteriormente.
-   El dispositivo tardó demasiado tiempo en responder a las solicitudes UDP. El Firewall de Windows puede bloquear las respuestas UDP que devuelven más de 4 segundos después de que se enviara la solicitud inicial. Siga los procedimientos que se indican en [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) para ver si el problema se reproduce con un host que responde en menos de 4 segundos.

Si se produce un error en la aplicación después de que el Firewall esté deshabilitado, el Firewall no provocará el error de aplicación. Vuelva a habilitar los firewalls y siga los pasos que se indican en uso de [un host y cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Los firewalls siempre se deben volver a habilitar después de que haya finalizado la solución de problemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
