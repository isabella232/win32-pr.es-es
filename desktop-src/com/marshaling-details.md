---
title: Detalles de serialización
description: Si utiliza el cálculo de referencias estándar, COM controla todos los detalles que se describen aquí.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0fd46ee29c712c6f2b5b286df76a30f1047e6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105717317"
---
# <a name="marshaling-details"></a>Detalles de serialización

Si utiliza el cálculo de referencias estándar, COM controla todos los detalles que se describen aquí. Sin embargo, hay pocos programadores que necesitan estos detalles y para los interesados en la información subyacente. El cálculo de referencias es el proceso de empaquetar y desempaquetar parámetros para que pueda tener lugar una llamada a procedimiento remoto.

Los diferentes tipos de parámetros se serializan de maneras diferentes. Por ejemplo, la serialización de un parámetro de entero implica simplemente copiar el valor en el búfer de mensajes. (Aunque incluso en este caso simple, hay problemas como el orden de los bytes que se deben tratar en las llamadas entre equipos). Sin embargo, la serialización de una matriz es un proceso más complejo. Los miembros de la matriz se copian en un orden específico para que el otro lado pueda reconstruir la matriz exactamente. Cuando se calculan las referencias de un puntero, se copian los datos a los que apunta el puntero siguiendo reglas y convenciones para tratar con punteros anidados en estructuras. Existen funciones únicas para controlar el cálculo de referencias de cada tipo de parámetro.

Con el cálculo de referencias estándar, los proxies y códigos auxiliares son recursos de todo el sistema para la interfaz e interactúan con el canal a través de un protocolo estándar. La serialización estándar se puede usar tanto en interfaces definidas por COM estándar como en interfaces personalizadas, como se indica a continuación:

-   En el caso de la mayoría de las interfaces COM, los proxies y códigos auxiliares para el cálculo de referencias estándar son objetos de componentes en proceso que se cargan desde un archivo DLL para todo el sistema proporcionado por COM en Ole32.dll.
-   En el caso de las interfaces personalizadas, el diseñador de la interfaz genera los proxies y códigos auxiliares para la serialización estándar, normalmente con MIDL. Estos proxies y códigos auxiliares se configuran estáticamente en el registro, por lo que cualquier posible cliente puede usar la interfaz personalizada a través de los límites del proceso. Estos proxies y códigos auxiliares se cargan desde un archivo DLL que se encuentra a través del registro del sistema, mediante el identificador de interfaz (IID) de la interfaz personalizada a la que se van a calcular las referencias.
-   Una alternativa al uso de MIDL para generar servidores proxy y códigos auxiliares para las interfaces personalizadas, se puede generar una biblioteca de tipos en su lugar y el sistema proporcionado, el motor de serialización controlado de tipo-libraryâ, calculará las referencias de la interfaz.

Como alternativa a la serialización estándar, una interfaz (estándar o personalizada) puede utilizar el cálculo de referencias personalizado. Con el cálculo de referencias personalizado, un objeto implementa dinámicamente los proxies en tiempo de ejecución para cada interfaz que admite. Para cualquier interfaz determinada, el objeto puede seleccionar el cálculo de referencias estándar proporcionado por COM o el cálculo de referencias personalizado. Esta opción la realiza el objeto en función de la interfaz. Una vez que se elige la opción para una interfaz determinada, permanece en vigor durante la duración del objeto. Sin embargo, una interfaz en un objeto puede utilizar el cálculo de referencias personalizado mientras que otro utiliza la serialización estándar.

La serialización personalizada es intrínsecamente única para el objeto que la implementa. Utiliza servidores proxy implementados por el objeto y proporcionados al sistema a petición en tiempo de ejecución. Los objetos que implementan el cálculo de referencias personalizado deben implementar la interfaz [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , mientras que los objetos que admiten el cálculo de referencias estándar no lo hacen.

Si decide escribir una interfaz personalizada, debe proporcionar compatibilidad con la serialización. Normalmente, proporcionará un archivo DLL de serialización estándar para la interfaz que diseña. Puede crear el código de proxy o stub y el archivo DLL de proxy/código auxiliar, o puede crear una biblioteca de tipos que COM usará para realizar la serialización controlada por datos (con los datos de la biblioteca de tipos).

Para que un cliente realice una llamada a un método de interfaz en un objeto de otro proceso, implica la cooperación de varios componentes. El proxy estándar es un fragmento de código específico de la interfaz que reside en el espacio de proceso del cliente y prepara los parámetros de la interfaz para transmitir. Empaqueta, o calcula las referencias, de tal forma que se pueden volver a crear y comprender en el proceso de recepción. El código auxiliar estándar, también un fragmento de código específico de la interfaz, reside en el espacio de proceso del servidor e invierte el trabajo del proxy. El código auxiliar desempaqueta o no calcula las referencias de los parámetros enviados y los reenvía a la aplicación de objeto. También empaqueta la información de respuesta que se devuelve al cliente.

> [!Note]  
> Los lectores más familiarizados con RPC que COM pueden utilizarse para ver los términos stub de cliente y código auxiliar de servidor. Estos términos son análogos a proxy y código auxiliar.

 

## <a name="components-of-interprocess-communications"></a>Componentes de comunicaciones entre procesos

En el diagrama siguiente se muestra el flujo de comunicación entre los componentes implicados. En el lado del cliente del límite del proceso, la llamada al método del cliente atraviesa el proxy y, a continuación, en el canal, que forma parte de la biblioteca COM. El canal envía el búfer que contiene los parámetros de cálculo de referencias a la biblioteca en tiempo de ejecución de RPC, que lo transmite por el límite del proceso. El tiempo de ejecución de RPC y las bibliotecas COM existen en ambos lados del proceso. La distinción entre el canal y el tiempo de ejecución de RPC es una característica de esta implementación y no forma parte del modelo de programación ni del modelo conceptual para objetos de cliente/servidor COM. Los servidores COM solo ven el proxy o el código auxiliar y, indirectamente, el canal. Las implementaciones futuras pueden utilizar diferentes capas por debajo del canal o ninguna capa.

![Diagrama que muestra los flujos de Client.exe y Server.exe en cada lado del límite del proceso.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal](channel.md)
</dt> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 