---
title: Configuración de una suscripción iniciada por origen
description: Las suscripciones iniciadas por el origen permiten definir una suscripción en un equipo del recopilador de eventos sin definir los equipos de origen de eventos y, a continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: f9d0ade037c0332f390bbea4c9f126f78f4172879fc50465fcf9e329e89fa23d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620655"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configuración de una suscripción iniciada por origen

Las suscripciones iniciadas por el origen permiten definir una suscripción en un equipo del recopilador de eventos sin definir los equipos de origen de eventos y, a continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos. Esto difiere de una suscripción iniciada por el recopilador porque, en el modelo de suscripción iniciada por el recopilador, el recopilador de eventos debe definir todos los orígenes de eventos de la suscripción de eventos.

Al configurar una suscripción iniciada por el origen, tenga en cuenta si los equipos de origen de eventos están en el mismo dominio que el equipo del recopilador de eventos. En las secciones siguientes se describen los pasos que deben seguirse cuando los orígenes de eventos están en el mismo dominio o no en el mismo dominio que el equipo del recopilador de eventos.

> [!Note]  
> Cualquier equipo de un dominio, local o remoto, puede ser un recopilador de eventos. Sin embargo, al elegir un recopilador de eventos, es importante seleccionar una máquina que esté topológicamente cerca de donde se generará la mayoría de los eventos. El envío de eventos a una máquina en una ubicación de red lejana en una WAN puede reducir el rendimiento general y la eficacia en la recopilación de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos se encuentran en el mismo dominio que el equipo del recopilador de eventos

Tanto los equipos de origen de eventos como el equipo del recopilador de eventos deben configurarse para configurar una suscripción iniciada por el origen.

> [!Note]  
> En estas instrucciones se supone que tiene acceso de administrador al controlador de dominio de Windows Server que atiende al dominio en el que el equipo remoto o los equipos se configurarán para recopilar eventos.

### <a name="configuring-the-event-source-computer"></a>Configuración del equipo de origen del evento

1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Windows administración remota:

    **winrm qc -q**

2. Ejecute el siguiente comando para iniciar la directiva de grupo:

    **%SYSTEMROOT% \\ System32 \\ gpedit.msc**

3. En el **nodo Configuración del** equipo, expanda el nodo **Plantillas administrativas,** expanda el nodo Componentes Windows **y,** a continuación, seleccione el nodo **Reenvío de** eventos.

4. Haga clic con el botón derecho **en la configuración SubscriptionManager** y seleccione **Propiedades.** Habilite la **opción SubscriptionManager** y haga clic en **el botón Mostrar** para agregar una dirección de servidor a la configuración. Agregue al menos una configuración que especifique el equipo del recopilador de eventos. La **ventana Propiedades de SubscriptionManager** contiene una pestaña **Explicar** que describe la sintaxis de la configuración.

5. Una vez agregada la configuración de **SubscriptionManager,** ejecute el siguiente comando para asegurarse de que se aplica la directiva:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configuración del equipo del recopilador de eventos

1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Windows administración remota:

    **winrm qc -q**

2. Ejecute el siguiente comando para configurar el servicio Recopilador de eventos:

    **wecutil qc /q**

3. Cree una suscripción iniciada por el origen. Esto se puede hacer mediante programación, mediante el Visor de eventos o mediante [**Wecutil.exe**](wecutil.md). Para obtener más información sobre cómo crear la suscripción mediante programación, vea el ejemplo de código en [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md). Si usa Wecutil.exe, debe crear un archivo XML de suscripción de eventos y usar el comando siguiente:

    **wecutil cs** *configurationFile.xml*

    El siguiente XML es un ejemplo del contenido de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos desde el registro de eventos de aplicación de un equipo remoto al registro ForwardedEvents en el equipo del recopilador de eventos.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > Al crear una suscripción iniciada por el origen, si AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList y DeniedSubjectList están vacíos, "O:NSG:NSD:(A;; GA;;;D C)(A;; GA;;; NS)" se usará como descriptor de seguridad predeterminado para AllowedSourceDomainComputers. El descriptor predeterminado concede a los miembros del grupo de dominio Equipos de dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Para validar que la suscripción funciona correctamente

1. En el equipo del recopilador de eventos, realice los pasos siguientes:

    1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para obtener el estado de tiempo de ejecución de la suscripción:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Compruebe que el origen del evento se ha conectado. Es posible que tenga que esperar hasta que el intervalo de actualización especificado en la directiva haya terminado después de crear la suscripción para que se conecte el origen del evento.
    3. Ejecute el siguiente comando para obtener la información de la suscripción:

        **wecutil gs** *&lt; subscriptionID &gt;*

    4. Obtenga el valor DeliveryMaxItems de la información de la suscripción.

2. En el equipo de origen del evento, genera los eventos que coinciden con la consulta de la suscripción de eventos. Se debe generar el número de eventos DeliveryMaxItems para que los eventos se reenván.
3. En el equipo del recopilador de eventos, compruebe que los eventos se han reenviado al registro ForwardedEvents o al registro especificado en la suscripción.

