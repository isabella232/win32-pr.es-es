---
title: Operación de servicio
description: La operación de servicio es el código y los metadatos asociados a una operación específica de un servicio.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Servicios Web de operaciones de servicio para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e7883c0988189db3d977a78615c024dc92df36
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104003300"
---
# <a name="service-operation"></a>Operación de servicio

La operación de servicio es el código y los metadatos asociados a una operación específica de un servicio.


En términos de WSDL, cada operación WSDL: Operation definida en el documento WSDL para un portType determinado es una operación de servicio.

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

Cada operación de servicio en el modelo de servicio se proporciona como una [**\_ \_ Descripción**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)de la operación de WS. La \_ Descripción de la operación WS \_ se genera mediante [wsutil.exe](web-service-compiler-tool.md).

Para cada WSDL: Operation, la herramienta genera una [**\_ \_ Descripción de operación WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)independiente.

![Diagrama que muestra cómo wsutil.exe genera un WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

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

En términos de código, cada operación de servicio tiene una función asociada. La definición de esta función es diferente para los clientes y servidores.

Las operaciones de servicio se clasifican en,

-   [Operaciones de servicio del lado cliente](client-side-service-operations.md)
-   [Operaciones de servicio del lado servidor](server-side-service-operations.md)

Esta clasificación se basa principalmente en el diseño de la firma del servidor y las implementaciones del lado cliente de las operaciones del servicio.

Vea también la [sección compatibilidad con WSDL](wsdl-support.md).

Las enumeraciones siguientes se utilizan con operaciones de servicio:

-   [**\_tipo de parámetro de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**\_motivo de \_ cancelación del servicio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**\_opción de \_ mensaje de operación de servicio WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Las siguientes estructuras se utilizan con operaciones de servicio:

-   [**\_Descripción del mensaje de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**Descripción de la \_ operación WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_Descripción del parámetro WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




