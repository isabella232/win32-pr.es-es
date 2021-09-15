---
title: Crear un servicio
description: La creación de un servicio web se simplifica en gran medida en WWSAPI mediante service model API y la WsUtil.exe web.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570113"
---
# <a name="creating-a-service"></a>Crear un servicio

La creación de un servicio web se simplifica en gran medida en WWSAPI mediante [service model](service-model-layer-overview.md) API y la [WsUtil.exe](wsutil-compiler-tool.md) web. El modelo de servicio proporciona una API que permite al servicio y al cliente enviar y recibir [mensajes](message.md) a través de un [canal](channel.md) a medida que llama al método C. La herramienta WsUtil genera códigos auxiliares y encabezados para implementar el servicio.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementación de un servicio de calculadora mediante WWSAPI

Con los orígenes generados de [ laWsutil.exe, ](wsutil-compiler-tool.md) implemente el servicio mediante los pasos siguientes.

Incluya los encabezados en el origen de la aplicación.

``` syntax
#include "CalculatorProxyStub.h"
```

Implemente las operaciones de servicio. En este ejemplo, las operaciones de servicio son las funciones Agregar y Restar del servicio de calculadora.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Defina el contrato de servicio estableciendo los campos de una [**estructura WS \_ SERVICE \_ CONTRACT.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

Ahora, cree un host de servicio y ábralo para la comunicación.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Consulte el ejemplo de código en [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) para obtener una implementación completa del servicio de calculadora.

 

 