## <a name="forwarding-the-security-log"></a>Reenvío del registro de seguridad

Para poder reenviar el registro de seguridad, debe agregar la cuenta DE SERVICIO DE RED al grupo Lectores de EventLog.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos no están en el mismo dominio que el equipo del recopilador de eventos

> [!Note]  
> En estas instrucciones se supone que tiene acceso de administrador a un controlador de dominio Windows Server. En este caso, dado que los equipos o equipos del recopilador de eventos remotos no están en el dominio al que sirve el controlador de dominio, es esencial iniciar un cliente individual estableciendo Windows Remote Management en "automatic" mediante Services (services.msc). Como alternativa, puede ejecutar "winrm quickconfig" en cada cliente remoto.

Se deben cumplir los siguientes requisitos previos antes de crear la suscripción.

1. En el equipo del recopilador de eventos, ejecute los siguientes comandos desde un símbolo del sistema con privilegios elevados para configurar Windows administración remota y el servicio Recopilador de eventos:

    **winrm qc -q**

    **wecutil qc /q**

2. El equipo recopilador debe tener un certificado de autenticación de servidor (certificado con un propósito de autenticación de servidor) en un almacén de certificados de equipo local.
3. En el equipo de origen del evento, ejecute el siguiente comando para configurar la Windows remota:

    **winrm qc -q**

4. La máquina de origen debe tener un certificado de autenticación de cliente (certificado con un propósito de autenticación de cliente) en un almacén de certificados de equipo local.
5. El puerto 5986 se abre en el equipo del recopilador de eventos. Para abrir este puerto, ejecute el comando :

    **netsh firewall add que permite usar TCP 5986 "Winrm HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisitos de certificados

- Debe instalarse un certificado de autenticación de servidor en el equipo del recopilador de eventos en el almacén personal de la máquina local. El firmante de este certificado debe coincidir con el FQDN del recopilador.
- Un certificado de autenticación de cliente debe instalarse en los equipos de origen de eventos en el almacén personal de la máquina local. El firmante de este certificado debe coincidir con el FQDN del equipo.
- Si el certificado de cliente lo ha emitido una entidad de certificación diferente a la del recopilador de eventos, esos certificados raíz e intermedio también deben instalarse en el recopilador de eventos.
- Si el certificado de cliente lo emitió una entidad de certificación intermedia y el recopilador se ejecuta Windows 2012 o posterior, tendrá que configurar la siguiente clave del Registro:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Compruebe que el servidor y el cliente pueden comprobar correctamente el estado de revocación en todos los certificados. El uso del **comando certutil** puede ayudar a solucionar los errores.

Encuentre más información en este artículo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configuración del agente de escucha en el recopilador de eventos

1. Establezca la autenticación de certificado con el siguiente comando:

    **winrm set winrm/config/service/auth @{Certificate="true"}**

2. Debe existir un agente de escucha HTTPS de WinRM con la huella digital del certificado de autenticación del servidor en el equipo del recopilador de eventos. Esto se puede comprobar con el siguiente comando:

    **winrm e winrm/config/listener**

3. Si no ve el agente de escucha HTTPS, o si la huella digital del agente de escucha HTTPS no es la misma que la huella digital del certificado de autenticación del servidor en el equipo recopilador, puede eliminar ese agente de escucha y crear uno con la huella digital correcta. Para eliminar el agente de escucha https, use el siguiente comando:

    **winrm delete winrm/config/Listener? Address=*+Transport=HTTPS**

    Para crear un nuevo agente de escucha, use el siguiente comando:

    **winrm create winrm/config/Listener? Address=&#42;+Transport=HTTPS @{Hostname="** &lt; _FQDN del recopilador_ &gt; **"; CertificateThumbprint="** &lt; _Huella digital del certificado de autenticación del servidor_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configuración de la asignación de certificados en el recopilador de eventos

1. Cree un nuevo usuario local y agrégrélo al grupo administradores local.
2. Cree la asignación de certificados mediante un certificado que esté presente en la "entidades de certificación raíz de confianza" o "Entidades de certificación intermedias" de la máquina.

    Este es el certificado de la ENTIDAD de certificación raíz o intermedia que emitió los certificados instalados en los equipos de origen de eventos (para evitar confusiones, esta es la CA inmediatamente por encima del certificado en la cadena de *certificados):*

    **winrm create winrm/config/service/certmapping? Huella digital** del emisor del certificado de ca emisora = &lt;  &gt; **+Subject=&#42;+URI=&#42; nombre de usuario @{UserName="** &lt;  &gt; **"; Password="** &lt; _password_ &gt; **"} -remote:localhost**

