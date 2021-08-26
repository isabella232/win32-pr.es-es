---
description: Uso de equipos con revoluciones HTTP al permitir que los usuarios usen un explorador web para facilitar el acceso a la información de un servidor remoto a través de una red.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Información general sobre el servicio SOAP de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68501d80596d8547715cb1694fe77a17a3ab4b6955ad1e1acd596f249be5f231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096875"
---
# <a name="com-soap-service-overview"></a>Información general sobre el servicio SOAP de COM+

Uso de equipos con revoluciones HTTP al permitir que los usuarios usen un explorador web para facilitar el acceso a la información de un servidor remoto a través de una red. Los servicios web XML han revolucionado el desarrollo de aplicaciones al permitir que las aplicaciones cliente llamen fácilmente a métodos remotos a través de una red.

A menudo resulta útil que una aplicación cliente pueda llamar a un método implementado en un servidor remoto. A veces, el método usa información volátil almacenada en el servidor remoto (por ejemplo, un método que devuelve el precio actual de las acciones correspondientes a un símbolo de marca de graduación determinado). En otras ocasiones, el desarrollador quiere la capacidad de actualizar la implementación de métodos sin tener que volver a implementar todas las aplicaciones que la usan.

Al igual que las páginas web, se accede a los servicios web XML a través de un servidor web, como IIS, mediante HTTP. Sin embargo, en lugar de páginas web codificadas en HTML, estos paquetes HTTP contienen los parámetros de entrada y salida de las llamadas a un método implementado en el servidor, codificados en SOAP.

Para usar un servicio web XML, debe conocer la dirección URL donde se expone el servicio y el nombre del método al que desea llamar, y debe proporcionar los parámetros de entrada al método . El estándar [SOAP 1.1](https://www.w3.org/TR/SOAP/) proporciona el ejemplo siguiente de un paquete HTTP que contiene una llamada remota a un servicio web XML en , que devuelve el precio actual de las acciones correspondientes a un símbolo de marca de graduación https://www.stockquoteserver.com/StockQuote determinado.

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Como se muestra en el ejemplo anterior, SOAP es una instancia XML que se puede incrustar en una solicitud HTTP. De forma similar, el resultado se devuelve como un paquete HTTP con una carga SOAP, como se muestra en el ejemplo siguiente.

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Aunque resulta útil tener cierto conocimiento de la infraestructura que subyace a los servicios web XML, COM+ facilita la creación y el uso de servicios web XML que a menudo no tendrá que profundizar en este nivel.

Puede exponer los métodos en las interfaces predeterminadas de los componentes COM configurados en cualquier aplicación COM+ como un servicio web XML. No se necesita ninguna consideración de programación especial al escribir los componentes, salvo que los métodos que desea exponer deben estar en la interfaz predeterminada y el componente debe configurarse (en el catálogo com+ del servidor). No es necesario escribir código para comunicarse a través de una interfaz de red ni para analizar SOAP. Para obtener instrucciones detalladas sobre el uso del servicio SOAP de COM+ para crear un servicio web XML, vea [Creating XML Web Services](creating-xml-web-services.md).

Al exponer una aplicación COM+ como un servicio web XML, se publica automáticamente información detallada sobre la sintaxis de todos los métodos disponibles en un servicio web XML mediante el Lenguaje de descripción de servicios Web (WSDL). Esta información la usan los clientes que usan el servicio web XML.

COM+ proporciona dos maneras de acceder y usar un servicio web XML remoto, como se muestra a continuación:

-   El *modo* de objeto conocido (WKO) se puede usar para acceder a cualquier servicio web XML que publique su sintaxis mediante WSDL, incluso si ese servicio web XML no se creó mediante COM+ o incluso Microsoft Windows.
-   El *modo de objeto activado por* el cliente (DHCP) solo se puede usar para acceder a los servicios web XML creados mediante la exposición de aplicaciones COM+. El modo SSL aumenta el rendimiento mediante conexiones persistentes, una característica no admitida por el estándar SOAP actual.

Ambos métodos permiten a las aplicaciones cliente llamar a los métodos de servicios web XML de forma remota de forma sencilla, sin tener que escribir código para comunicarse a través de una interfaz de red o analizar SOAP. Para obtener más información sobre cómo obtener acceso a servicios web XML en cualquiera de los dos modos, vea Acceso a servicios Web XML en modo [DESEP](accessing-xml-web-services-in-cao-mode.md) y Acceso a servicios [Web XML en modo WKO.](accessing-xml-web-services-in-wko-mode.md)

> [!Note]  
> COM+ solo admite la especificación SOAP-RPC, no SOAP-Document especificación.

 

COM+ facilita especialmente el uso de servicios web XML, ya que permite usar las aplicaciones COM+ existentes como servicios web XML en el modo DEON DE forma completamente transparente. Si [](exporting-a-soap-enabled-application.md) exporta una aplicación COM+ que se ha expuesto como un [](importing-a-soap-enabled-application.md) servicio web XML desde el servidor, cualquier cliente que importe la aplicación puede usar de forma transparente el servicio web XML del servidor siempre que se use la aplicación importada. Esta instalación facilita la conversión de aplicaciones COM+ existentes en servicios web XML y la implementación de esos servicios a través de una red.

El uso de servicios web XML tiene varias ventajas únicas con respecto a las implementaciones alternativas de llamadas a procedimiento remoto (RPC), incluidas las siguientes:

-   SOAP es una verdadera implementación de RPC multiplataforma, que aumenta la interoperabilidad.
-   Los servicios web XML admiten métodos con parámetros de entrada y salida.
-   Los servicios web XML se ejecutan a través de HTTP, que normalmente puede atravesar firewalls que podrían bloquear otras implementaciones de RPC.
-   Cuando se implementa un servicio web XML mediante COM+, el desarrollador no tiene que escribir ningún código especializado; se trata de una gran ventaja con respecto a los mecanismos de RPC alternativos.

> [!Note]  
> Los servicios web XML no admiten llamadas transaccionales asincrónicas o transparentes. Use el servicio Componentes en cola de [COM+](com--queued-components.md) cuando necesite esta funcionalidad.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad del servicio SOAP de COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



