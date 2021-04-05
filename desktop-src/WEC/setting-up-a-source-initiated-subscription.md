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
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="dc04e-103">Configuración de una suscripción iniciada por el origen</span><span class="sxs-lookup"><span data-stu-id="dc04e-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="dc04e-104">Las suscripciones iniciadas por el origen permiten definir una suscripción en un equipo del recopilador de eventos sin definir los equipos de origen del evento y, a continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="dc04e-105">Esto difiere de una suscripción iniciada por el recopilador porque en el modelo de suscripción Iniciado por el recopilador, el recopilador de eventos debe definir todos los orígenes de eventos de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="dc04e-106">Al configurar una suscripción iniciada por el origen, considere si los equipos de origen de eventos están en el mismo dominio que el equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="dc04e-107">En las secciones siguientes se describen los pasos que se deben seguir cuando los orígenes de eventos están en el mismo dominio o no en el mismo dominio que el equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="dc04e-108">Cualquier equipo de un dominio, local o remoto, puede ser un recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="dc04e-109">Sin embargo, al elegir un recopilador de eventos, es importante seleccionar una máquina topológicamente cercana a la ubicación en la que se generará la mayoría de los eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="dc04e-110">El envío de eventos a un equipo en una ubicación de red lejana en una WAN puede reducir el rendimiento general y la eficacia de la recopilación de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="dc04e-111">Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos están en el mismo dominio que el equipo del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="dc04e-112">Tanto los equipos de origen de eventos como el equipo del recopilador de eventos deben estar configurados para configurar una suscripción iniciada por el origen.</span><span class="sxs-lookup"><span data-stu-id="dc04e-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="dc04e-113">En estas instrucciones se da por hecho que tiene acceso de administrador al controlador de dominio de Windows Server que atiende al dominio en el que se configurarán los equipos remotos para recopilar eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="dc04e-114">Configuración del equipo de origen de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="dc04e-115">Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Administración remota de Windows:</span><span class="sxs-lookup"><span data-stu-id="dc04e-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="dc04e-116">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="dc04e-117">Inicie la Directiva de grupo mediante la ejecución del siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="dc04e-118">**% SYSTEMROOT% \\ system32 \\ gpedit. msc**</span><span class="sxs-lookup"><span data-stu-id="dc04e-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="dc04e-119">En el **nodo configuración del equipo** , expanda el nodo **plantillas administrativas** , expanda el nodo **componentes de Windows** y, a continuación, seleccione el nodo **reenvío de eventos** .</span><span class="sxs-lookup"><span data-stu-id="dc04e-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="dc04e-120">Haga clic con el botón secundario en el valor **SubscriptionManager** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="dc04e-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="dc04e-121">Habilite la opción **SubscriptionManager** y haga clic en el botón **Mostrar** para agregar una dirección de servidor a la configuración.</span><span class="sxs-lookup"><span data-stu-id="dc04e-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="dc04e-122">Agregue al menos un valor de configuración que especifique el equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="dc04e-123">La ventana **propiedades de SubscriptionManager** contiene una pestaña **explicativa** que describe la sintaxis de la configuración.</span><span class="sxs-lookup"><span data-stu-id="dc04e-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="dc04e-124">Una vez agregada la configuración **SubscriptionManager** , ejecute el siguiente comando para asegurarse de que se aplica la Directiva:</span><span class="sxs-lookup"><span data-stu-id="dc04e-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="dc04e-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="dc04e-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="dc04e-126">Configuración del equipo del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="dc04e-127">Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para configurar Administración remota de Windows:</span><span class="sxs-lookup"><span data-stu-id="dc04e-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="dc04e-128">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="dc04e-129">Ejecute el siguiente comando para configurar el servicio Recopilador de eventos:</span><span class="sxs-lookup"><span data-stu-id="dc04e-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="dc04e-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="dc04e-131">Cree una suscripción iniciada por el origen.</span><span class="sxs-lookup"><span data-stu-id="dc04e-131">Create a source initiated subscription.</span></span> <span data-ttu-id="dc04e-132">Esto puede realizarse mediante programación, mediante el Visor de eventos o mediante [**Wecutil.exe**](wecutil.md).</span><span class="sxs-lookup"><span data-stu-id="dc04e-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="dc04e-133">Para obtener más información sobre cómo crear la suscripción mediante programación, vea el ejemplo de código de [creación de una suscripción iniciada](creating-a-source-initiated-subscription.md)por el origen.</span><span class="sxs-lookup"><span data-stu-id="dc04e-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="dc04e-134">Si usa Wecutil.exe, debe crear un archivo XML de suscripción de eventos y usar el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="dc04e-135">**wecutil cs** *configurationFile.xml*</span><span class="sxs-lookup"><span data-stu-id="dc04e-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="dc04e-136">El siguiente código XML es un ejemplo del contenido de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos desde el registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados en el equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

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
    > <span data-ttu-id="dc04e-137">Al crear una suscripción iniciada por el origen, si AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList y DeniedSubjectList están todos vacíos, entonces "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "se usará como descriptor de seguridad predeterminado para AllowedSourceDomainComputers.</span><span class="sxs-lookup"><span data-stu-id="dc04e-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="dc04e-138">El descriptor predeterminado concede a los miembros del grupo de dominio equipos del dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04e-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="dc04e-139">Para validar que la suscripción funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="dc04e-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="dc04e-140">En el equipo del recopilador de eventos, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc04e-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="dc04e-141">Ejecute el siguiente comando desde un símbolo del sistema con privilegios elevados en el controlador de dominio de Windows Server para obtener el estado de tiempo de ejecución de la suscripción:</span><span class="sxs-lookup"><span data-stu-id="dc04e-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="dc04e-142">**wecutil gr** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="dc04e-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="dc04e-143">Compruebe que el origen del evento se ha conectado.</span><span class="sxs-lookup"><span data-stu-id="dc04e-143">Verify that the event source has connected.</span></span> <span data-ttu-id="dc04e-144">Es posible que tenga que esperar hasta que se haya creado el intervalo de actualización especificado en la Directiva después de crear la suscripción para que el origen del evento se conecte.</span><span class="sxs-lookup"><span data-stu-id="dc04e-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="dc04e-145">Ejecute el siguiente comando para obtener la información de la suscripción:</span><span class="sxs-lookup"><span data-stu-id="dc04e-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="dc04e-146">**wecutil GS** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="dc04e-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="dc04e-147">Obtiene el valor de DeliveryMaxItems de la información de suscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04e-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="dc04e-148">En el equipo de origen del evento, genere los eventos que coinciden con la consulta de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="dc04e-149">Se debe generar el número de eventos DeliveryMaxItems para que se reenvíen los eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="dc04e-150">En el equipo del recopilador de eventos, compruebe que los eventos se han reenviado al registro Eventos reenviados o al registro especificado en la suscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04e-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="dc04e-151">Reenvío del registro de seguridad</span><span class="sxs-lookup"><span data-stu-id="dc04e-151">Forwarding the security log</span></span>

