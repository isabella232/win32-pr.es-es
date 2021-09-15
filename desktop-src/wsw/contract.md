---
title: Contrato
description: Un contrato de servicio lleva metadatos que definen cómo un servicio controla los mensajes de canal.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Servicios web de contrato para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570116"
---
# <a name="contract"></a>Contrato

Un contrato de servicio lleva metadatos que definen cómo un servicio controla los mensajes de canal.


Un [**WS \_ SERVICE CONTRACT \_ lleva**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) metadatos para que un servicio controle un [mensaje de \_ WS.](ws-message.md)

![Diagrama que muestra WS_SERVICE_CONTRACT metadatos en un mensaje a un punto de conexión de servicio.](images/servicecontractintro.png)

Tiene una descripción [**de WS \_ CONTRACT \_ y**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) una tabla de funciones. Opcionalmente, una aplicación puede especificar [**WS \_ SERVICE MESSAGE \_ RECEIVE \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Si no [**se proporciona WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) y una tabla de funciones, la aplicación debe especificar [**WS SERVICE MESSAGE RECEIVE \_ \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagrama que muestra las operaciones agregar y restar servicios en el contrato de servicio ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Consulte el [ejemplo de](httpcalculatorserviceexample.md) calculadora para obtener más información.

Descripción del contrato

[**WS \_ CONTRACT \_ DESCRIPTION son**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) metadatos que definen el contrato de tipo del servicio. Generado por [wsutil.exe](web-service-compiler-tool.md).

En términos de WSDL, [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) se asigna a wsdl:portType. Para cada wsdl:portType del documento WSDL, se generará una descripción de **WS \_ CONTRACT \_** independiente.

Una descripción del contrato se forma de en o más operaciones [de servicio](service-operation.md). Estas operaciones se dan como una matriz de [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagrama que muestra un WS_CONTRACT_DESCRIPTION como una matriz de WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

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

Para obtener más información sobre la conversión wsdl:portType a [**WS \_ CONTRACT \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) vea la [sección de salida de WSDL](wsdl-support.md).

Ejemplo: [ **WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Tabla de funciones

Function Table es una estructura de punteros de función que representa cada una de las operaciones [de servicio](service-operation.md) en el contrato de servicio. La definición de la tabla de funciones también se [ generawsutil.exe](web-service-compiler-tool.md).

Ejemplo: Tabla de funciones

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

Uso de [ **WS \_ SERVICE \_ MESSAGE RECEIVE \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ SERVICE \_ MESSAGE \_ RECEIVE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) tiene un doble rol mutuamente excluyente.

Si se especifica [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) en [**WS \_ SERVICE \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract), se convierte en el controlador de mensajes predeterminado para todas las acciones que no son compatibles con la descripción de **WS CONTRACT \_ \_ especificada.** De lo contrario, si **WS \_ CONTRACT \_ DESCRIPTION** no se especifica en **WS \_ SERVICE \_ CONTRACT** y [**WS \_ SERVICE MESSAGE RECEIVE \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) se especifica en **WS \_ SERVICE \_ CONTRACT,** todos los mensajes entrantes se pasan a esta devolución de llamada. [](ws-message.md)

Para obtener más ejemplos, consulte

-   [Ejemplo de servicio sin tipo](untypedserviceexample.md)
-   [Ejemplo de servicio de calculadora](httpcalculatorserviceexample.md)
-   [Operaciones de servicio](service-operation.md)

Las devoluciones de llamada siguientes forman parte del contrato:

-   [**DEVOLUCIÓN DE \_ LLAMADA DE RECEPCIÓN DE MENSAJES \_ \_ DEL \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DE CÓDIGO AUXILIAR DEL \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Las estructuras siguientes forman parte del contrato:

-   [**DESCRIPCIÓN DEL CONTRATO DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**CONTRATO DE SERVICIO DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




