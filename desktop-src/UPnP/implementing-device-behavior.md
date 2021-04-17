---
title: Implementar el comportamiento del dispositivo
description: El comportamiento de un dispositivo se define mediante los servicios que expone.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105653133"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="406ec-103">Implementar el comportamiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="406ec-103">Implementing Device Behavior</span></span>

<span data-ttu-id="406ec-104">El comportamiento de un dispositivo se define mediante los servicios que expone.</span><span class="sxs-lookup"><span data-stu-id="406ec-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="406ec-105">Cada servicio tiene una descripción del servicio que enumera sus acciones y variables de estado.</span><span class="sxs-lookup"><span data-stu-id="406ec-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="406ec-106">En conjunto, estas descripciones de servicio componen la interfaz de servicio, que define la forma en que un punto de control puede interactuar con un servicio.</span><span class="sxs-lookup"><span data-stu-id="406ec-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="406ec-107">Cada servicio debe tener al menos una acción.</span><span class="sxs-lookup"><span data-stu-id="406ec-107">Each service must have at least one action.</span></span>

<span data-ttu-id="406ec-108">Para implementar un servicio, un dispositivo hospedado debe proporcionar un objeto de modelo de objetos componentes (COM) que exponga la interfaz para el servicio.</span><span class="sxs-lookup"><span data-stu-id="406ec-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="406ec-109">En la descripción del servicio, las interfaces de servicio se especifican en el lenguaje de plantilla UPnP (UTL). sin embargo, las interfaces de objeto COM normalmente se especifican en el lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="406ec-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="406ec-110">También puede especificar la interfaz COM en una biblioteca de tipos o un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="406ec-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="406ec-111">El kit de desarrollo de software (SDK) de la plataforma incluye la herramienta Utl2idl, que traduce una descripción del servicio en UTL a una interfaz COM en IDL.</span><span class="sxs-lookup"><span data-stu-id="406ec-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="406ec-112">Los ejemplos siguientes ilustran este proceso de conversión.</span><span class="sxs-lookup"><span data-stu-id="406ec-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="406ec-113">El desarrollador del dispositivo proporciona la descripción del servicio y se escribe en UTL.</span><span class="sxs-lookup"><span data-stu-id="406ec-113">The service description is provided by the device developer and is written in UTL.</span></span>

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

<span data-ttu-id="406ec-114">El siguiente paso consiste en ejecutar la herramienta Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="406ec-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="406ec-115">Genera el archivo IDL que contiene la interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="406ec-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="406ec-116">Para obtener más información sobre los archivos IDL y la palabra clave **interface** , vea archivo e [**interfaz**](/windows/desktop/Midl/interface) de [definición de interfaz (IDL)](/windows/desktop/Midl/interface-definition-idl-file) en la referencia de MIDL.</span><span class="sxs-lookup"><span data-stu-id="406ec-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> <span data-ttu-id="406ec-117">El valor devuelto es el \[ primer \] parámetro out en la lista de argumentos de la descripción de servicio; sin embargo, aparece como el último parámetro después de la conversión.</span><span class="sxs-lookup"><span data-stu-id="406ec-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="406ec-118">Todos los demás parámetros permanecen en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="406ec-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="406ec-119">Para proporcionar la funcionalidad del servicio, implemente esta interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="406ec-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="406ec-120">Obtener información sobre un punto de conexión</span><span class="sxs-lookup"><span data-stu-id="406ec-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="406ec-121">En el entorno UPnP, la información de extremo incluye información sobre una solicitud y su origen.</span><span class="sxs-lookup"><span data-stu-id="406ec-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="406ec-122">Un dispositivo puede examinar esta información para tomar una decisión sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="406ec-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="406ec-123">Opcionalmente, la información de extremo está disponible para el servicio implementado.</span><span class="sxs-lookup"><span data-stu-id="406ec-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="406ec-124">El host del dispositivo tiene acceso a la información del punto de conexión; sin embargo, el host de dispositivo no comunica la información al servicio implementado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="406ec-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="406ec-125">Puede habilitar el host del dispositivo para compartir la información del punto de conexión con el servicio implementado mediante la modificación de la interfaz COM en el archivo IDL (generado por la herramienta Utl2idl).</span><span class="sxs-lookup"><span data-stu-id="406ec-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="406ec-126">Puede Agregar un \[ parámetro in \] a cada método que requiera información de extremo.</span><span class="sxs-lookup"><span data-stu-id="406ec-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="406ec-127">El \[ parámetro in adicional \] debe ser el primero de la lista de argumentos, un puntero a una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y denominado explícitamente **punkRemoteEndpointInfo**.</span><span class="sxs-lookup"><span data-stu-id="406ec-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="406ec-128">No se requieren modificaciones en el XML del servicio o se recomienda.</span><span class="sxs-lookup"><span data-stu-id="406ec-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="406ec-129">En el ejemplo siguiente se muestra la nueva definición del método **PowerOn** cuando se modifica para que reciba la información del punto de conexión:</span><span class="sxs-lookup"><span data-stu-id="406ec-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="406ec-130">"HRESULT PowerOn ( \[ en \] IUnknown \* punkRemoteEndpointInfo);"</span><span class="sxs-lookup"><span data-stu-id="406ec-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="406ec-131">El host del dispositivo pasa a través de este nuevo parámetro un puntero a un objeto de información de punto de conexión, una interfaz [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="406ec-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="406ec-132">La interfaz **IUPnPRemoteEndpointInfo** proporciona tres métodos para tener acceso a la información del extremo.</span><span class="sxs-lookup"><span data-stu-id="406ec-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="406ec-133">Debe llamar al método adecuado para obtener la información de punto de conexión necesaria para la implementación del servicio.</span><span class="sxs-lookup"><span data-stu-id="406ec-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="406ec-134">Como alternativa a la modificación manual de la interfaz COM, puede usar la herramienta Utl2idl con el modificador **-CI** .</span><span class="sxs-lookup"><span data-stu-id="406ec-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="406ec-135">Este modificador hace que la herramienta agregue el parámetro de información de extremo a cada uno de los métodos de la interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="406ec-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="406ec-136">El uso del modificador **-CI** no facilita la modificación de métodos individuales.</span><span class="sxs-lookup"><span data-stu-id="406ec-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="406ec-137">Si la información de extremo no es necesaria para todos los métodos de una interfaz, debe agregar el parámetro manualmente para generar las implementaciones más eficaces.</span><span class="sxs-lookup"><span data-stu-id="406ec-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="406ec-138">Implementación de un objeto de servicio</span><span class="sxs-lookup"><span data-stu-id="406ec-138">Implementing a Service Object</span></span>

