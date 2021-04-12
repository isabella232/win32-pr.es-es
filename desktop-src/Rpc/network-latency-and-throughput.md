---
title: Latencia y rendimiento de la red
description: Latencia y rendimiento de red con llamada a procedimiento remoto (RPC).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269262"
---
# <a name="network-latency-and-throughput"></a>Latencia y rendimiento de la red

Tres problemas principales se refieren al uso óptimo de la red:

-   Latencia de red
-   Saturación de red
-   Implicaciones en el procesamiento de paquetes

En esta sección se presenta una tarea de programación que requiere el uso de RPC y, a continuación, se diseñan dos soluciones: una mal escrita y una escrita correctamente. A continuación, se analizan ambas soluciones y se describe su efecto en el rendimiento de la red.

Antes de hablar de las dos soluciones, en las próximas secciones se describen y aclaran los problemas de rendimiento relacionados con la red.

## <a name="network-latency"></a>Latencia de red

El ancho de banda de red y la latencia de red son términos independientes. Las redes con ancho de banda alto no garantizan una latencia baja. Por ejemplo, una ruta de acceso de red que atraviesa un vínculo satélite suele tener una latencia elevada, aunque el rendimiento sea muy alto. No es raro que un recorrido de ida y vuelta de red que atraviesa un vínculo satélite tenga cinco o más segundos de latencia. La implicación de este retraso es: una aplicación diseñada para enviar una solicitud, esperar una respuesta, enviar otra solicitud, esperar otra respuesta, etc., esperará al menos cinco segundos para cada intercambio de paquetes, independientemente de la velocidad del servidor. A pesar del aumento de la velocidad de los equipos, las transmisiones de satélite y los medios de red se basan en la velocidad de la luz, que normalmente permanece constante. Como tal, es poco probable que se produzcan mejoras en la latencia de las redes satélite existentes.

## <a name="network-saturation"></a>Saturación de red

En muchas redes se produce alguna saturación. Las redes más fáciles de saturar son vínculos de módem lentos, como los módems analógicos estándar 56K. Sin embargo, también se pueden saturar los vínculos Ethernet con muchos equipos en un único segmento. Lo mismo se aplica a las redes de área extensa con un vínculo de bajo ancho de banda o sobrecargado, como un enrutador o conmutador que puede controlar una cantidad limitada de tráfico. En estos casos, si la red envía más paquetes de los que puede controlar su vínculo más débil, quita los paquetes. Para evitar congestiones, la pila TCP de Windows se escala de nuevo cuando se detectan paquetes que pueden producir retrasos significativos.

## <a name="packet-processing-implications"></a>Implicaciones en el procesamiento de paquetes

Cuando se desarrollan programas para entornos de nivel superior como RPC, COM e incluso Windows Sockets, los desarrolladores suelen olvidar la cantidad de trabajo que tiene lugar en segundo plano para cada paquete enviado o recibido. Cuando llega un paquete desde la red, el equipo presta una interrupción de la tarjeta de red. Después, una llamada a procedimiento diferida (DPC) se pone en cola y debe hacerlo a través de los controladores. Si se utiliza cualquier forma de seguridad, es posible que el paquete tenga que descifrarse o que se haya comprobado el hash criptográfico. También se debe realizar una serie de comprobaciones de validez en cada Estado. Solo entonces el paquete llega al destino final: el código del servidor. El envío de muchos fragmentos pequeños de datos produce una sobrecarga de procesamiento de paquetes para cada pequeño fragmento de datos. El envío de un gran fragmento de datos tiende a consumir un tiempo de CPU significativamente menor en todo el sistema, aunque el costo de ejecución de muchos fragmentos pequeños en comparación con un fragmento grande puede ser el mismo para la aplicación de servidor.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Ejemplo 1: un servidor RPC mal diseñado

Imagine una aplicación que debe tener acceso a archivos remotos y que la tarea a mano es diseñar una interfaz RPC para manipular el archivo remoto. La solución más sencilla consiste en reflejar las rutinas de archivo de Studio para archivos locales. Si lo hace, puede producirse una interfaz limpia y familiar de forma engañosa. Este es un archivo. idl abreviado:

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

Parece bastante elegante, pero en realidad, se trata de una receta respetada en el tiempo para el desastre en el rendimiento. Al contrario que la opinión popular, la llamada a procedimiento remoto no es simplemente una llamada a procedimiento local con una conexión entre el llamador y el destinatario.

