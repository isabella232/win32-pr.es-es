---
title: Protocolo WS-Management
description: Estándar público para el intercambio remoto de datos de administración con cualquier dispositivo de equipo que implemente el protocolo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149606"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="4fc3e-103">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="4fc3e-103">WS-Management Protocol</span></span>

<span data-ttu-id="4fc3e-104">El protocolo WS-Management fue desarrollado por un grupo de fabricantes de hardware y software como estándar público para el intercambio remoto de datos de administración con cualquier equipo que implemente dicho protocolo.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="4fc3e-105">Estándares</span><span class="sxs-lookup"><span data-stu-id="4fc3e-105">Standards</span></span>

<span data-ttu-id="4fc3e-106">Para obtener más información sobre el protocolo de WS-Management, consulte [especificación de servicios web para administración (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="4fc3e-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="4fc3e-107">La intención del protocolo es proporcionar coherencia e interoperabilidad para las operaciones de administración en muchos tipos de dispositivos (incluido el firmware) y sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="4fc3e-108">WS-Management Protocolo se puede extender a medida que el sector de ti identifica nuevas operaciones.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="4fc3e-109">La implementación actual del Protocolo de WS-Management se basa en las siguientes especificaciones estándar: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration y WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="4fc3e-110">Para obtener más información acerca de los estándares de WS-Management y los esquemas XML, vea. <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="4fc3e-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="4fc3e-111">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="4fc3e-111">Messages</span></span>

<span data-ttu-id="4fc3e-112">El protocolo WS-Management proporciona un estándar para construir [*mensajes*](windows-remote-management-glossary.md) XML mediante varios estándares de servicios Web, como [*WS-Addressing*](windows-remote-management-glossary.md) y [*WS-Transfer*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4fc3e-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="4fc3e-113">Estos estándares definen esquemas XML para los mensajes del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="4fc3e-114">Los mensajes hacen referencia a un [*recurso*](windows-remote-management-glossary.md) mediante un [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4fc3e-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="4fc3e-115">El protocolo WS-Management agrega un conjunto de definiciones para las operaciones de administración y los valores.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="4fc3e-116">Por ejemplo, WS-Transfer define las operaciones de obtención, colocación, creación y eliminación de un recurso.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="4fc3e-117">WS-Management protocolo agrega Rename, Partial get y put parcial.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="4fc3e-118">Los mensajes siguen las convenciones de [*Protocolo simple de acceso a objetos (SOAP)*](windows-remote-management-glossary.md) que usan todos los protocolos de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="4fc3e-119">En el ejemplo de código siguiente se muestra un mensaje con una operación get.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="4fc3e-120">Este ejemplo se muestra como ayuda para comprender el aspecto de los mensajes subyacentes.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="4fc3e-121">No es necesario saber cómo generar mensajes SOAP.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="4fc3e-122">Los mensajes se ensamblan mediante Administración remota de Windows cuando se ejecuta un comando con la herramienta de línea de comandos **WinRM** o se ejecuta un script escrito con la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4fc3e-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="4fc3e-123">El mensaje es una solicitud para obtener la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con una propiedad **DeviceID** de "c:" de un servidor denominado equiporemoto.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="4fc3e-124">La solicitud utiliza el transporte HTTP a través del puerto 80.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="4fc3e-125">La cuenta que envía la solicitud debe estar en el grupo de administradores local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="4fc3e-126">Los caracteres situados delante de los dos puntos al principio de cada etiqueta indican qué estándar define el elemento XML.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="4fc3e-127">Por ejemplo, ` <wsa:To>` indica que el elemento to está definido por el estándar WS-Addressing e `<s:Header>` indica el principio del contenido del encabezado de un mensaje SOAP.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="4fc3e-128">Tenga en cuenta que la mayoría del mensaje se compone de elementos XML definidos por SOAP o WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="4fc3e-129">WS-Management protocolo agrega MaxEnvelopeSize, selector y SelectorSet.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="4fc3e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fc3e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fc3e-131">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="4fc3e-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4fc3e-132">Administración remota de hardware</span><span class="sxs-lookup"><span data-stu-id="4fc3e-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 