<span data-ttu-id="406ec-139">Debe usar la herramienta Utl2idl para traducir cada descripción de servicio de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="406ec-140">Un objeto que proporciona la funcionalidad para un servicio se conoce como objeto de [*servicio*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="406ec-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="406ec-141">Además de proporcionar la funcionalidad de servicio, los objetos de servicio controlan los errores mediante la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="406ec-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="406ec-142">Para obtener más información, consulte [uso de la API de host de dispositivo con tecnología UPnP](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="406ec-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="406ec-143">Para garantizar la compatibilidad con Visual Basic, que no admite \[ parámetros de salida \] , los parámetros **/Direction** de **Dirección** de la descripción del servicio se convierten en \[ parámetros in y out \] en IDL.</span><span class="sxs-lookup"><span data-stu-id="406ec-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="406ec-144">El servidor debe liberar estos \[ parámetros in y out \] .</span><span class="sxs-lookup"><span data-stu-id="406ec-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="406ec-145">Implementación de un objeto de control de dispositivo</span><span class="sxs-lookup"><span data-stu-id="406ec-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="406ec-146">Además de implementar objetos de servicio, debe implementar un [*objeto de control de dispositivo*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="406ec-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="406ec-147">Un objeto de control de dispositivo es el punto central de administración y control de los objetos de servicio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="406ec-148">En el momento del registro, el objeto de control de dispositivo se pasa al host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="406ec-149">Cuando llega una suscripción de evento o una solicitud de control para uno de los servicios del dispositivo, el host del dispositivo llama a este objeto de control de dispositivo para obtener el objeto de servicio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="406ec-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="406ec-150">En ese momento, el objeto de control de dispositivo crea una instancia del objeto de servicio o devuelve la interfaz de una instancia existente del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="406ec-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="406ec-151">Puede registrar la descripción de un dispositivo en varios equipos o varias veces en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="406ec-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="406ec-152">Dado que el nombre de dispositivo único (UDN) debe ser diferente para cada instancia del dispositivo, el host de dispositivo genera un UDN único para cada dispositivo y dispositivo incrustado cada vez que se registra el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="406ec-153">Use el UDN especificado en la plantilla de Descripción del dispositivo para obtener los UDN reales generados por el host del dispositivo y asociados con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="406ec-154">Para anular el registro de un dispositivo, debe usar el identificador proporcionado por el entorno UPnP cuando se registró el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="406ec-155">Los objetos de control de dispositivo deben implementar la interfaz [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="406ec-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="406ec-156">El host del dispositivo invoca el método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo, pasando la descripción del dispositivo basado en UPnP que el dispositivo ha publicado previamente para el dispositivo y una cadena de inicialización que se especificó en el momento del registro (consulte [registro de un dispositivo hospedado con el host del dispositivo](registering-a-hosted-device-with-the-device-host.md)).</span><span class="sxs-lookup"><span data-stu-id="406ec-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="406ec-157">En esta descripción del dispositivo, el objeto de control de dispositivo lee el UDNs asignado a cada uno de los dispositivos en el árbol de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="406ec-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="406ec-158">También puede usar el método [**IUPnPRegistrar:: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) para obtener esta información.</span><span class="sxs-lookup"><span data-stu-id="406ec-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="406ec-159">Cuando el host del dispositivo requiere un puntero a un objeto de servicio que implementa un servicio determinado, invoca el método [**IUPnPDeviceControl:: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) en el objeto de control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="406ec-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="406ec-160">El host del dispositivo pasa el UDN y el identificador de servicio del servicio para el que está solicitando un objeto de servicio y la dirección de un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en el que se espera que el método devuelva un puntero al objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="406ec-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="406ec-161">El parámetro UDN es necesario porque el objeto de control de dispositivo administra los servicios para todo el árbol de dispositivos, incluidos los dispositivos anidados.</span><span class="sxs-lookup"><span data-stu-id="406ec-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="406ec-162">Si el host del dispositivo solicita un dispositivo anidado, **GetServiceObject** usa UDN para identificarlo.</span><span class="sxs-lookup"><span data-stu-id="406ec-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 