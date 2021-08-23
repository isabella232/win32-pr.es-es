---
title: Operación de servicio
description: La operación de servicio es el código y los metadatos asociados a una operación específica de un servicio.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Servicios web de operación de servicio para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acde0c2151dea483a3e82f45c7031fa201614076f7a5ea624926fbe08e7588b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026273"
---
# <a name="service-operation"></a>Operación de servicio

La operación de servicio es el código y los metadatos asociados a una operación específica de un servicio.


En términos de WSDL, cada wsdl:operation definido en el documento WSDL para un portType determinado es una operación de servicio.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Cada operación de servicio dentro del modelo de servicio se proporciona como [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). WS \_ OPERATION DESCRIPTION se genera mediante \_ [wsutil.exe](web-service-compiler-tool.md).

Para cada wsdl:operation, la herramienta genera una descripción [**independiente de la operación de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagrama que muestra wsutil.exe genera una WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

En términos de código, cada operación de servicio tiene una función asociada. La definición de esta función es diferente para el cliente y los servidores.

Las operaciones de servicio se clasifican en,

-   [Operaciones de servicio del lado cliente](client-side-service-operations.md)
-   [Operaciones de servicio del lado servidor](server-side-service-operations.md)

Esta clasificación se basa principalmente en el diseño de firma del servidor y las implementaciones del lado cliente de las operaciones de servicio.

Consulte también la [sección compatibilidad con WSDL](wsdl-support.md).

Las enumeraciones siguientes se usan con operaciones de servicio:

-   [**WS \_ PARAMETER \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**MOTIVO DE \_ CANCELACIÓN \_ DEL SERVICIO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**WS \_ SERVICE \_ OPERATION \_ MESSAGE \_ OPTION**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Las estructuras siguientes se usan con operaciones de servicio:

-   [**DESCRIPCIÓN DEL MENSAJE DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**DESCRIPCIÓN DE LA \_ OPERACIÓN WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**DESCRIPCIÓN DEL PARÁMETRO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




