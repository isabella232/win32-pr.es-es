---
title: Rendimiento y latencia de red
description: Latencia de red y rendimiento con llamada a procedimiento remoto (RPC).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169077"
---
# <a name="network-latency-and-throughput"></a>Rendimiento y latencia de red

Tres problemas principales están relacionados con el uso óptimo de la red:

-   Latencia de red
-   Saturación de la red
-   Implicaciones del procesamiento de paquetes

En esta sección se presenta una tarea de programación que requiere el uso de RPC y, a continuación, se diseñan dos soluciones: una mal escrita y otra bien escrita. A continuación, se examinan ambas soluciones y se analiza su efecto en el rendimiento de la red.

Antes de analizar las dos soluciones, las siguientes secciones de abordan y aclaran los problemas de rendimiento relacionados con la red.

## <a name="network-latency"></a>Latencia de red

El ancho de banda de red y la latencia de red son términos independientes. Las redes con un ancho de banda alto no garantizan una latencia baja. Por ejemplo, una ruta de acceso de red que atraviesa un vínculo satélite a menudo tiene una latencia alta, aunque el rendimiento sea muy alto. No es raro que un recorrido de ida y vuelta de red que atraviesa un vínculo satélite tenga cinco o más segundos de latencia. La implicación de este retraso es esta: una aplicación diseñada para enviar una solicitud, esperar una respuesta, enviar otra solicitud, esperar otra respuesta, y así sucesivamente, esperará al menos cinco segundos para cada intercambio de paquetes, independientemente de la rapidez con la que se encuentra el servidor. A pesar de la velocidad creciente de los equipos, las transmisiones por satélite y los medios de red se basan en la velocidad de la luz, que generalmente permanece constante. Por lo tanto, es poco probable que se produzcan mejoras en la latencia de las redes satélite existentes.

## <a name="network-saturation"></a>Saturación de red

Cierta saturación se produce en muchas redes. Las redes más fáciles de saturar son los vínculos de módem lento, como los módems análogos estándar de 56 k. Sin embargo, los vínculos Ethernet con muchos equipos de un solo segmento también pueden saturarse. Lo mismo sucede con las redes de área extensa con un vínculo de ancho de banda bajo o sobrecargado, como un enrutador o conmutador que puede controlar una cantidad limitada de tráfico. En estos casos, si la red envía más paquetes de los que puede controlar su vínculo más débil, quita los paquetes. Para evitar la congestión, Windows pila TCP se reduce cuando se detectan paquetes eliminados, lo que puede provocar retrasos significativos.

## <a name="packet-processing-implications"></a>Implicaciones del procesamiento de paquetes

Cuando los programas se desarrollan para entornos de nivel superior, como RPC, COM e incluso sockets de Windows, los desarrolladores tienden a olvidar la cantidad de trabajo que se realiza en segundo plano para cada paquete enviado o recibido. Cuando un paquete llega de la red, el equipo atiende una interrupción de la tarjeta de red. A continuación, se pone en cola una llamada a procedimiento diferido (DPC) y se debe abrir paso a través de los controladores. Si se usa cualquier forma de seguridad, es posible que tenga que descifrar el paquete o comprobar el hash criptográfico. También se deben realizar varias comprobaciones de validez en cada estado. Solo entonces el paquete llega al destino final: el código del servidor. El envío de muchos fragmentos pequeños de datos da como resultado una sobrecarga de procesamiento de paquetes por cada fragmento pequeño de datos. El envío de un gran fragmento de datos tiende a consumir mucho menos tiempo de CPU en todo el sistema, aunque el costo de ejecución de muchos fragmentos pequeños en comparación con un fragmento grande puede ser el mismo para la aplicación de servidor.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Ejemplo 1: Un servidor RPC mal diseñado

Imagine una aplicación que debe tener acceso a archivos remotos y la tarea a mano consiste en diseñar una interfaz RPC para manipular el archivo remoto. La solución más sencilla es reflejar las rutinas de archivo de Studio para los archivos locales. Si lo hace, puede dar lugar a una interfaz falsamente limpia y familiar. Este es un archivo .idl abreviado:

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

Esto parece lo suficientemente elegante, pero en realidad se trata de una receta respetada en el tiempo para el desastre de rendimiento. Al contrario de la opinión popular, la llamada a procedimiento remoto no es simplemente una llamada de procedimiento local con una conexión entre el autor de la llamada y el destinatario.

