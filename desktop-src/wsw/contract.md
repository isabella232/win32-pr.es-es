---
title: Contrato
description: Un contrato de servicio lleva metadatos que definen cómo un servicio controla los mensajes de canal.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Contrato de servicios web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69be302ace90c82b7b0db5666289cf4d312458e7283a04e2a1d892faa894ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026592"
---
# <a name="contract"></a>Contrato

Un contrato de servicio lleva metadatos que definen cómo un servicio controla los mensajes de canal.


Un [**WS \_ SERVICE CONTRACT \_ lleva**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) metadatos para que un servicio controle [un mensaje \_ de WS.](ws-message.md)

![Diagrama que muestra WS_SERVICE_CONTRACT metadatos de un mensaje a un punto de conexión de servicio.](images/servicecontractintro.png)

Tiene una descripción [**de WS \_ CONTRACT \_ y**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) una tabla de funciones. Una aplicación puede especificar opcionalmente [**WS \_ SERVICE MESSAGE \_ RECEIVE \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Si no [**se proporciona WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) y una tabla de funciones, la aplicación debe especificar [**WS SERVICE MESSAGE RECEIVE \_ \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagrama que muestra las operaciones agregar y restar servicio en el contrato de servicio ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Consulte el ejemplo [de](httpcalculatorserviceexample.md) calculadora para obtener más información.

Descripción del contrato

[**WS \_ CONTRACT \_ DESCRIPTION son**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) metadatos que definen el contrato de tipo del servicio. Generado por [wsutil.exe](web-service-compiler-tool.md).

En términos de WSDL, [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) se asigna a wsdl:portType. Para cada wsdl:portType del documento WSDL se generará una descripción de **WS \_ CONTRACT \_** independiente.

Una descripción del contrato se conste de en o más [operaciones de servicio](service-operation.md). Estas operaciones se dan como una matriz de [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

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

Function Table es una estructura de punteros de función que representa cada una de las [operaciones de servicio](service-operation.md) en el contrato de servicio. La definición de la tabla de funciones también la [ generawsutil.exe](web-service-compiler-tool.md).

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

Uso de la [ **devolución de \_ llamada RECEIVE DE WS SERVICE \_ \_ \_ MESSAGE**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ SERVICE \_ MESSAGE \_ RECEIVE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) tiene un doble rol mutuamente excluyente.

Si se especifica [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) en [**WS \_ SERVICE \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract), se convierte en el controlador de mensajes predeterminado para todas las acciones que no son compatibles con la descripción del **contrato WS \_ \_ especificado.** De lo contrario, si no se especifica **WS \_ CONTRACT \_ DESCRIPTION** en **WS \_ SERVICE \_ CONTRACT** y se especifica la [](ws-message.md) devolución de llamada [**WS \_ SERVICE \_ MESSAGE \_ \_ RECEIVE**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) en **WS SERVICE \_ \_ CONTRACT,** todos los mensajes entrantes se pasan a esta devolución de llamada.

Para obtener más ejemplos, consulte

-   [Ejemplo de servicio sin tipo](untypedserviceexample.md)
-   [Ejemplo de servicio de calculadora](httpcalculatorserviceexample.md)
-   [Operaciones de servicio](service-operation.md)

Las devoluciones de llamada siguientes forman parte del contrato:

-   [**DEVOLUCIÓN DE \_ LLAMADA DE RECEPCIÓN DE MENSAJES DEL \_ \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**DEVOLUCIÓN DE LLAMADA \_ DEL CÓDIGO AUXILIAR DEL \_ \_ SERVICIO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Las estructuras siguientes forman parte del contrato:

-   [**DESCRIPCIÓN DEL \_ CONTRATO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**CONTRATO DE \_ SERVICIO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




