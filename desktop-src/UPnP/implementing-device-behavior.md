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
# <a name="implementing-device-behavior"></a>Implementar el comportamiento del dispositivo

El comportamiento de un dispositivo se define mediante los servicios que expone. Cada servicio tiene una descripción del servicio que enumera sus acciones y variables de estado. En conjunto, estas descripciones de servicio componen la interfaz de servicio, que define la forma en que un punto de control puede interactuar con un servicio. Cada servicio debe tener al menos una acción.

Para implementar un servicio, un dispositivo hospedado debe proporcionar un objeto de modelo de objetos componentes (COM) que exponga la interfaz para el servicio. En la descripción del servicio, las interfaces de servicio se especifican en el lenguaje de plantilla UPnP (UTL). sin embargo, las interfaces de objeto COM normalmente se especifican en el lenguaje de definición de interfaz (IDL). También puede especificar la interfaz COM en una biblioteca de tipos o un archivo de encabezado. El kit de desarrollo de software (SDK) de la plataforma incluye la herramienta Utl2idl, que traduce una descripción del servicio en UTL a una interfaz COM en IDL.

Los ejemplos siguientes ilustran este proceso de conversión. El desarrollador del dispositivo proporciona la descripción del servicio y se escribe en UTL.

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

El siguiente paso consiste en ejecutar la herramienta Utl2idl. Genera el archivo IDL que contiene la interfaz COM. Para obtener más información sobre los archivos IDL y la palabra clave **interface** , vea archivo e [**interfaz**](/windows/desktop/Midl/interface) de [definición de interfaz (IDL)](/windows/desktop/Midl/interface-definition-idl-file) en la referencia de MIDL.

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
> El valor devuelto es el \[ primer \] parámetro out en la lista de argumentos de la descripción de servicio; sin embargo, aparece como el último parámetro después de la conversión.
> 
> Todos los demás parámetros permanecen en el mismo orden.

 

Para proporcionar la funcionalidad del servicio, implemente esta interfaz COM.

## <a name="obtaining-information-about-an-endpoint"></a>Obtener información sobre un punto de conexión

En el entorno UPnP, la información de extremo incluye información sobre una solicitud y su origen. Un dispositivo puede examinar esta información para tomar una decisión sobre la solicitud.

Opcionalmente, la información de extremo está disponible para el servicio implementado. El host del dispositivo tiene acceso a la información del punto de conexión; sin embargo, el host de dispositivo no comunica la información al servicio implementado de forma predeterminada. Puede habilitar el host del dispositivo para compartir la información del punto de conexión con el servicio implementado mediante la modificación de la interfaz COM en el archivo IDL (generado por la herramienta Utl2idl). Puede Agregar un \[ parámetro in \] a cada método que requiera información de extremo. El \[ parámetro in adicional \] debe ser el primero de la lista de argumentos, un puntero a una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y denominado explícitamente **punkRemoteEndpointInfo**. No se requieren modificaciones en el XML del servicio o se recomienda. En el ejemplo siguiente se muestra la nueva definición del método **PowerOn** cuando se modifica para que reciba la información del punto de conexión:

"HRESULT PowerOn ( \[ en \] IUnknown \* punkRemoteEndpointInfo);"

El host del dispositivo pasa a través de este nuevo parámetro un puntero a un objeto de información de punto de conexión, una interfaz [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) . La interfaz **IUPnPRemoteEndpointInfo** proporciona tres métodos para tener acceso a la información del extremo. Debe llamar al método adecuado para obtener la información de punto de conexión necesaria para la implementación del servicio.

Como alternativa a la modificación manual de la interfaz COM, puede usar la herramienta Utl2idl con el modificador **-CI** . Este modificador hace que la herramienta agregue el parámetro de información de extremo a cada uno de los métodos de la interfaz COM. El uso del modificador **-CI** no facilita la modificación de métodos individuales. Si la información de extremo no es necesaria para todos los métodos de una interfaz, debe agregar el parámetro manualmente para generar las implementaciones más eficaces.

## <a name="implementing-a-service-object"></a>Implementación de un objeto de servicio

Debe usar la herramienta Utl2idl para traducir cada descripción de servicio de un dispositivo.

Un objeto que proporciona la funcionalidad para un servicio se conoce como objeto de [*servicio*](s-gly.md). Además de proporcionar la funcionalidad de servicio, los objetos de servicio controlan los errores mediante la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Para obtener más información, consulte [uso de la API de host de dispositivo con tecnología UPnP](using-the-device-host-api-with-upnp-technology.md).

Para garantizar la compatibilidad con Visual Basic, que no admite \[ parámetros de salida \] , los parámetros **/Direction** de **Dirección** de la descripción del servicio se convierten en \[ parámetros in y out \] en IDL. El servidor debe liberar estos \[ parámetros in y out \] .

## <a name="implementing-a-device-control-object"></a>Implementación de un objeto de control de dispositivo

Además de implementar objetos de servicio, debe implementar un [*objeto de control de dispositivo*](d-gly.md). Un objeto de control de dispositivo es el punto central de administración y control de los objetos de servicio del dispositivo. En el momento del registro, el objeto de control de dispositivo se pasa al host del dispositivo. Cuando llega una suscripción de evento o una solicitud de control para uno de los servicios del dispositivo, el host del dispositivo llama a este objeto de control de dispositivo para obtener el objeto de servicio correspondiente. En ese momento, el objeto de control de dispositivo crea una instancia del objeto de servicio o devuelve la interfaz de una instancia existente del objeto de servicio.

Puede registrar la descripción de un dispositivo en varios equipos o varias veces en el mismo equipo. Dado que el nombre de dispositivo único (UDN) debe ser diferente para cada instancia del dispositivo, el host de dispositivo genera un UDN único para cada dispositivo y dispositivo incrustado cada vez que se registra el dispositivo. Use el UDN especificado en la plantilla de Descripción del dispositivo para obtener los UDN reales generados por el host del dispositivo y asociados con el dispositivo. Para anular el registro de un dispositivo, debe usar el identificador proporcionado por el entorno UPnP cuando se registró el dispositivo.

Los objetos de control de dispositivo deben implementar la interfaz [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) . El host del dispositivo invoca el método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) del objeto de control de dispositivo, pasando la descripción del dispositivo basado en UPnP que el dispositivo ha publicado previamente para el dispositivo y una cadena de inicialización que se especificó en el momento del registro (consulte [registro de un dispositivo hospedado con el host del dispositivo](registering-a-hosted-device-with-the-device-host.md)). En esta descripción del dispositivo, el objeto de control de dispositivo lee el UDNs asignado a cada uno de los dispositivos en el árbol de dispositivos. También puede usar el método [**IUPnPRegistrar:: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) para obtener esta información.

Cuando el host del dispositivo requiere un puntero a un objeto de servicio que implementa un servicio determinado, invoca el método [**IUPnPDeviceControl:: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) en el objeto de control de dispositivo. El host del dispositivo pasa el UDN y el identificador de servicio del servicio para el que está solicitando un objeto de servicio y la dirección de un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en el que se espera que el método devuelva un puntero al objeto de servicio. El parámetro UDN es necesario porque el objeto de control de dispositivo administra los servicios para todo el árbol de dispositivos, incluidos los dispositivos anidados. Si el host del dispositivo solicita un dispositivo anidado, **GetServiceObject** usa UDN para identificarlo.

 

 