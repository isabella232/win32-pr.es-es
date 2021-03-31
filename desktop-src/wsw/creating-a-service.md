---
title: Crear un servicio
description: La creación de un servicio Web se ha simplificado en gran medida en WWSAPI mediante la API del modelo de servicio y la herramienta WsUtil.exe.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903850"
---
# <a name="creating-a-service"></a>Crear un servicio

La creación de un servicio Web se ha simplificado en gran medida en WWSAPI mediante la API del [modelo de servicio](service-model-layer-overview.md) y la herramienta [WsUtil.exe](wsutil-compiler-tool.md) . El modelo de servicio proporciona una API que permite que el servicio y el cliente envíen y reciban [mensajes](message.md) a través de un [canal](channel.md) como llamadas a métodos de C. La herramienta WsUtil genera código auxiliar y encabezados para implementar el servicio.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementar un servicio de calculadora mediante WWSAPI

Mediante los orígenes generados de la herramienta [Wsutil.exe](wsutil-compiler-tool.md) , implemente el servicio mediante los pasos siguientes.

Incluya los encabezados en el origen de la aplicación.

``` syntax
#include "CalculatorProxyStub.h"
```

Implemente las operaciones de servicio. En este ejemplo, las operaciones de servicio son las funciones de suma y resta del servicio de calculadora.

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

Defina el contrato de servicio estableciendo los campos de una estructura de [**\_ \_ contrato de servicio de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .

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

 

 




