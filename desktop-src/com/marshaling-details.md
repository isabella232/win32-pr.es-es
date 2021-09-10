---
title: Detalles de serialización
description: Si usa la serialización estándar, COM controla todos los detalles que se describen aquí.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0fd46ee29c712c6f2b5b286df76a30f1047e6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369436"
---
# <a name="marshaling-details"></a>Detalles de serialización

Si usa la serialización estándar, COM controla todos los detalles que se describen aquí. Sin embargo, hay pocos programadores que necesitan estos detalles y para los interesados en la información subyacente. La serialización es el proceso de empaquetar y desempaquetar parámetros para que se pueda realizar una llamada a procedimiento remoto.

Los distintos tipos de parámetros se serializan de maneras diferentes. Por ejemplo, serializar un parámetro entero implica simplemente copiar el valor en el búfer del mensaje. (Aunque incluso en este caso simple, hay problemas como la ordenación de bytes para tratar en llamadas entre equipos). Sin embargo, calcular las referencias de una matriz es un proceso más complejo. Los miembros de la matriz se copian en un orden específico para que el otro lado pueda reconstruir la matriz exactamente. Cuando se serializa un puntero, los datos a los que apunta el puntero se copian siguiendo las reglas y convenciones para tratar con punteros anidados en estructuras. Existen funciones únicas para controlar la serialización de cada tipo de parámetro.

Con la serialización estándar, los servidores proxy y los códigos auxiliares son recursos de todo el sistema para la interfaz e interactúan con el canal a través de un protocolo estándar. La serialización estándar se puede usar tanto en interfaces estándar definidas por COM como en interfaces personalizadas, como se muestra a continuación:

-   En el caso de la mayoría de las interfaces COM, los servidores proxy y los códigos auxiliares para la serialización estándar son objetos de componentes en proceso que se cargan desde un archivo DLL de todo el sistema proporcionado por COM en Ole32.dll.
-   En el caso de las interfaces personalizadas, el diseñador de interfaces genera los servidores proxy y los códigos auxiliares para la serialización estándar, normalmente con MIDL. Estos servidores proxy y código auxiliar se configuran estáticamente en el Registro, por lo que cualquier cliente potencial puede usar la interfaz personalizada a través de los límites del proceso. Estos servidores proxy y código auxiliar se cargan desde un archivo DLL que se encuentra a través del registro del sistema, mediante el identificador de interfaz (IID) para la interfaz personalizada que serializan.
-   Una alternativa al uso de MIDL para generar servidores proxy y código auxiliar para interfaces personalizadas, se puede generar una biblioteca de tipos en su lugar y el motor de serialización controlado por biblioteca de tipos proporcionado por el sistema serializará la interfaz.

Como alternativa a la serialización estándar, una interfaz (estándar o personalizada) puede usar la serialización personalizada. Con la serialización personalizada, un objeto implementa dinámicamente los servidores proxy en tiempo de ejecución para cada interfaz que admite. Para cualquier interfaz determinada, el objeto puede seleccionar serialización estándar proporcionada por COM o serialización personalizada. Esta opción la realiza el objeto en función de la interfaz por interfaz. Una vez que se elige para una interfaz determinada, permanece en vigor durante la duración del objeto. Sin embargo, una interfaz de un objeto puede usar la serialización personalizada, mientras que otra usa la serialización estándar.

La serialización personalizada es intrínsecamente única para el objeto que la implementa. Usa servidores proxy implementados por el objeto y proporcionados al sistema a petición en tiempo de ejecución. Los objetos que implementan la serialización personalizada deben implementar la [**interfaz IMarshal,**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) mientras que los objetos que admiten la serialización estándar no lo hacen.

Si decide escribir una interfaz personalizada, debe proporcionar compatibilidad con la serialización para ella. Normalmente, proporcionará un archivo DLL de serialización estándar para la interfaz que diseñe. Puede crear el código proxy/stub y el archivo DLL de proxy/stub, o puede crear una biblioteca de tipos que COM usará para realizar cálculos de referencias controlados por datos (mediante los datos de la biblioteca de tipos).

Para que un cliente realice una llamada a un método de interfaz en un objeto de otro proceso implica la cooperación de varios componentes. El proxy estándar es un fragmento de código específico de la interfaz que reside en el espacio de proceso del cliente y prepara los parámetros de interfaz para la transmisión. Empaqueta, o serializa, de forma que se puedan volver a crear y comprender en el proceso de recepción. El código auxiliar estándar, también un fragmento de código específico de la interfaz, reside en el espacio de proceso del servidor y invierte el trabajo del proxy. El código auxiliar desempaquete o desmarque los parámetros enviados y los reenvía a la aplicación de objeto. También empaqueta la información de respuesta para devolverla al cliente.

> [!Note]  
> Los lectores más familiarizados con RPC que COM pueden usarse para ver los términos código auxiliar de cliente y código auxiliar del servidor. Estos términos son análogos al proxy y el código auxiliar.

 

## <a name="components-of-interprocess-communications"></a>Componentes de las comunicaciones entre procesos

En el diagrama siguiente se muestra el flujo de comunicación entre los componentes implicados. En el lado cliente del límite del proceso, la llamada al método del cliente pasa a través del proxy y, a continuación, al canal, que forma parte de la biblioteca COM. El canal envía el búfer que contiene los parámetros serializados a la biblioteca en tiempo de ejecución de RPC, que lo transmite a través del límite del proceso. El tiempo de ejecución de RPC y las bibliotecas COM existen en ambos lados del proceso. La distinción entre el canal y el tiempo de ejecución de RPC es una característica de esta implementación y no forma parte del modelo de programación ni del modelo conceptual para objetos de cliente/servidor COM. Los servidores COM solo ven el proxy o el código auxiliar y, indirectamente, el canal. Las implementaciones futuras pueden usar capas diferentes debajo del canal o ninguna capa.

![Diagrama que muestra los flujos Client.exe y Server.exe en cada lado para el límite de proceso.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

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

 

 