<span data-ttu-id="dc04e-152">Para poder reenviar el registro de seguridad, debe agregar la cuenta de servicio de red al grupo lectores del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="dc04e-153">Configuración de una suscripción iniciada por el origen en la que los orígenes de eventos no están en el mismo dominio que el equipo del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="dc04e-154">En estas instrucciones se da por hecho que tiene acceso de administrador a un controlador de dominio de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dc04e-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="dc04e-155">En este caso, dado que el equipo o equipos del recopilador de eventos remotos no están en el dominio atendido por el controlador de dominio, es esencial iniciar un cliente individual estableciendo Administración remota de Windows en "automático" mediante servicios (Services. msc).</span><span class="sxs-lookup"><span data-stu-id="dc04e-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="dc04e-156">Como alternativa, puede ejecutar "WinRM quickconfig" en cada cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="dc04e-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="dc04e-157">Antes de crear la suscripción, deben cumplirse los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="dc04e-158">En el equipo del recopilador de eventos, ejecute los siguientes comandos desde un símbolo del sistema con privilegios elevados para configurar Administración remota de Windows y el servicio Recopilador de eventos:</span><span class="sxs-lookup"><span data-stu-id="dc04e-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="dc04e-159">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-159">**winrm qc -q**</span></span>

    <span data-ttu-id="dc04e-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="dc04e-161">El equipo del recopilador debe tener un certificado de autenticación de servidor (certificado con un propósito de autenticación de servidor) en un almacén de certificados del equipo local.</span><span class="sxs-lookup"><span data-stu-id="dc04e-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="dc04e-162">En el equipo de origen del evento, ejecute el siguiente comando para configurar Administración remota de Windows:</span><span class="sxs-lookup"><span data-stu-id="dc04e-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="dc04e-163">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="dc04e-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="dc04e-164">El equipo de origen debe tener un certificado de autenticación del cliente (certificado con un propósito de autenticación del cliente) en un almacén de certificados del equipo local.</span><span class="sxs-lookup"><span data-stu-id="dc04e-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="dc04e-165">El puerto 5986 está abierto en el equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="dc04e-166">Para abrir este puerto, ejecute el comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-166">To open this port, run the command:</span></span>

    <span data-ttu-id="dc04e-167">**netsh firewall Add portopening TCP 5986 "WinRM HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="dc04e-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="dc04e-168">Requisitos de certificados</span><span class="sxs-lookup"><span data-stu-id="dc04e-168">Certificates requirements</span></span>

