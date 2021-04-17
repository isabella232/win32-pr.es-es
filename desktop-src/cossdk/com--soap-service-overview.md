---
description: 'Uso de equipos con revolución HTTP: permite a los usuarios usar un explorador Web para facilitar el acceso a la información de un servidor remoto a través de una red.'
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Introducción al servicio SOAP de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666189"
---
# <a name="com-soap-service-overview"></a>Introducción al servicio SOAP de COM+

Uso de equipos con revolución HTTP: permite a los usuarios usar un explorador Web para facilitar el acceso a la información de un servidor remoto a través de una red. Los servicios Web XML ahora han revolucionado el desarrollo de aplicaciones, ya que permiten a las aplicaciones cliente llamar fácilmente a métodos remotos a través de una red.

A menudo resulta útil que una aplicación cliente pueda llamar a un método implementado en un servidor remoto. A veces, el método usa la información volátil almacenada en el servidor remoto (por ejemplo, un método que devuelve el precio actual de las acciones correspondientes a un símbolo de indicador determinado). En otras ocasiones, el desarrollador desea tener la capacidad de actualizar la implementación de los métodos sin tener que volver a implementar todas las aplicaciones que lo usan.

Al igual que las páginas web, se tiene acceso a los servicios Web XML a través de un servidor Web, como IIS, mediante HTTP. Sin embargo, en lugar de las páginas web codificadas en HTML, estos paquetes HTTP contienen los parámetros de entrada y salida de las llamadas a un método implementado en el servidor, codificados en SOAP.

Para usar un servicio Web XML, debe conocer la dirección URL en la que se expone el servicio y el nombre del método al que desea llamar, y debe proporcionar los parámetros de entrada al método. [El estándar SOAP 1,1](https://www.w3.org/TR/SOAP/) proporciona el siguiente ejemplo de un paquete http que contiene una llamada remota a un servicio Web XML en https://www.stockquoteserver.com/StockQuote , que devuelve el precio actual de las acciones correspondientes a un símbolo de indicador determinado.

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

Como se muestra en el ejemplo anterior, SOAP es una instancia de XML que se puede incrustar en una solicitud HTTP. Del mismo modo, el resultado se devuelve como un paquete HTTP con una carga de SOAP, tal y como se muestra en el ejemplo siguiente.

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

Aunque es útil conocer la infraestructura que subyace a los servicios Web XML, COM+ facilita la creación y el uso de servicios Web XML que no suele tener que profundizar en este nivel.

Puede exponer los métodos de las interfaces predeterminadas de los componentes COM configurados en cualquier aplicación COM+ como un servicio Web XML. No es necesario tener en cuenta ninguna consideración de programación especial al escribir los componentes de, salvo que los métodos que desea exponer deben estar en la interfaz predeterminada y el componente debe estar configurado (en el catálogo de COM+ del servidor). No es necesario escribir código para comunicarse a través de una interfaz de red o para analizar SOAP. Para obtener instrucciones detalladas acerca del uso del servicio SOAP de COM+ para crear un servicio Web XML, vea [crear servicios Web XML](creating-xml-web-services.md).

Al exponer una aplicación COM+ como un servicio Web XML, se publica automáticamente información detallada acerca de la sintaxis de todos los métodos disponibles en un servicio Web XML mediante el lenguaje de descripción de servicios web (WSDL). Esta información la usan los clientes que usan el servicio Web XML.

COM+ proporciona dos maneras de obtener acceso y utilizar un servicio Web XML remoto, como se indica a continuación:

-   El modo *de objeto conocido* (WKO) se puede utilizar para tener acceso a cualquier servicio Web XML que publique su sintaxis mediante WSDL, incluso si ese servicio Web XML no se creó con com+ o incluso Microsoft Windows.
-   El modo *objeto activado* en el cliente (CaO) solo se puede utilizar para tener acceso a los servicios Web XML creados mediante la exposición de aplicaciones com+. El modo CAO aumenta el rendimiento mediante el uso de conexiones persistentes, una característica no admitida por el estándar SOAP actual.

Ambos métodos permiten a las aplicaciones cliente llamar a los métodos de servicios Web XML de forma remota de un modo sencillo, sin tener que escribir código para comunicarse a través de una interfaz de red o analizar SOAP. Para obtener más información sobre cómo obtener acceso a los servicios Web XML en cualquier modo, vea obtener acceso a los servicios [Web XML en modo de Cao](accessing-xml-web-services-in-cao-mode.md) y [obtener acceso a los servicios Web XML en el modo WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> COM+ solo admite la especificación SOAP-RPC, no la especificación SOAP-Document.

 

COM+ facilita el uso de servicios Web XML, ya que permite usar aplicaciones COM+ existentes como servicios Web XML en el modo de CAO de una manera completamente transparente. Si [exporta](exporting-a-soap-enabled-application.md) una aplicación com+ que se ha expuesto como un servicio Web XML desde su servidor, cualquier cliente que [importe](importing-a-soap-enabled-application.md) la aplicación puede usar de forma transparente el servicio Web XML del servidor siempre que se use la aplicación importada. Esta característica hace que la conversión de las aplicaciones COM+ existentes en servicios Web XML y la implementación de esos servicios a través de una red sea muy sencilla.

El uso de servicios Web XML tiene varias ventajas exclusivas sobre implementaciones alternativas de llamadas a procedimientos remotos (RPC), entre las que se incluyen las siguientes:

-   SOAP es una verdadera implementación de RPC multiplataforma, lo que aumenta la interoperabilidad.
-   Los servicios Web XML admiten métodos con parámetros de entrada y de salida.
-   Los servicios Web XML se ejecutan a través de HTTP, que normalmente pueden penetrar en firewalls que podrían bloquear otras implementaciones de RPC.
-   Cuando se implementa un servicio Web XML mediante COM+, el desarrollador no tiene que escribir ningún código especializado; Esta es una gran ventaja sobre los mecanismos de RPC alternativos.

> [!Note]  
> Los servicios Web XML no admiten llamadas transaccionales asincrónicas o de forma transparente. Use el servicio de [componentes en cola de com+](com--queued-components.md) cuando necesite esta funcionalidad.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad del servicio SOAP de COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