Para ver cómo se comporta el rendimiento de esta receta, considere la posibilidad de usar un archivo de 2 k, donde 20 bytes se leen desde el principio y, después, 20 bytes desde el final, y vea cómo funciona esto. En el lado del cliente, se realizan las siguientes llamadas (muchas rutas de acceso de código se omiten por motivos de brevedad):

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Ahora Imagine que el servidor está separado del cliente por un vínculo satélite con un tiempo de ida y vuelta de cinco segundos. Cada una de esas llamadas debe esperar una respuesta para poder continuar, lo que significa un mínimo absoluto para ejecutar esta secuencia de 25 segundos. Teniendo en cuenta que solo se están recuperando 40 bytes, se trata de un rendimiento outrageously lento. Los clientes de esta aplicación serían Furious.

Ahora Imagine que la red está saturada, porque la capacidad de un enrutador en algún lugar de la ruta de acceso de red es sobrecargada. Este diseño obliga al enrutador a administrar al menos 10 paquetes si no tenemos seguridad (una para cada solicitud y otra para cada respuesta). Eso también no es bueno.

Este diseño también obliga al servidor a recibir cinco paquetes y enviar cinco paquetes. De nuevo, no es una implementación muy buena.

## <a name="example-2-a-better-designed-rpc-server"></a>Ejemplo 2: un servidor RPC mejor diseñado

Vamos a rediseñar la interfaz descrita en el ejemplo 1 y ver si podemos mejorarla. Es importante tener en cuenta que el hecho de que este servidor sea realmente bueno requiere conocer el patrón de uso de los archivos especificados: este tipo de conocimiento no se presupone en este ejemplo. Por lo tanto, se trata de un servidor RPC mejor diseñado, pero no un servidor RPC diseñado de forma óptima.

La idea de este ejemplo es contraer tantas operaciones remotas en una operación como sea posible. El primer intento es el siguiente:

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

En este ejemplo se contraen todas las operaciones de lectura y escritura, lo que permite abrir un opcional en la misma operación, así como un cierre y una búsqueda opcionales.

Esta misma secuencia de operación, cuando se escribe de forma abreviada, tiene el siguiente aspecto:

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Al considerar el mejor servidor RPC diseñado, en la segunda llamada el servidor comprueba que el *\_ nombre de archivo* es **null** y usa el archivo abierto almacenado en RFP. Después, verá que hay instrucciones de búsqueda y colocará el puntero de archivo 20 bytes antes del final antes de que se lea. Cuando haya terminado, reconocerá que la marca **CloseWhenDone** está establecida en **true** y cerrará el archivo y cerrará RFP.

En la red de latencia alta, esta mejor versión tarda 10 segundos en completarse (2,5 veces más rápido) y requiere el procesamiento de solo cuatro paquetes. dos reciben del servidor y dos envían desde el servidor. El *IFS* adicional y la anulación del cálculo de referencias del servidor son insignificantes en comparación con todo lo demás.

Si la ordenación causal se especifica correctamente, la interfaz se puede hacer incluso asincrónica y las dos llamadas se pueden enviar en paralelo. Cuando se utilizan las llamadas de ordenación causal, se siguen enviando en orden, lo que significa que en la red de alta latencia solo se aplica un retraso de cinco segundos, aunque el número de paquetes enviados y recibidos sea el mismo.

Podemos contraer esto aún más mediante la creación de un método que toma una matriz de estructuras, cada miembro de la matriz que describe una operación de archivo determinada. una variación remota de e/s de dispersión y recopilación. El enfoque se paga siempre que el resultado de cada operación no requiera más procesamiento en el cliente. en otras palabras, la aplicación va a leer los 20 bytes al final, independientemente de lo que sean los primeros 20 bytes leídos.

Sin embargo, si se debe realizar algún procesamiento en los primeros 20 bytes después de leerlos para determinar la operación siguiente, el contracción de todo en una operación no funciona (al menos no en todos los casos). La elegancia de RPC es que una aplicación puede tener ambos métodos en la interfaz y llamar a cualquier método en función de las necesidades.

En general, cuando la red está implicada, es mejor combinar tantas llamadas en una sola llamada como sea posible. Si una aplicación tiene dos actividades independientes, use operaciones asincrónicas y permita que se ejecuten en paralelo. En esencia, mantenga la canalización completa.

 

 




