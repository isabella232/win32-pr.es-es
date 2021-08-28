---
title: Habilitación del seguimiento de EAPHost
description: Puede ayudar a los usuarios a encontrar las causas principales de los problemas que se producen durante el proceso de autenticación eap. La información de depuración puede incluir las llamadas API realizadas, las llamadas a funciones internas realizadas y las transiciones de estado realizadas.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c638fa7f546028cd9cf66227cfe3c302d6599492d1cbbfcfdac6c2b428273db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086297"
---
# <a name="enabling-eaphost-tracing"></a>Habilitación del seguimiento de EAPHost

Los registros de seguimiento que contienen información de depuración pueden ayudar a los usuarios a encontrar las causas principales de los problemas que se producen durante el proceso de autenticación eap. La información de depuración puede incluir las llamadas API realizadas, las llamadas a funciones internas realizadas y las transiciones de estado realizadas.

El seguimiento se puede habilitar tanto en el lado cliente como en el lado autenticador. El seguimiento también se puede habilitar para las llamadas a las API del Servicio de enrutamiento y acceso remoto [(RRAS).](/windows/desktop/RRAS/routing-start-page) Para obtener más información, vea [Seguimiento en el servicio de enrutamiento y acceso remoto.](#tracing-on-the-routing-and-remote-access-service)

> [!Note]  
> Los registros de seguimiento solo están disponibles en inglés.

 

Cuando el seguimiento de EAPHost está habilitado, la información de registro se almacena en un archivo .etl en una ubicación especificada por el usuario. Si se producen errores durante la autenticación eap, el seguimiento genera un archivo .etl que se puede enviar a Desarrollador de Microsoft compatibilidad con el análisis de la causa principal. Los asociados que tienen acceso a recursos compartidos de compilación, símbolos y archivos de formato de seguimiento de Microsoft Windows pueden convertir los archivos .etl en un archivo de texto sin formato mediante la **herramienta tracerpt.**

Los errores del servidor de directivas de red (NPS) no se capturan en los registros de EAPHost. Si está intentando solucionar un error de NPS, vea el ITENTARLOM. LOG e [IASNAP. Archivos LOG.](https://go.microsoft.com/fwlink/p/?linkid=84108)

## <a name="tracing-on-the-client"></a>Seguimiento en el cliente

Para habilitar el seguimiento en el lado cliente:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **logman** **start trace** **EapHostPeer** **-o** **. \\ EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**
3.  Reproduzca el escenario del que desea hacer un seguimiento.
4.  Ejecute el siguiente comando: **logman** **stop** **EapHostPeer** **-ets**
5.  Convierta el archivo etl en texto mediante el siguiente comando: **tracerpt EapHostPeer.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Si no tiene acceso a la herramienta tracerpt, evite el último paso y envíe el archivo .etl a Desarrollador de Microsoft soporte técnico.

     

## <a name="tracing-on-the-authenticator"></a>Seguimiento en el Authenticator

Para habilitar el seguimiento en el lado autenticador:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **logman** **start trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**
3.  Reproduzca el escenario del que desea hacer un seguimiento.
4.  Ejecute el siguiente comando: **logman** **stop** **EapHostAuthr** **-ets**
5.  Convierta el archivo etl en texto mediante el siguiente comando: **tracerpt EapHostAuthr.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Si no tiene acceso a la herramienta tracerpt, evite el último paso y, en su lugar, envíe el archivo .etl a Desarrollador de Microsoft Soporte técnico.

     

## <a name="event-tracing"></a>Seguimiento de eventos

En Windows 7 y versiones posteriores de Windows, EapHost proporciona seguimiento basado en eventos en el autenticador y el elemento del mismo nivel. La ventaja del seguimiento basado en eventos es que no se necesitan archivos de símbolos para ver los mensajes de seguimiento. Para habilitar el seguimiento de eventos:

1.  Abra **EventViewer.**
2.  Los mensajes críticos de EapHost se registran en: "Eventos administrativos \\ de vistas personalizadas"
3.  Los mensajes no críticos se registran en: "Aplicaciones y servicios \\ de Microsoft \\ Windows \\ EapHost
4.  Los mensajes de evento de tipo "Analítico" y "Depurar"  se pueden ver en la  misma ruta de acceso seleccionando Mostrar registros analíticos y de depuración en el menú de vista de la barra de título.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Seguimiento en el servicio de enrutamiento y acceso remoto

Para habilitar el seguimiento de RRAS:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **netsh** **ras** **set** **tr** _ **\* *_* en**
3.  Abra **el seguimiento %systemroot% \\ para** ver los seguimientos ras.

Para deshabilitar el seguimiento de RRAS:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **netsh** **ras** **set** **tr** _ **\* *_* dis**

Para obtener más información, [vea Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[Servicio de enrutamiento y acceso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 