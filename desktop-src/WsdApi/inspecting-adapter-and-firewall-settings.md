---
description: Un firewall mal configurado puede provocar un error en las aplicaciones WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Inspección del adaptador y el firewall Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ea14051ac65dbd0b749fa00566afc9ed82e5571f6027dafa003e12013888b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130787"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Inspección del adaptador y el firewall Configuración

Un firewall mal configurado puede provocar un error en las aplicaciones WSD. En este tema se proporcionan algunos procedimientos de solución de problemas que se usan cuando los clientes y hosts de WSD no se pueden ver entre sí en la red. La configuración del firewall debe inspeccionarse antes de usar cualquier otro procedimiento de solución de problemas de aplicaciones.

**Para inspeccionar la configuración del adaptador y el firewall**

1.  Compruebe que la **excepción de detección** de redes está habilitada.
2.  Compruebe que no hay ninguna regla de firewall específica de la aplicación que bloquee la aplicación.
3.  Habilite explícitamente los puertos utilizados para la detección y el intercambio de metadatos.
4.  Deshabilite el firewall y vuelva a probar la aplicación.
    > [!Note]  
    > El firewall debe volver a habilitarse después de completar este paso.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Comprobación de que la excepción de detección de redes está habilitada

Si hay WS-Discovery aplicaciones en ejecución, se debe permitir la **excepción** de firewall de detección de redes.

**Para habilitar la excepción de firewall de detección de redes**

1.  Haga clic **en Inicio**, haga clic **en Ejecutar** y, a continuación, **escribafirewall.cpl**. Se abre el **applet Windows Firewall Panel de control.**
2.  Elija **Permitir un programa a través de Windows Firewall.**
3.  En la **pestaña Excepciones,** active la casilla **Detección de** redes.
4.  Haga **clic en** Aceptar para cerrar el applet del firewall.

Vuelva a probar el programa después de realizar este cambio de firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos de solución de problemas. De lo contrario, pase al paso siguiente.

## <a name="checking-for-application-specific-firewall-rules"></a>Comprobación de reglas de firewall específicas de la aplicación

La configuración avanzada del firewall Windows puede tener lugar en un complemento de Control de administración de Microsoft (MMC) denominado **Windows Firewall con seguridad avanzada**. Este complemento se puede usar para solucionar problemas sospechosos de firewall.

Los desarrolladores pueden usar [Windows Firewall con](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) API de seguridad avanzada para crear reglas de firewall que se apliquen a sus aplicaciones WSD. En concreto, el [**método Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) de la [**interfaz INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) se puede usar para agregar una nueva regla de firewall. Si las reglas de firewall se crean incorrectamente, es posible que los clientes y hosts no puedan verse entre sí en la red.

**Para comprobar si hay reglas de firewall específicas de la aplicación**

1.  Haga clic **en Inicio**, haga clic **en Ejecutar** y, a continuación, **escriba wf.msc**.
2.  Busque reglas específicas de la aplicación que puedan estar bloqueando el tráfico. Para obtener más información, [vea Windows Firewall con seguridad avanzada- Herramientas de diagnóstico y solución de problemas](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Quite las reglas específicas de la aplicación.

Si no se encontraron reglas específicas de la aplicación, pase al paso siguiente. Si se ha encontrado y quitado una regla específica de la aplicación, vuelva a probar el programa después de realizar el cambio del firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos de solución de problemas. De lo contrario, pase al paso siguiente.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Habilitación de los puertos usados para la detección y el intercambio de metadatos

WS-Discovery usa el puerto UDP 3702 para el intercambio de mensajes. Además, los puertos TCP 5357 y 5358 se usan a veces para el intercambio de metadatos. Estos puertos se pueden abrir explícitamente en el firewall mediante los procedimientos descritos en Abrir un [puerto en Windows Firewall](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).

Vuelva a probar el programa después de realizar este cambio de firewall. Si el programa funciona ahora correctamente, se ha identificado la causa del problema y no es necesario realizar más pasos de solución de problemas. De lo contrario, pase al paso siguiente.

## <a name="disabling-the-firewall"></a>Deshabilitación del firewall

El Windows firewall se puede deshabilitar para ayudar a solucionar problemas sospechosos. Otros firewalls aplicables (como el firewall en un enrutador) también se pueden deshabilitar para solucionar problemas. Para obtener información sobre cómo habilitar y deshabilitar el firewall de Windows, vea Activar o desactivar [Windows firewall.](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)

Vuelva a probar la aplicación después de deshabilitar los firewalls aplicables. Si el programa funciona ahora correctamente, el firewall estaba bloqueando el tráfico. Hay algunas causas posibles del tráfico bloqueado.

-   Las excepciones específicas de la aplicación bloquearon el tráfico. Compruebe las reglas de firewall específicas de la aplicación como se describió anteriormente.
-   El dispositivo tardó demasiado tiempo en responder a las solicitudes UDP. El Windows firewall puede bloquear las respuestas UDP que devuelven más de 4 segundos después de enviar la solicitud inicial. Siga los procedimientos descritos en Uso de un host y un cliente genéricos para la detección de [WS de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) para ver si el problema se reproduce con un host que responde en menos de 4 segundos.

Si la aplicación sigue generando un error después de deshabilitar el firewall, el firewall no está causando el error de la aplicación. Vuelva a habilitar los firewalls y continúe con la solución de problemas siguiendo los procedimientos descritos en Using [a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Los firewalls siempre deben volver a habilitarse una vez finalizada la solución de problemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
