---
title: Contrato
description: Un contrato de servicio incluye metadatos que definen cómo un servicio controla los mensajes del canal.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Servicios Web de contrato para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566888"
---
# <a name="contract"></a>Contrato

Un contrato de servicio incluye metadatos que definen cómo un servicio controla los mensajes del canal.


Un [**\_ \_ contrato de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) transporta los metadatos de un servicio para administrar un [ \_ mensaje de WS](ws-message.md).

![Diagrama que muestra metadatos de WS_SERVICE_CONTRACT en un mensaje a un extremo de servicio.](images/servicecontractintro.png)

Tiene una [**Descripción del \_ contrato \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) y una tabla de funciones. Una aplicación puede especificar opcionalmente [**una \_ \_ devolución de \_ \_ llamada de recepción de mensajes del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Si no se proporciona una [**\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) y una tabla de funciones, se requiere que la aplicación especifique una devolución de [**\_ \_ \_ \_ llamada de recepción de mensajes del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagrama que muestra las operaciones de servicio de agregar y restar en el contrato de servicio de ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Vea el ejemplo de [calculadora](httpcalculatorserviceexample.md) para obtener más información.

Descripción del contrato

[**WS \_ La \_ Descripción del contrato**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) son los metadatos que definen el contrato de tipo del servicio. Generado por [wsutil.exe](web-service-compiler-tool.md).

En términos de WSDL, una [**\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) se asigna a un WSDL: portType. Para cada WSDL: portType del documento WSDL se generará **una \_ \_ Descripción** independiente del contrato de WS.

Una descripción del contrato se compone de una o más [operaciones de servicio](service-operation.md). Estas operaciones se proporcionan como una matriz de [**la \_ \_ Descripción**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)de la operación de WS.

![Diagrama que muestra una WS_CONTRACT_DESCRIPTION como una matriz de WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Para obtener detalles de la conversión de WSDL: portType a [**WS \_ Contract \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , consulte la [sección salida de WSDL](wsdl-support.md).

Ejemplo: [ **\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Tabla de funciones

La tabla de funciones es una estructura de punteros de función que representa cada una de las [operaciones de servicio](service-operation.md) en el contrato de servicio. La definición de la tabla de función también se genera mediante [wsutil.exe](web-service-compiler-tool.md).

Ejemplo: tabla de funciones

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Usar la [ **\_ devolución de \_ \_ \_ llamada de recepción de mensajes del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ La \_ \_ devolución de \_ llamada de recepción de mensajes de servicio**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) tiene un rol dual mutuamente excluyente.

Si se especifica una [**\_ \_ Descripción del contrato de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) en el [**\_ \_ contrato de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract), se convierte en el controlador de mensajes predeterminado para todas las acciones que no son compatibles con la **\_ \_ Descripción del contrato de WS** especificado. De lo contrario, si no se especifica la **\_ \_ Descripción del contrato de WS** en el **\_ \_ contrato de servicio de WS** y se especifica la devolución de [**\_ \_ \_ \_ llamada de recepción de mensajes del servicio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) en el **\_ \_ contrato de servicio WS** , todos los [mensajes](ws-message.md) que llegan se pasan a esta devolución de llamada.

Para obtener más ejemplos, vea.

-   [Ejemplo de servicio sin tipo](untypedserviceexample.md)
-   [Ejemplo de servicio de calculadora](httpcalculatorserviceexample.md)
-   [Operaciones de servicio](service-operation.md)

Las siguientes devoluciones de llamada son parte del contrato:

-   [**\_devolución de \_ llamada de recepción de mensaje del servicio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_devolución de \_ llamada de stub de servicio WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Las siguientes estructuras forman parte del contrato:

-   [**\_Descripción del contrato de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_contrato de servicio de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




