---
title: Configuración de una suscripción iniciada por el origen
description: Las suscripciones iniciadas por el origen permiten definir una suscripción en un equipo del recopilador de eventos sin definir los equipos de origen del evento y, a continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/04/2020
ms.locfileid: "104420513"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configuración de una suscripción iniciada por el origen

Las suscripciones iniciadas por el origen permiten definir una suscripción en un equipo del recopilador de eventos sin definir los equipos de origen del evento y, a continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos. Esto difiere de una suscripción iniciada por el recopilador porque en el modelo de suscripción Iniciado por el recopilador, el recopilador de eventos debe definir todos los orígenes de eventos de la suscripción de eventos.

Al configurar una suscripción iniciada por el origen, considere si los equipos de origen de eventos están en el mismo dominio que el equipo del recopilador de eventos. En las secciones siguientes se describen los pasos que se deben seguir cuando los orígenes de eventos están en el mismo dominio o no en el mismo dominio que el equipo del recopilador de eventos.

> [!Note]  
> Cualquier equipo de un dominio, local o remoto, puede ser un recopilador de eventos. Sin embargo, al elegir un recopilador de eventos, es importante seleccionar una máquina topológicamente cercana a la ubicación en la que se generará la mayoría de los eventos. El envío de eventos a un equipo en una ubicación de red lejana en una WAN puede reducir el rendimiento general y la eficacia de la recopilación de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos están en el mismo dominio que el equipo del recopilador de eventos

Tanto los equipos de origen de eventos como el equipo del recopilador de eventos deben estar configurados para configurar una suscripción iniciada por el origen.

> [!Note]  
> En estas instrucciones se da por hecho que tiene acceso de administrador al controlador de dominio de Windows Server que atiende al dominio en el que se configurarán los equipos remotos para recopilar eventos.

### <a name="configuring-the-event-source-computer"></a>Configuración del equipo de origen de eventos

1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Administración remota de Windows:

    **WinRM QC-q**

2. Inicie la Directiva de grupo mediante la ejecución del siguiente comando:

    **% SYSTEMROOT% \\ system32 \\ gpedit. msc**

3. En el **nodo configuración del equipo** , expanda el nodo **plantillas administrativas** , expanda el nodo **componentes de Windows** y, a continuación, seleccione el nodo **reenvío de eventos** .

4. Haga clic con el botón secundario en el valor **SubscriptionManager** y seleccione **propiedades**. Habilite la opción **SubscriptionManager** y haga clic en el botón **Mostrar** para agregar una dirección de servidor a la configuración. Agregue al menos un valor de configuración que especifique el equipo del recopilador de eventos. La ventana **propiedades de SubscriptionManager** contiene una pestaña **explicativa** que describe la sintaxis de la configuración.

5. Una vez agregada la configuración **SubscriptionManager** , ejecute el siguiente comando para asegurarse de que se aplica la Directiva:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configuración del equipo del recopilador de eventos

1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Administración remota de Windows:

    **WinRM QC-q**

2. Ejecute el siguiente comando para configurar el servicio Recopilador de eventos:

    **wecutil QC/q**

3. Cree una suscripción iniciada por el origen. Esto puede realizarse mediante programación, mediante el Visor de eventos o mediante [**Wecutil.exe**](wecutil.md). Para obtener más información sobre cómo crear la suscripción mediante programación, vea el ejemplo de código de [creación de una suscripción iniciada](creating-a-source-initiated-subscription.md)por el origen. Si usa Wecutil.exe, debe crear un archivo XML de suscripción de eventos y usar el siguiente comando:

    **wecutil cs** *configurationFile.xml*

    El siguiente código XML es un ejemplo del contenido de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos desde el registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados en el equipo del recopilador de eventos.

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
    > Al crear una suscripción iniciada por el origen, si AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList y DeniedSubjectList están todos vacíos, entonces "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "se usará como descriptor de seguridad predeterminado para AllowedSourceDomainComputers. El descriptor predeterminado concede a los miembros del grupo de dominio equipos del dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Para validar que la suscripción funciona correctamente

1. En el equipo del recopilador de eventos, realice los pasos siguientes:

    1. Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para obtener el estado de tiempo de ejecución de la suscripción:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Compruebe que el origen del evento se ha conectado. Es posible que tenga que esperar hasta que se haya creado el intervalo de actualización especificado en la Directiva después de crear la suscripción para que el origen del evento se conecte.
    3. Ejecute el siguiente comando para obtener la información de la suscripción:

        **wecutil GS** *&lt; subscriptionID &gt;*

    4. Obtiene el valor de DeliveryMaxItems de la información de suscripción.

2. En el equipo de origen del evento, genere los eventos que coinciden con la consulta de la suscripción de eventos. Se debe generar el número de eventos DeliveryMaxItems para que se reenvíen los eventos.
3. En el equipo del recopilador de eventos, compruebe que los eventos se han reenviado al registro Eventos reenviados o al registro especificado en la suscripción.