- <span data-ttu-id="dc04e-169">Se debe instalar un certificado de autenticación de servidor en el equipo del recopilador de eventos del almacén personal del equipo local.</span><span class="sxs-lookup"><span data-stu-id="dc04e-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="dc04e-170">El sujeto de este certificado debe coincidir con el FQDN del recopilador.</span><span class="sxs-lookup"><span data-stu-id="dc04e-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="dc04e-171">Es necesario instalar un certificado de autenticación del cliente en los equipos de origen del evento en el almacén personal del equipo local.</span><span class="sxs-lookup"><span data-stu-id="dc04e-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="dc04e-172">El sujeto de este certificado debe coincidir con el FQDN del equipo.</span><span class="sxs-lookup"><span data-stu-id="dc04e-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="dc04e-173">Si el certificado de cliente ha sido emitido por una entidad de certificación distinta de la del recopilador de eventos, esos certificados raíz e intermedio deben instalarse también en el recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="dc04e-174">Si el certificado de cliente lo emitió una entidad de certificación intermedia y el recopilador ejecuta Windows 2012 o una versión posterior, tendrá que configurar la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="dc04e-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="dc04e-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="dc04e-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="dc04e-176">Compruebe que tanto el servidor como el cliente pueden comprobar correctamente el estado de revocación de todos los certificados.</span><span class="sxs-lookup"><span data-stu-id="dc04e-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="dc04e-177">El uso del comando **certutil** puede ayudarle a solucionar los errores.</span><span class="sxs-lookup"><span data-stu-id="dc04e-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="dc04e-178">Obtenga más información en este artículo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="dc04e-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="dc04e-179">Configuración del agente de escucha en el recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="dc04e-180">Establezca la autenticación del certificado con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="dc04e-181">**WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="dc04e-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="dc04e-182">En el equipo del recopilador de eventos debe existir un agente de escucha HTTPS de WinRM con la impresión en miniatura del certificado de autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="dc04e-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="dc04e-183">Esto se puede comprobar con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="dc04e-184">**WinRM e WinRM/config/Listener**</span><span class="sxs-lookup"><span data-stu-id="dc04e-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="dc04e-185">Si no ve el agente de escucha HTTPS, o si la impresión en miniatura del agente de escucha HTTPS no es la misma que la del certificado de autenticación del servidor en el equipo del recopilador, puede eliminar ese agente de escucha y crear uno nuevo con la impresión de miniatura correcta.</span><span class="sxs-lookup"><span data-stu-id="dc04e-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="dc04e-186">Para eliminar el agente de escucha https, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="dc04e-187">**¿eliminar WinRM/config/Listener? Address = \* + Transport = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="dc04e-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="dc04e-188">Para crear un nuevo agente de escucha, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="dc04e-189">**¿crear WinRM/config/Listener? Address =&#42;+ Transport = https @ {hostname = "** &lt; _FQDN del recopilador_ &gt; **"; CertificateThumbprint = "** &lt; _impresión en miniatura del certificado de autenticación del servidor_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="dc04e-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="dc04e-190">Configurar la asignación de certificados en el recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="dc04e-191">Cree un nuevo usuario local y agréguelo al grupo de administradores local.</span><span class="sxs-lookup"><span data-stu-id="dc04e-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="dc04e-192">Cree la asignación de certificados mediante un certificado presente en las "entidades de certificación raíz de confianza" o "entidades de certificación intermedias".</span><span class="sxs-lookup"><span data-stu-id="dc04e-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="dc04e-193">Este es el certificado de la entidad de certificación raíz o intermedia que emitió los certificados instalados en los equipos de origen de eventos *(para evitar confusiones, es decir, la CA que está inmediatamente por encima del certificado en la cadena de certificados)*:</span><span class="sxs-lookup"><span data-stu-id="dc04e-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="dc04e-194">**¿crear WinRM/config/Service/certmapping?** = &lt; _Huella digital del emisor del certificado de CA emisor_ &gt; **+ asunto =&#42;+ URI =&#42; @ {nombredeusuario = "** &lt; _nombre de usuario_ &gt; **"; Password = "** &lt; _contraseña_ &gt; **"}-Remote: localhost**</span><span class="sxs-lookup"><span data-stu-id="dc04e-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="dc04e-195">Desde un cliente, pruebe el agente de escucha y la asignación de certificados con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="dc04e-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="dc04e-196">**WinRM g WinRM/config-r:https://** &lt; FQDN del recopilador de _eventos_ &gt; **: 5986-a:Certificate-Certificate: "** &lt; _Huella digital del certificado_ &gt; de autenticación del cliente **"**</span><span class="sxs-lookup"><span data-stu-id="dc04e-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="dc04e-197">Esto debería devolver la configuración de WinRM del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="dc04e-198">**No mueva más** allá de este paso si no se muestra la configuración.</span><span class="sxs-lookup"><span data-stu-id="dc04e-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="dc04e-199">**¿Qué ocurre en este paso?**</span><span class="sxs-lookup"><span data-stu-id="dc04e-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="dc04e-200">El cliente se conecta al recopilador de eventos y envía el certificado especificado</span><span class="sxs-lookup"><span data-stu-id="dc04e-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="dc04e-201">El recopilador de eventos busca la CA emisora y comprueba si es una asignación de certificado coincidente.</span><span class="sxs-lookup"><span data-stu-id="dc04e-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="dc04e-202">El recopilador de eventos valida la cadena de certificados de cliente y el estado de revocación</span><span class="sxs-lookup"><span data-stu-id="dc04e-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="dc04e-203">Si los pasos anteriores se realizan correctamente, se completa la autenticación.</span><span class="sxs-lookup"><span data-stu-id="dc04e-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="dc04e-204">Podría obtener un error de acceso denegado que se queja sobre el método de autenticación, lo que podría ser engañoso.</span><span class="sxs-lookup"><span data-stu-id="dc04e-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="dc04e-205">Para solucionar el problema, compruebe el registro de CAPI en el recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="dc04e-206">Enumere las entradas certmapping configuradas con el comando: **WinRM enum WinRM/config/Service/certmapping**</span><span class="sxs-lookup"><span data-stu-id="dc04e-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="dc04e-207">Configuración del equipo de origen de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="dc04e-208">Inicie sesión con una cuenta de administrador y abra el Editor de directivas de grupo local (gpedit. msc).</span><span class="sxs-lookup"><span data-stu-id="dc04e-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="dc04e-209">Vaya al equipo local \ configuración del Equipo\plantillas Administrativas\componentes de Components\Event reenvío.</span><span class="sxs-lookup"><span data-stu-id="dc04e-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="dc04e-210">Abra la Directiva "configurar la dirección del servidor, el intervalo de actualización y la entidad emisora de certificados de un administrador de suscripciones de destino".</span><span class="sxs-lookup"><span data-stu-id="dc04e-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="dc04e-211">Habilite la Directiva y haga clic en el SubscriptionManagers "Mostrar..." botón.</span><span class="sxs-lookup"><span data-stu-id="dc04e-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="dc04e-212">En la ventana SubscriptionManagers, escriba la siguiente cadena:</span><span class="sxs-lookup"><span data-stu-id="dc04e-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="dc04e-213">**Servidor = https://** &lt; _FQDN del servidor_ &gt; del recopilador de eventos **: 5986/wsman/SubscriptionManager/WEC, Refresh =** &lt; _Intervalo de actualización en segundos_ &gt; **, IssuerCA =** &lt; _Huella digital del certificado de CA emisora_&gt;</span><span class="sxs-lookup"><span data-stu-id="dc04e-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="dc04e-214">Ejecute la siguiente línea de comandos para actualizar la configuración de directiva de grupo local: gpupdate/force</span><span class="sxs-lookup"><span data-stu-id="dc04e-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="dc04e-215">Estos pasos deben generar el evento 104 en el equipo de origen Visor de eventos el registro de aplicaciones y servicios Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational con el siguiente mensaje:</span><span class="sxs-lookup"><span data-stu-id="dc04e-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="dc04e-216">"El reenviador se ha conectado correctamente al administrador de suscripciones en la dirección &lt; FQDN &gt; seguido del evento 100 con el mensaje:" la suscripción &lt; sub_name &gt; se creó correctamente ".</span><span class="sxs-lookup"><span data-stu-id="dc04e-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="dc04e-217">En el recopilador de eventos, el estado en tiempo de ejecución de la suscripción mostrará ahora 1 equipo activo.</span><span class="sxs-lookup"><span data-stu-id="dc04e-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="dc04e-218">Abra el registro Eventos reenviados en el recopilador de eventos y compruebe si tiene los eventos reenviados desde los equipos de origen.</span><span class="sxs-lookup"><span data-stu-id="dc04e-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="dc04e-219">Conceder el permiso para la clave privada del certificado de cliente en el origen del evento</span><span class="sxs-lookup"><span data-stu-id="dc04e-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="dc04e-220">Abra la consola de administración de certificados para equipo local en el equipo de origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="dc04e-221">Haga clic con el botón derecho en el certificado de cliente y administre las claves privadas.</span><span class="sxs-lookup"><span data-stu-id="dc04e-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="dc04e-222">Conceda permiso de lectura al usuario del servicio de red.</span><span class="sxs-lookup"><span data-stu-id="dc04e-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="dc04e-223">Configuración de suscripción de eventos</span><span class="sxs-lookup"><span data-stu-id="dc04e-223">Event subscription configuration</span></span>

