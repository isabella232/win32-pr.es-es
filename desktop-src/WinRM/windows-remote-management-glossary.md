---
title: Administración remota de Windows Glosario
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105678667"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="5cc03-103">Administración remota de Windows Glosario</span><span class="sxs-lookup"><span data-stu-id="5cc03-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="5cc03-104">wsman: items \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5cc03-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-105">WS-Management elemento de protocolo devuelto en una enumeración que obtiene las instancias y la instancia de [*EPRs*](/windows).</span><span class="sxs-lookup"><span data-stu-id="5cc03-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="5cc03-106">**wsman: items** es un contenedor que contiene una instancia y su EPR.</span><span class="sxs-lookup"><span data-stu-id="5cc03-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="5cc03-107">Este tipo de enumeración se inicia cuando se establece la marca **WSManFlagReturnObjectAndEPR** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cc03-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="5cc03-108">B</span><span class="sxs-lookup"><span data-stu-id="5cc03-108">B</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-109">**controlador de administración de placa base (BMC)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-110">Microcontrolador conectado localmente a un servidor.</span><span class="sxs-lookup"><span data-stu-id="5cc03-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="5cc03-111">Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5cc03-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="5cc03-112">Tiene acceso a los datos de BMC a través del proveedor WMI de [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-113">**Autenticación básica**</span><span class="sxs-lookup"><span data-stu-id="5cc03-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-114">El nombre de usuario y la contraseña enviados en el intercambio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5cc03-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="5cc03-115">La autenticación básica puede configurarse para usar el transporte HTTP o HTTPS en un dominio o grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="5cc03-116">Este método de autenticación es el menos seguro de todos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-117">**BMC**</span><span class="sxs-lookup"><span data-stu-id="5cc03-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-118">Consulte [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="5cc03-119">C</span><span class="sxs-lookup"><span data-stu-id="5cc03-119">C</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-120">**ESTUDIO**</span><span class="sxs-lookup"><span data-stu-id="5cc03-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-121">Consulte [*modelo de información común (CIM)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-122">**client**</span><span class="sxs-lookup"><span data-stu-id="5cc03-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-123">La aplicación cliente que usa el protocolo WS-Management para tener acceso al servicio de administración en el equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="5cc03-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-124">**Modelo de información común (CIM)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-125">El modelo de la [*aplicación de administración distribuida (DMTF)*](windows-remote-management-glossary.md) que describe cómo representar los objetos de equipo y de red del mundo real.</span><span class="sxs-lookup"><span data-stu-id="5cc03-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="5cc03-126">CIM utiliza un paradigma orientado a objetos, donde los objetos administrados se modelan mediante los conceptos de clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="5cc03-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="5cc03-127">D</span><span class="sxs-lookup"><span data-stu-id="5cc03-127">D</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-128">**Autenticación implícita**</span><span class="sxs-lookup"><span data-stu-id="5cc03-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-129">Un intercambio en el que el servidor recibe una solicitud de un cliente y envía datos sobre el cliente a un servidor de autenticación, normalmente un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="5cc03-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="5cc03-130">Si el cliente está autenticado, el servidor recibe una clave de sesión implícita que se usa para autenticar las solicitudes posteriores desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="5cc03-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-131">**Distributed Management Task Force (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-132">La organización del sector que desarrolla estándares de administración y tecnología de integración para entornos empresariales y de Internet.</span><span class="sxs-lookup"><span data-stu-id="5cc03-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-133">**DTMF**</span><span class="sxs-lookup"><span data-stu-id="5cc03-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-134">Consulte [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="5cc03-135">E</span><span class="sxs-lookup"><span data-stu-id="5cc03-135">E</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-136">**finales**</span><span class="sxs-lookup"><span data-stu-id="5cc03-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-137">Un recurso que se puede direccionar mediante una [*referencia de extremo (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-138">**referencia de extremo (EPR)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-139">Combinación de elementos de dirección WS-Addressing y WS-Management que describen de forma conjunta una dirección de un recurso en el encabezado SOAP del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5cc03-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="5cc03-140">Se trata de un término de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="5cc03-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-141">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="5cc03-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-142">Conjunto o colección de instancias de [*recurso*](windows-remote-management-glossary.md) o acción de solicitar este conjunto.</span><span class="sxs-lookup"><span data-stu-id="5cc03-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="5cc03-143">En WS-Management protocolo, se usa [*WS-Enumeration*](windows-remote-management-glossary.md) para obtener la colección.</span><span class="sxs-lookup"><span data-stu-id="5cc03-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="5cc03-144">En la implementación de scripting del servicio WinRM de enumeración, se usan [**Session. Enumerate**](session-enumerate.md) y el objeto de [**enumerador**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="5cc03-145">El método y la interfaz de C++ correspondientes son [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) y [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="5cc03-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="5cc03-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-147">Consulte [*referencia de extremo (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-148">**Servicio de recopilación de eventos**</span><span class="sxs-lookup"><span data-stu-id="5cc03-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-149">Componente del sistema operativo que recibe eventos del BMC y otros componentes o aplicaciones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-150">**reenvío de eventos**</span><span class="sxs-lookup"><span data-stu-id="5cc03-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-151">Una notificación de eventos que se producen en equipos remotos se puede enviar a aplicaciones de suscripción.</span><span class="sxs-lookup"><span data-stu-id="5cc03-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="5cc03-152">El reenvío de eventos no es una característica de WinRM, sino del [registro de eventos de Windows](/windows/desktop/WES/windows-event-log).</span><span class="sxs-lookup"><span data-stu-id="5cc03-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="5cc03-153">El reenvío de eventos está disponible por primera vez en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5cc03-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="5cc03-154">Las aplicaciones de administración, como Microsoft Operations Manager (MOM) usan el reenvío de eventos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="5cc03-155">F</span><span class="sxs-lookup"><span data-stu-id="5cc03-155">F</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="5cc03-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-157">Mecanismo de consulta para especificar un conjunto limitado de instancias en la solicitud de un [*recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-158">Puede especificar un parámetro de *filtro* en las llamadas a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="5cc03-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-159">**dialecto de filtro**</span><span class="sxs-lookup"><span data-stu-id="5cc03-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-160">Cadena XML que identifica el dialecto XML usado para especificar un [*filtro*](windows-remote-management-glossary.md) en una llamada a [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="5cc03-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="5cc03-161">El servicio WinRM admite [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialecto de filtro al recibir solicitudes.</span><span class="sxs-lookup"><span data-stu-id="5cc03-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-162">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="5cc03-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-163">Cadena XML que identifica parte de una instancia de un recurso en lugar de todo el recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc03-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="5cc03-164">La compatibilidad de fragmentos se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-165">**dialecto de fragmento**</span><span class="sxs-lookup"><span data-stu-id="5cc03-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-166">Cadena XML que identifica el dialecto XML usado para especificar un [*fragmento*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-167">La compatibilidad de fragmentos se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="5cc03-168">El servicio WinRM admite [*XPath*](windows-remote-management-glossary.md) para el dialecto de fragmentos al recibir solicitudes.</span><span class="sxs-lookup"><span data-stu-id="5cc03-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="5cc03-169">I</span><span class="sxs-lookup"><span data-stu-id="5cc03-169">I</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-170">**en banda**</span><span class="sxs-lookup"><span data-stu-id="5cc03-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-171">La aplicación cliente obtiene los datos de BMC a través del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-172">**Interfaz de administración de plataforma inteligente (IPMI)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-173">Un estándar del sector de TI para la arquitectura del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-174">Las características de administración de hardware de Windows proporcionan un [*controlador IPMI*](windows-remote-management-glossary.md) y un [*proveedor IPMI*](windows-remote-management-glossary.md) de WMI que permite que los scripts de administración, las herramientas de línea de comandos y las aplicaciones obtengan datos de BMC.</span><span class="sxs-lookup"><span data-stu-id="5cc03-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="5cc03-175">El proveedor IPMI tiene [clases](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="5cc03-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-177">Vea [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-178">**Controlador IPMI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-179">El controlador de kernel que permite el acceso a los dispositivos del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) desde los componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-180">**Proveedor IPMI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-181">Proveedor WMI estándar que define las clases que modelan la [*IPMI*](windows-remote-management-glossary.md) y sus datos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="5cc03-182">El [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un archivo dll com que obtiene datos de BMC.</span><span class="sxs-lookup"><span data-stu-id="5cc03-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="5cc03-183">K</span><span class="sxs-lookup"><span data-stu-id="5cc03-183">K</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-184">**KCS**</span><span class="sxs-lookup"><span data-stu-id="5cc03-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-185">Consulte [*estilo de controladora de teclado (KCS)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-186">**Autenticación Kerberos**</span><span class="sxs-lookup"><span data-stu-id="5cc03-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-187">Método de autenticación mutua entre el cliente y el servidor que usa claves cifradas.</span><span class="sxs-lookup"><span data-stu-id="5cc03-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="5cc03-188">En el caso de los equipos que se ejecutan en un sistema operativo basado en Windows, la cuenta de cliente debe ser una cuenta de dominio en el mismo dominio que el servidor.</span><span class="sxs-lookup"><span data-stu-id="5cc03-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="5cc03-189">Cuando un cliente usa las credenciales predeterminadas, Kerberos es el método de autenticación si la cadena de conexión no es una de las siguientes: localhost, 127.0.0.1 o \[ :: 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5cc03-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-190">**Estilo de controlador de teclado (KCS)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-191">Protocolo utilizado por el [*controlador IPMI*](windows-remote-management-glossary.md) para comunicarse con el [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="5cc03-192">L</span><span class="sxs-lookup"><span data-stu-id="5cc03-192">L</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="5cc03-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-194">Servicio de administración que implementa WS-Management protocolo para enviar y recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="5cc03-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="5cc03-195">WinRM es un servicio de escucha.</span><span class="sxs-lookup"><span data-stu-id="5cc03-195">WinRM is a listener service.</span></span> <span data-ttu-id="5cc03-196">Un agente de escucha se define mediante un transporte (HTTP o HTTPS) y una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="5cc03-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="5cc03-197">Puede crear más de una instancia del agente de escucha de WinRM en un solo equipo proporcionándole una dirección TCP/IP diferente o un número de puerto.</span><span class="sxs-lookup"><span data-stu-id="5cc03-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="5cc03-198">M</span><span class="sxs-lookup"><span data-stu-id="5cc03-198">M</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-199">**message**</span><span class="sxs-lookup"><span data-stu-id="5cc03-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-200">Paquete de información transmitida entre equipos o redes independientes construidas con el protocolo [*SOAP*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="5cc03-201">El paquete tiene un encabezado, que describe el destino del mensaje y el transporte, y un cuerpo que incluye el contenido que se va a utilizar cuando llegue el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5cc03-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="5cc03-202">Un mensaje es una combinación de elementos de especificaciones como [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)y [*WS-Management*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="5cc03-203">N</span><span class="sxs-lookup"><span data-stu-id="5cc03-203">N</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-204">**namespace**</span><span class="sxs-lookup"><span data-stu-id="5cc03-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-205">Un espacio de nombres [*WMI*](windows-remote-management-glossary.md) , que es una agrupación lógica de clases e instancias WMI para controlar el ámbito y el acceso.</span><span class="sxs-lookup"><span data-stu-id="5cc03-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="5cc03-206">La fuente más frecuente de datos de administración para sistemas que ejecutan Windows es el \\ espacio de nombres root cimv2, que contiene clases como el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="5cc03-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="5cc03-207">Los espacios de nombres aparecen en el URI de recurso para las clases WMI, por ejemplo https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .</span><span class="sxs-lookup"><span data-stu-id="5cc03-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-208">**Negociar la autenticación**</span><span class="sxs-lookup"><span data-stu-id="5cc03-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-209">Un tipo de autenticación negociada y de inicio de sesión único que es la implementación de Windows del [*mecanismo de negociación de GSSAPI simple y protegido (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-210">La negociación SPNEGO determina si la autenticación se controla mediante Kerberos o NTLM.</span><span class="sxs-lookup"><span data-stu-id="5cc03-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="5cc03-211">Kerberos es el mecanismo preferido.</span><span class="sxs-lookup"><span data-stu-id="5cc03-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="5cc03-212">Negociar la autenticación en sistemas basados en Windows también se denomina autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="5cc03-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-213">**sensor numérico**</span><span class="sxs-lookup"><span data-stu-id="5cc03-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-214">Un tipo numérico de sensor en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md), por ejemplo, temperatura o tensión.</span><span class="sxs-lookup"><span data-stu-id="5cc03-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="5cc03-215">O</span><span class="sxs-lookup"><span data-stu-id="5cc03-215">O</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-216">**Opción**</span><span class="sxs-lookup"><span data-stu-id="5cc03-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-217">Los datos adicionales requeridos por el proveedor de recursos para procesar una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cc03-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="5cc03-218">Por ejemplo, algunos proveedores de WMI requieren datos adicionales proporcionados como objetos [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="5cc03-219">La compatibilidad con la opción se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-220">**fuera de banda**</span><span class="sxs-lookup"><span data-stu-id="5cc03-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-221">La aplicación cliente obtiene los datos directamente del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) de otro equipo, en lugar de hacerlo a través del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="5cc03-222">P</span><span class="sxs-lookup"><span data-stu-id="5cc03-222">P</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-223">**obtener**</span><span class="sxs-lookup"><span data-stu-id="5cc03-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-224">Se envía un mensaje de extracción [*de WS-Enumeration*](windows-remote-management-glossary.md) para continuar una enumeración iniciada por una llamada inicial a WS-Enumeration: Enumerate.</span><span class="sxs-lookup"><span data-stu-id="5cc03-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="5cc03-225">El [**enumerador**](enumerator-readitem.md) realiza la operación de extracción en el servicio WinRM. Readitem o [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span><span class="sxs-lookup"><span data-stu-id="5cc03-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="5cc03-226">R</span><span class="sxs-lookup"><span data-stu-id="5cc03-226">R</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-227">**resource**</span><span class="sxs-lookup"><span data-stu-id="5cc03-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-228">Un [*extremo*](windows-remote-management-glossary.md) que representa un tipo distinto de operación de administración o valor.</span><span class="sxs-lookup"><span data-stu-id="5cc03-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="5cc03-229">Un servicio expone uno o más recursos y algunos recursos pueden tener más de una instancia.</span><span class="sxs-lookup"><span data-stu-id="5cc03-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="5cc03-230">Un recurso de administración es similar a una clase WMI o una tabla de base de datos, y una instancia de es similar a una instancia de la clase o una fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="5cc03-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="5cc03-231">Por ejemplo, la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc03-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="5cc03-232">`Win32_LogicalDisk="C:\"` es una instancia específica del recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc03-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-233">**URI de recurso**</span><span class="sxs-lookup"><span data-stu-id="5cc03-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-234">[*Identificador uniforme de recursos (URI)*](windows-remote-management-glossary.md) que se usa para identificar un tipo específico de recurso, como discos o procesos, en un sistema.</span><span class="sxs-lookup"><span data-stu-id="5cc03-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="5cc03-235">S</span><span class="sxs-lookup"><span data-stu-id="5cc03-235">S</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-236">**SEL**</span><span class="sxs-lookup"><span data-stu-id="5cc03-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-237">Consulte [*registro de eventos del sistema (SEL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-238">**Adaptador SEL**</span><span class="sxs-lookup"><span data-stu-id="5cc03-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-239">Adaptador que envía los datos del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) al [*recopilador de eventos*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-240">**situado**</span><span class="sxs-lookup"><span data-stu-id="5cc03-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-241">Un par de nombre y valor que representa una instancia determinada de un [*recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-242">Es esencialmente un filtro o una "clave" que identifica la instancia deseada del recurso.</span><span class="sxs-lookup"><span data-stu-id="5cc03-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="5cc03-243">La compatibilidad con el selector se encuentra en el objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-244">**sensor**</span><span class="sxs-lookup"><span data-stu-id="5cc03-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-245">Un dispositivo de medición en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-246">**service**</span><span class="sxs-lookup"><span data-stu-id="5cc03-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-247">Aplicación que proporciona servicios de administración a los clientes a través del Protocolo de WS-Management y otros [*servicios web*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-248">Normalmente, un servicio es el mismo que el [*agente de escucha*](windows-remote-management-glossary.md) de una red.</span><span class="sxs-lookup"><span data-stu-id="5cc03-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="5cc03-249">El servicio tiene una dirección de transporte física.</span><span class="sxs-lookup"><span data-stu-id="5cc03-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-250">**sesión**</span><span class="sxs-lookup"><span data-stu-id="5cc03-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-251">Una conexión entre un [*cliente*](windows-remote-management-glossary.md) administración remota de Windows y el [*agente de escucha*](windows-remote-management-glossary.md)WinRM local o remoto, o servicio.</span><span class="sxs-lookup"><span data-stu-id="5cc03-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="5cc03-252">Esta conexión es similar a la conexión entre un script de cliente WMI y WMI en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5cc03-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="5cc03-253">Las operaciones de sesión, como enumerar un recurso (enumerar), obtener una instancia de un recurso (GET) o ejecutar un método de recursos (Invoke) son métodos del objeto de **sesión** .</span><span class="sxs-lookup"><span data-stu-id="5cc03-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="5cc03-254">[**WSMan. createSession**](wsman-createsession.md)crea un objeto de **sesión** .</span><span class="sxs-lookup"><span data-stu-id="5cc03-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-255">**Mecanismo de negociación simple y protegida de GSS-API (SPNEGO)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-256">Mecanismo de autenticación utilizado por el cliente o el servidor que recibe solicitudes de datos a través de WinRM en un contexto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5cc03-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="5cc03-257">SPNEGO se basa en un protocolo de solicitud de comentarios (RFC) producido por Internet Engineering Task Force (IETF).</span><span class="sxs-lookup"><span data-stu-id="5cc03-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="5cc03-258">SPNEGO también se conoce como [*autenticación integrada de Windows*](windows-remote-management-glossary.md), el término que se usa en los temas de ayuda de administración remota de Windows.</span><span class="sxs-lookup"><span data-stu-id="5cc03-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-259">**Protocolo simple de acceso a objetos (SOAP)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-260">Protocolo basado en XML utilizado por los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="5cc03-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-261">**SOAP**</span><span class="sxs-lookup"><span data-stu-id="5cc03-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-262">Vea [*Protocolo simple de acceso a objetos (SOAP)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="5cc03-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-264">Consulte [*mecanismo de negociación simple y protegida de GSS-API (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-265">**Registro de eventos del sistema (SEL)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-266">La base de datos de eventos en el hardware del [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="5cc03-267">El [*adaptador SEL*](windows-remote-management-glossary.md) transmite estos eventos al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="5cc03-268">U</span><span class="sxs-lookup"><span data-stu-id="5cc03-268">U</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-269">**identificador uniforme de recursos (URI)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-270">Cadena que identifica un recurso de la empresa, como un equipo, un proceso, una unidad de disco o un sensor de temperatura en un [*controlador de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-271">El URI es el mecanismo de direccionamiento del servicio Web definido en el identificador uniforme de recursos (URI) de Internet Engineering Task Force (IETF): Sintaxis genérica \[ RFC3986 \] .</span><span class="sxs-lookup"><span data-stu-id="5cc03-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-273">Consulte [*identificador uniforme de recursos (URI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="5cc03-274">W</span><span class="sxs-lookup"><span data-stu-id="5cc03-274">W</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-275">**servicio Web**</span><span class="sxs-lookup"><span data-stu-id="5cc03-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-276">Aplicación de software que se usa para la interacción entre equipos a través de Internet o una red.</span><span class="sxs-lookup"><span data-stu-id="5cc03-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="5cc03-277">Los servicios web se describen mediante el [*lenguaje de descripción de servicios web (WSDL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-278">La descripción específica del servicio web indica a otros servicios cómo interactuar con el servicio Web mediante mensajes SOAP.</span><span class="sxs-lookup"><span data-stu-id="5cc03-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="5cc03-279">Los mensajes se transmiten entre equipos mediante un transporte, normalmente HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5cc03-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="5cc03-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)y [*WS-Management*](windows-remote-management-glossary.md) son ejemplos de protocolos usados por las aplicaciones de servicios web para comunicarse entre sí.</span><span class="sxs-lookup"><span data-stu-id="5cc03-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-281">**Lenguaje de descripción de servicios web (WSDL)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-282">Lenguaje basado en XML que se usa para definir cómo interactuar con un servicio Web.</span><span class="sxs-lookup"><span data-stu-id="5cc03-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="5cc03-283">Normalmente, el WSDL describe qué mensajes SOAP requiere el servicio web para devolver datos o realizar operaciones.</span><span class="sxs-lookup"><span data-stu-id="5cc03-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="5cc03-284">El WSDL permite que una implementación de un sistema operativo se comunique con el servicio Web implementado en otro sistema operativo, siempre que se cumplan los requisitos del WSDL.</span><span class="sxs-lookup"><span data-stu-id="5cc03-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-285">**Autenticación integrada de Windows**</span><span class="sxs-lookup"><span data-stu-id="5cc03-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-286">Consulte [*negociar la autenticación*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-287">**Instrumental de administración de Windows (WMI)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-288">La implementación de Microsoft del estándar Web-Based Enterprise Management (WBEM) publicada por el [*equipo de administración distribuida (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5cc03-289">WMI permite administrar equipos locales y remotos y modela los objetos de equipo y red mediante una extensión del estándar [*modelo de información común (CIM)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc03-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-290">**Administración remota de Windows (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-291">Implementación de Microsoft de un servicio Web de administración basado en el protocolo [*WS-Management*](windows-remote-management-glossary.md) estándar público.</span><span class="sxs-lookup"><span data-stu-id="5cc03-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-292">**Shell remoto de Windows (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-293">Herramienta de Shell que se basa en [*administración remota de Windows*](windows-remote-management-glossary.md) para ejecutar comandos remotos, especialmente en el caso de los servidores sin periféricos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="5cc03-294">La herramienta de línea de comandos es Winrs.</span><span class="sxs-lookup"><span data-stu-id="5cc03-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-296">Consulte [*instrumental de administración de Windows (WMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-297">**Complemento WMI**</span><span class="sxs-lookup"><span data-stu-id="5cc03-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-298">El complemento WinRM que hace que los datos de WMI estén disponibles para los clientes de WinRM.</span><span class="sxs-lookup"><span data-stu-id="5cc03-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-299">**WS-Addressing (WSA)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-300">Un protocolo estándar público, que está basado en SOAP, que crea un sistema de direcciones usado en los encabezados de los mensajes enviados a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="5cc03-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="5cc03-301">El estándar define cómo se pueden ubicar los recursos a través de redes y firewalls.</span><span class="sxs-lookup"><span data-stu-id="5cc03-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="5cc03-302">WS-Addressing es uno de los protocolos de servicio Web que componen el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5cc03-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-303">**WS-Enumeration (wsen)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-304">Protocolo estándar público, que se basa en SOAP, para enumerar una secuencia de elementos XML que pueden representar colecciones de datos, registros u otras estructuras de información lineal.</span><span class="sxs-lookup"><span data-stu-id="5cc03-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="5cc03-305">WS-Enumeration es uno de los protocolos de servicio Web que componen el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5cc03-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-306">**WS-Eventing (WSE)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-307">Protocolo estándar público, que está basado en SOAP, que permite a un servicio Web (el suscriptor) suscribirse y aceptar mensajes de notificación de eventos de otro servicio Web (el origen del evento).</span><span class="sxs-lookup"><span data-stu-id="5cc03-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="5cc03-308">WS-Eventing es uno de los protocolos de servicio Web que componen el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5cc03-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-309">**WS-Management**</span><span class="sxs-lookup"><span data-stu-id="5cc03-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-310">Un protocolo estándar público, que está basado en SOAP, para compartir datos de administración entre todos los sistemas operativos, equipos y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="5cc03-311">Todos los [*mensajes*](windows-remote-management-glossary.md) enviados por los componentes de servidor o cliente de WinRM usan este protocolo.</span><span class="sxs-lookup"><span data-stu-id="5cc03-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5cc03-312">**WS-Transfer (wxf)**</span><span class="sxs-lookup"><span data-stu-id="5cc03-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-313">Un protocolo estándar público, que está basado en SOAP, para tener acceso a representaciones XML de recursos basados en servicios web a través de un sencillo conjunto de verbos como Get, Put, Invoke o DELETE.</span><span class="sxs-lookup"><span data-stu-id="5cc03-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="5cc03-314">WS-Transfer define operaciones para enviar y recibir la representación de un recurso determinado y operaciones para crear o eliminar un recurso y su representación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5cc03-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="5cc03-315">X</span><span class="sxs-lookup"><span data-stu-id="5cc03-315">X</span></span>

<dl> <dt>

<span data-ttu-id="5cc03-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="5cc03-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="5cc03-317">Una notación de ruta de acceso para direccionar partes de un documento XML, similar a una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="5cc03-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="5cc03-318">Una expresión XPath es una secuencia de frases que se va a obtener de la ubicación actual del documento XML a otro nodo o conjunto de nodos.</span><span class="sxs-lookup"><span data-stu-id="5cc03-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="5cc03-319">Las frases se separan con caracteres de barra diagonal ("/").</span><span class="sxs-lookup"><span data-stu-id="5cc03-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="5cc03-320">El servicio WinRM admite [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) para el [*dialecto de fragmentos*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5cc03-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 