## <a name="forwarding-the-security-log"></a>Reenvío del registro de seguridad

Para poder reenviar el registro de seguridad, debe agregar la cuenta de servicio de red al grupo lectores del registro de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos no están en el mismo dominio que el equipo del recopilador de eventos

> [!Note]  
> En estas instrucciones se da por hecho que tiene acceso de administrador a un controlador de dominio de Windows Server. En este caso, dado que el equipo o equipos del recopilador de eventos remotos no están en el dominio atendido por el controlador de dominio, es esencial iniciar un cliente individual estableciendo Administración remota de Windows en "automático" mediante servicios (Services. msc). Como alternativa, puede ejecutar "WinRM quickconfig" en cada cliente remoto.

Antes de crear la suscripción, deben cumplirse los siguientes requisitos previos.

1. En el equipo del recopilador de eventos, ejecute los siguientes comandos desde un símbolo del sistema con privilegios elevados para configurar Administración remota de Windows y el servicio Recopilador de eventos:

    **WinRM QC-q**

    **wecutil QC/q**

2. El equipo del recopilador debe tener un certificado de autenticación de servidor (certificado con un propósito de autenticación de servidor) en un almacén de certificados del equipo local.
3. En el equipo de origen del evento, ejecute el siguiente comando para configurar Administración remota de Windows:

    **WinRM QC-q**

4. El equipo de origen debe tener un certificado de autenticación del cliente (certificado con un propósito de autenticación del cliente) en un almacén de certificados del equipo local.
5. El puerto 5986 está abierto en el equipo del recopilador de eventos. Para abrir este puerto, ejecute el comando:

    **netsh firewall Add portopening TCP 5986 "WinRM HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisitos de certificados

- Se debe instalar un certificado de autenticación de servidor en el equipo del recopilador de eventos del almacén personal del equipo local. El sujeto de este certificado debe coincidir con el FQDN del recopilador.
- Es necesario instalar un certificado de autenticación del cliente en los equipos de origen del evento en el almacén personal del equipo local. El sujeto de este certificado debe coincidir con el FQDN del equipo.
- Si el certificado de cliente ha sido emitido por una entidad de certificación distinta de la del recopilador de eventos, esos certificados raíz e intermedio deben instalarse también en el recopilador de eventos.
- Si el certificado de cliente lo emitió una entidad de certificación intermedia y el recopilador ejecuta Windows 2012 o una versión posterior, tendrá que configurar la siguiente clave del registro:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Compruebe que tanto el servidor como el cliente pueden comprobar correctamente el estado de revocación de todos los certificados. El uso del comando **certutil** puede ayudarle a solucionar los errores.

Obtenga más información en este artículo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configuración del agente de escucha en el recopilador de eventos

1. Establezca la autenticación del certificado con el siguiente comando:

    **WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**

2. En el equipo del recopilador de eventos debe existir un agente de escucha HTTPS de WinRM con la impresión en miniatura del certificado de autenticación del servidor. Esto se puede comprobar con el siguiente comando:

    **WinRM e WinRM/config/Listener**

3. Si no ve el agente de escucha HTTPS, o si la impresión en miniatura del agente de escucha HTTPS no es la misma que la del certificado de autenticación del servidor en el equipo del recopilador, puede eliminar ese agente de escucha y crear uno nuevo con la impresión de miniatura correcta. Para eliminar el agente de escucha https, use el siguiente comando:

    **¿eliminar WinRM/config/Listener? Address = * + Transport = HTTPS**

    Para crear un nuevo agente de escucha, use el siguiente comando:

    **¿crear WinRM/config/Listener? Address =&#42;+ Transport = https @ {hostname = "** &lt; _FQDN del recopilador_ &gt; **"; CertificateThumbprint = "** &lt; _impresión en miniatura del certificado de autenticación del servidor_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurar la asignación de certificados en el recopilador de eventos

1. Cree un nuevo usuario local y agréguelo al grupo de administradores local.
2. Cree la asignación de certificados mediante un certificado presente en las "entidades de certificación raíz de confianza" o "entidades de certificación intermedias".

    Este es el certificado de la entidad de certificación raíz o intermedia que emitió los certificados instalados en los equipos de origen de eventos *(para evitar confusiones, es decir, la CA que está inmediatamente por encima del certificado en la cadena de certificados)*:

    **¿crear WinRM/config/Service/certmapping?** = &lt; _Huella digital del emisor del certificado de CA emisor_ &gt; **+ asunto =&#42;+ URI =&#42; @ {nombredeusuario = "** &lt; _nombre de usuario_ &gt; **"; Password = "** &lt; _contraseña_ &gt; **"}-Remote: localhost**

