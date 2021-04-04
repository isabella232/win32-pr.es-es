---
title: Habilitación del seguimiento de EAPHost
description: Puede ayudar a los usuarios a encontrar las causas raíz de los problemas que se producen durante el proceso de autenticación de EAP. La información de depuración puede incluir llamadas API realizadas, llamadas a funciones internas realizadas y transiciones de estado realizadas.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104078644"
---
# <a name="enabling-eaphost-tracing"></a>Habilitación del seguimiento de EAPHost

Los registros de seguimiento que contienen información de depuración pueden ayudar a los usuarios a encontrar las causas raíz de los problemas que se producen durante el proceso de autenticación de EAP. La información de depuración puede incluir llamadas API realizadas, llamadas a funciones internas realizadas y transiciones de estado realizadas.

El seguimiento se puede habilitar tanto en el lado cliente como en el lado autenticador. También se puede habilitar el seguimiento para las llamadas a las API del [servicio de enrutamiento y acceso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page) . Para obtener más información, vea [seguimiento en el servicio de enrutamiento y acceso remoto](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> Los registros de seguimiento solo están disponibles en inglés.

 

Cuando el seguimiento de EAPHost está habilitado, la información de registro se almacena en un archivo. ETL en una ubicación especificada por el usuario. Si se producen errores durante la autenticación de EAP, el seguimiento genera un archivo. ETL que se puede enviar a Microsoft soporte técnico Developer para el análisis de la causa raíz. Los asociados que tienen acceso a recursos compartidos de compilación de Microsoft Windows, símbolos y archivos traceformat pueden convertir los archivos. ETL en un archivo de texto sin formato mediante la herramienta **tracerpt** .

Los errores del servidor de directivas de redes (NPS) no se capturan en los registros de EAPHost. Si está intentando solucionar un error de NPS, vea el IASSAM. LOG y [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) Archivos de registro.

## <a name="tracing-on-the-client"></a>Seguimiento en el cliente

Para habilitar el seguimiento en el lado cliente:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **Logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. ETL** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**
3.  Reproduzca el escenario del que desea realizar un seguimiento.
4.  Ejecute el siguiente comando: **Logman** **Stop** **EapHostPeer** **-ETS**
5.  Convierta el archivo ETL en texto con el siguiente comando **: tracerpt EapHostPeer. ETL** **– PDB** **&lt; &gt; pdbpath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Si no tiene acceso a la herramienta tracerpt, evite el último paso y envíe el archivo. ETL a Microsoft soporte técnico Developer.

     

## <a name="tracing-on-the-authenticator"></a>Seguimiento en el autenticador

Para habilitar el seguimiento en el lado del autenticador:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **Logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. ETL** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**
3.  Reproduzca el escenario del que desea realizar un seguimiento.
4.  Ejecute el siguiente comando: **Logman** **Stop** **EapHostAuthr** **-ETS**
5.  Convierta el archivo ETL en texto con el siguiente comando **: tracerpt EapHostAuthr. ETL** **– PDB** **&lt; &gt; pdbpath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Si no tiene acceso a la herramienta tracerpt, evite el último paso y, en su lugar, envíe el archivo. ETL a Microsoft soporte técnico Developer.

     

## <a name="event-tracing"></a>Seguimiento de eventos

En Windows 7 y versiones posteriores de Windows, EapHost proporciona seguimiento basado en eventos en el autenticador y en el mismo nivel. La ventaja del seguimiento basado en eventos es que no se necesitan archivos de símbolos para ver los mensajes de seguimiento. Para habilitar el seguimiento de eventos:

1.  Abra **EventViewer**.
2.  Los mensajes críticos de EapHost se registran en: "Custom views \\ Administrative Events"
3.  Los mensajes no críticos se registran en: "aplicaciones y servicios \\ Microsoft \\ Windows \\ EAPHost
4.  Los mensajes de eventos de tipo "análisis" y "depuración" se pueden ver en la misma ruta de acceso; para ello, seleccione **Mostrar registros analíticos y de depuración** en el menú **Ver** de la barra de título.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Seguimiento en el servicio de enrutamiento y acceso remoto

Para habilitar el seguimiento de RRAS:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **netsh** **ras** **set** **TR** **\* *_ _* en**
3.  Abrir el **\\ seguimiento de% SystemRoot%** para ver los SEGUIMIENTOs de Ras

Para deshabilitar el seguimiento de RRAS:

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **netsh** **ras** **set** **TR** **\* *_ _* dis**

Para obtener más información, vea [comandos Netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> <dt>

[Servicio de enrutamiento y acceso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 