Para ver cómo funciona esta receta, considere un archivo 2K, donde se leen 20 bytes desde el principio y, a continuación, 20 bytes desde el final, y vea cómo funciona. En el lado cliente, se realizan las siguientes llamadas (muchas rutas de acceso de código se omiten por brevedad):

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Ahora imagine que el servidor está separado del cliente por un vínculo satélite con un tiempo de ida y vuelta de cinco segundos. Cada una de esas llamadas debe esperar una respuesta antes de poder continuar, lo que significa un mínimo absoluto para ejecutar esta secuencia de 25 segundos. Teniendo en cuenta que solo se recuperan 40 bytes, el rendimiento es muy lento. Los clientes de esta aplicación serían desafusos.

Ahora imagine que la red está saturada, porque la capacidad de un enrutador en algún lugar de la ruta de acceso de red está sobrecargada. Este diseño obliga al enrutador a controlar al menos 10 paquetes si no tenemos seguridad (uno para cada solicitud y otro para cada respuesta). Eso tampoco es bueno.

Este diseño también obliga al servidor a recibir cinco paquetes y enviar cinco paquetes. Una vez más, no es una implementación muy buena.

## <a name="example-2-a-better-designed-rpc-server"></a>Ejemplo 2: Un servidor RPC mejor diseñado

Vamos a rediseñar la interfaz que se describe en el ejemplo 1 y a ver si podemos mejorarla. Es importante tener en cuenta que hacer que este servidor sea realmente bueno requiere conocimiento del patrón de uso de los archivos dados: este conocimiento no se supone para este ejemplo. Por lo tanto, se trata de un servidor RPC mejor diseñado, pero no un servidor RPC diseñado de forma óptima.

La idea de este ejemplo es contraer tantas operaciones remotas como sea posible en una operación. El primer intento es el siguiente:

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

En este ejemplo se contraen todas las operaciones en una lectura y escritura, lo que permite una apertura opcional en la misma operación, así como un cierre y búsqueda opcionales.

Esta misma secuencia de operación, cuando se escribe en forma abreviada, tiene el siguiente aspecto:

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Al considerar el servidor RPC mejor diseñado, en *la \_* segunda llamada al servidor comprueba que el nombre de archivo es **NULL** y usa el archivo abierto almacenado en rfp. A continuación, ve que hay instrucciones de búsqueda y colocará el puntero de archivo 20 bytes antes del final antes de leerlo. Cuando haya terminado, reconocerá que la **marca CloseWhenDone** está establecida en **TRUE** y cerrará el archivo y cerrará rfp.

En la red de latencia alta, esta mejor versión tarda 10 segundos en completarse (2,5 veces más rápido) y requiere el procesamiento de solo cuatro paquetes. dos recibe del servidor y dos los envía desde el servidor. Los *ifs adicionales* y la desmarqueción que realiza el servidor son insignificantes en comparación con todo lo demás.

Si la ordenación causal se especifica correctamente, la interfaz incluso se puede convertir en asincrónica y las dos llamadas se pueden enviar en paralelo. Cuando se usa la ordenación causal, las llamadas se siguen distribuyendo en orden, lo que significa que en la red de latencia alta solo se mantiene un retraso de cinco segundos, aunque el número de paquetes enviados y recibidos sea el mismo.

Esto se puede contraer aún más mediante la creación de un método que toma una matriz de estructuras, cada miembro de la matriz que describe una operación de archivo determinada. una variación remota de E/S de dispersión/recopilación. El enfoque da sus resultados siempre y cuando el resultado de cada operación no requiera un procesamiento adicional en el cliente; En otras palabras, la aplicación leerá los 20 bytes al final, independientemente de cuáles sean los primeros 20 bytes leídos.

Sin embargo, si se debe realizar algún procesamiento en los primeros 20 bytes después de leerlos para determinar la siguiente operación, contraer todo en una operación no funciona (al menos no en todos los casos). La comodidad de RPC es que una aplicación puede tener ambos métodos en la interfaz y llamar a cualquiera de los métodos en función de la necesidad.

En general, cuando la red está implicada, es mejor combinar tantas llamadas en una sola llamada como sea posible. Si una aplicación tiene dos actividades independientes, use operaciones asincrónicas y deje que se ejecuten en paralelo. Básicamente, mantenga la canalización completa.

 

 