3. Desde un cliente, pruebe el agente de escucha y la asignación de certificados con el siguiente comando:

    **winrm g winrm/config -r:https://** &lt; _FQDN del recopilador de eventos_ &gt; **:5986 -a:certificate -certificate:"** &lt; _Huella digital del certificado de autenticación de cliente_ &gt; **"**

    Esto debe devolver la configuración de WinRM del recopilador de eventos. **No pase** este paso si no se muestra la configuración.

    **¿Qué ocurre en este paso?**
    - El cliente se conecta al recopilador de eventos y envía el certificado especificado.
    - El recopilador de eventos busca la CA emisora y comprueba si es una asignación de certificado correspondiente.
    - El recopilador de eventos valida la cadena de certificados de cliente y el estado de revocaciones.
    - Si los pasos anteriores se completan correctamente, se completa la autenticación.

> [!NOTE]
> Es posible que reciba un error de acceso denegado que se queje del método de autenticación, lo que podría ser engañoso. Para solucionar problemas, compruebe el registro capi en el recopilador de eventos.

4. Enume las entradas de certmapping configuradas con el comando: **winrm enum winrm/config/service/certmapping**

### <a name="event-source-computer-configuration"></a>Configuración del equipo de origen de eventos

1. Inicie sesión con una cuenta de administrador y abra Editor de directivas de grupo local (gpedit.msc)
2. Vaya a Directiva de equipo local\Configuración del equipo\Plantillas administrativas\Windows Componentes\Reenvío de eventos.
3. Abra la directiva "Configurar la dirección del servidor, el intervalo de actualización y la entidad de certificación del emisor de un administrador de suscripciones de destino".
4. Habilite la directiva y haga clic en subscriptionManagers "Mostrar...". Botón.
5. En la ventana SubscriptionManagers, escriba la cadena siguiente:

    **Server=HTTPS://** &lt; _FQDN del servidor del recopilador de eventos_ &gt; **:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt; _Intervalo de actualización en segundos_ &gt; **,IssuerCA=** &lt; _Huella digital del certificado de entidad de certificación emisora_&gt;

6. Ejecute la siguiente línea de comandos para actualizar la configuración directiva de grupo local:Gpupdate /force
7. Estos pasos deben generar el evento 104 en el equipo de origen Visor de eventos Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log con el mensaje siguiente:

    "El reenviador se ha conectado correctamente al administrador de suscripciones en el FQDN de la dirección seguido del evento 100 con el mensaje: "La suscripción sub_name se ha creado &lt; &gt; &lt; &gt; correctamente".

8. En el Recopilador de eventos, el estado de tiempo de ejecución de la suscripción mostrará ahora 1 equipo activo.
9. Abra el registro ForwardedEvents en el recopilador de eventos y compruebe si tiene los eventos reenviados desde los equipos de origen.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Conceder permiso en la clave privada del certificado de cliente en el origen de eventos

1. Abra la consola de administración de certificados para Equipo local en el equipo de origen de eventos.
2. Haga clic con el botón derecho en el certificado de cliente y, a continuación, en Administrar claves privadas.
3. Conceda permiso de lectura al usuario NETWORK SERVICE.

### <a name="event-subscription-configuration"></a>Configuración de suscripción de eventos

1. Abra Visor de eventos en el Recopilador de eventos y vaya al nodo Suscripciones.
2. Haga clic con el botón derecho en Suscripciones y elija "Crear suscripción..."
3. Asigne un nombre y una descripción opcional para la nueva suscripción.
4. Seleccione la opción "Equipo de origen iniciado" y haga clic en "Seleccionar grupos de equipos...".
5. En Grupos de equipos, haga clic en "Agregar equipos que no son de dominio...". y escriba el nombre de host del origen del evento.
6. Haga clic en "Agregar certificados...". y agregue el certificado de la entidad de certificación que emite los certificados de cliente. Puede hacer clic en Ver certificado para validar el certificado.
7. En Certificate Authorities (Autoridades de certificados), haga clic en Ok (Aceptar) para agregar el certificado.
8. Cuando termine de agregar Equipos, haga clic en Aceptar.
9. Vuelva a las propiedades de suscripción, haga clic en Seleccionar eventos...
10. Configure el filtro de consulta de eventos especificando los niveles de evento, los registros de eventos o los orígenes de eventos, los identificadores de evento y cualquier otra opción de filtrado.
11. Vuelva a las propiedades de la suscripción, haga clic en Avanzadas...
12. Elija una de las opciones de optimización para la entrega de eventos del evento de origen al recopilador de eventos o deje el valor predeterminado Normal: 
    1. **Minimizar el ancho de** banda: los eventos se entregarán con menos frecuencia para ahorrar ancho de banda.
    2. **Minimizar la latencia:** los eventos se entregarán en cuanto se produzcan para reducir la latencia de los eventos.
13. Cambie protocolo a HTTPS y haga clic en Aceptar.
14. Haga clic en Aceptar para crear la nueva suscripción.
15. Para comprobar el estado de tiempo de ejecución de la suscripción, haga clic con el botón derecho y elija "Estado de tiempo de ejecución".