1. <span data-ttu-id="dc04e-224">Abra Visor de eventos en el recopilador de eventos y navegue hasta el nodo Suscripciones.</span><span class="sxs-lookup"><span data-stu-id="dc04e-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="dc04e-225">Haga clic con el botón secundario en suscripciones y elija "crear suscripción...".</span><span class="sxs-lookup"><span data-stu-id="dc04e-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="dc04e-226">Asigne un nombre y una descripción opcional para la nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04e-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="dc04e-227">Seleccione la opción "Iniciado por el equipo de origen" y haga clic en "seleccionar grupos de equipos...".</span><span class="sxs-lookup"><span data-stu-id="dc04e-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="dc04e-228">En grupos de equipos, haga clic en "agregar equipos que no son de dominio..."</span><span class="sxs-lookup"><span data-stu-id="dc04e-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="dc04e-229">y escriba el nombre de host del origen del evento.</span><span class="sxs-lookup"><span data-stu-id="dc04e-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="dc04e-230">Haga clic en "agregar certificados..."</span><span class="sxs-lookup"><span data-stu-id="dc04e-230">Click “Add Certificates…”</span></span> <span data-ttu-id="dc04e-231">y agregue el certificado de la entidad de certificación que emite los certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="dc04e-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="dc04e-232">Puede hacer clic en ver certificado para validar el certificado.</span><span class="sxs-lookup"><span data-stu-id="dc04e-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="dc04e-233">En entidades de certificación, haga clic en Aceptar para agregar el certificado.</span><span class="sxs-lookup"><span data-stu-id="dc04e-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="dc04e-234">Cuando termine de agregar equipos, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="dc04e-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="dc04e-235">De nuevo a las propiedades de la suscripción, haga clic en seleccionar eventos...</span><span class="sxs-lookup"><span data-stu-id="dc04e-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="dc04e-236">Configure el filtro de consulta de eventos especificando los niveles de evento, los registros de eventos o los orígenes de eventos, los IDENTIFICADOres de evento y cualquier otra opción de filtrado.</span><span class="sxs-lookup"><span data-stu-id="dc04e-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="dc04e-237">En las propiedades de la suscripción, haga clic en opciones avanzadas...</span><span class="sxs-lookup"><span data-stu-id="dc04e-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="dc04e-238">Elija una de las opciones de optimización para la entrega de eventos desde el evento de origen al recopilador de eventos o deje el valor predeterminado normal:</span><span class="sxs-lookup"><span data-stu-id="dc04e-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="dc04e-239">**Minimizar el ancho de banda**: los eventos se entregarán menos frecuencia para ahorrar ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="dc04e-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="dc04e-240">**Minimizar la latencia**: los eventos se entregarán en cuanto se produzcan para reducir la latencia de los eventos.</span><span class="sxs-lookup"><span data-stu-id="dc04e-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="dc04e-241">Cambie el protocolo a HTTPS y haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="dc04e-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="dc04e-242">Haga clic en Aceptar para crear la nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04e-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="dc04e-243">Para comprobar el estado de tiempo de ejecución de la suscripción, haga clic con el botón derecho y seleccione "estado en tiempo de ejecución"</span><span class="sxs-lookup"><span data-stu-id="dc04e-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