3. Desde un cliente, pruebe el agente de escucha y la asignación de certificados con el siguiente comando:

    **WinRM g WinRM/config-r:https://** &lt; FQDN del recopilador de _eventos_ &gt; **: 5986-a:Certificate-Certificate: "** &lt; _Huella digital del certificado_ &gt; de autenticación del cliente **"**

    Esto debería devolver la configuración de WinRM del recopilador de eventos. **No mueva más** allá de este paso si no se muestra la configuración.

    **¿Qué ocurre en este paso?**
    - El cliente se conecta al recopilador de eventos y envía el certificado especificado
    - El recopilador de eventos busca la CA emisora y comprueba si es una asignación de certificado coincidente.
    - El recopilador de eventos valida la cadena de certificados de cliente y el estado de revocación
    - Si los pasos anteriores se realizan correctamente, se completa la autenticación.

> [!NOTE]
> Podría obtener un error de acceso denegado que se queja sobre el método de autenticación, lo que podría ser engañoso. Para solucionar el problema, compruebe el registro de CAPI en el recopilador de eventos.

4. Enumere las entradas certmapping configuradas con el comando: **WinRM enum WinRM/config/Service/certmapping**

### <a name="event-source-computer-configuration"></a>Configuración del equipo de origen de eventos

1. Inicie sesión con una cuenta de administrador y abra el Editor de directivas de grupo local (gpedit. msc).
2. Vaya al equipo local \ configuración del Equipo\plantillas Administrativas\componentes de Components\Event reenvío.
3. Abra la Directiva "configurar la dirección del servidor, el intervalo de actualización y la entidad emisora de certificados de un administrador de suscripciones de destino".
4. Habilite la Directiva y haga clic en el SubscriptionManagers "Mostrar..." botón.
5. En la ventana SubscriptionManagers, escriba la siguiente cadena:

    **Servidor = https://** &lt; _FQDN del servidor_ &gt; del recopilador de eventos **: 5986/wsman/SubscriptionManager/WEC, Refresh =** &lt; _Intervalo de actualización en segundos_ &gt; **, IssuerCA =** &lt; _Huella digital del certificado de CA emisora_&gt;

6. Ejecute la siguiente línea de comandos para actualizar la configuración de directiva de grupo local: gpupdate/force
7. Estos pasos deben generar el evento 104 en el equipo de origen Visor de eventos el registro de aplicaciones y servicios Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational con el siguiente mensaje:

    "El reenviador se ha conectado correctamente al administrador de suscripciones en la dirección &lt; FQDN &gt; seguido del evento 100 con el mensaje:" la suscripción &lt; sub_name &gt; se creó correctamente ".

8. En el recopilador de eventos, el estado en tiempo de ejecución de la suscripción mostrará ahora 1 equipo activo.
9. Abra el registro Eventos reenviados en el recopilador de eventos y compruebe si tiene los eventos reenviados desde los equipos de origen.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Conceder el permiso para la clave privada del certificado de cliente en el origen del evento

1. Abra la consola de administración de certificados para equipo local en el equipo de origen de eventos.
2. Haga clic con el botón derecho en el certificado de cliente y administre las claves privadas.
3. Conceda permiso de lectura al usuario del servicio de red.

### <a name="event-subscription-configuration"></a>Configuración de suscripción de eventos

1. Abra Visor de eventos en el recopilador de eventos y navegue hasta el nodo Suscripciones.
2. Haga clic con el botón secundario en suscripciones y elija "crear suscripción...".
3. Asigne un nombre y una descripción opcional para la nueva suscripción.
4. Seleccione la opción "Iniciado por el equipo de origen" y haga clic en "seleccionar grupos de equipos...".
5. En grupos de equipos, haga clic en "agregar equipos que no son de dominio..." y escriba el nombre de host del origen del evento.
6. Haga clic en "agregar certificados..." y agregue el certificado de la entidad de certificación que emite los certificados de cliente. Puede hacer clic en ver certificado para validar el certificado.
7. En entidades de certificación, haga clic en Aceptar para agregar el certificado.
8. Cuando termine de agregar equipos, haga clic en Aceptar.
9. De nuevo a las propiedades de la suscripción, haga clic en seleccionar eventos...
10. Configure el filtro de consulta de eventos especificando los niveles de evento, los registros de eventos o los orígenes de eventos, los IDENTIFICADOres de evento y cualquier otra opción de filtrado.
11. En las propiedades de la suscripción, haga clic en opciones avanzadas...
12. Elija una de las opciones de optimización para la entrega de eventos desde el evento de origen al recopilador de eventos o deje el valor predeterminado normal: 
    1. **Minimizar el ancho de banda**: los eventos se entregarán menos frecuencia para ahorrar ancho de banda.
    2. **Minimizar la latencia**: los eventos se entregarán en cuanto se produzcan para reducir la latencia de los eventos.
13. Cambie el protocolo a HTTPS y haga clic en Aceptar.
14. Haga clic en Aceptar para crear la nueva suscripción.
15. Para comprobar el estado de tiempo de ejecución de la suscripción, haga clic con el botón derecho y seleccione "estado en tiempo de ejecución"
