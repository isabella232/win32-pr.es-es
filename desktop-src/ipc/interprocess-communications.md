---
description: El sistema operativo Windows proporciona mecanismos para facilitar la comunicación y el uso compartido de datos entre aplicaciones. Colectivamente, las actividades habilitadas por estos mecanismos se denominan comunicaciones entre procesos (IPC).
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Comunicaciones entre procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca9789da756ae5449e77237c1140386a6f5cfd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910206"
---
# <a name="interprocess-communications"></a>Comunicaciones entre procesos

El sistema operativo Windows proporciona mecanismos para facilitar la comunicación y el uso compartido de datos entre aplicaciones. Colectivamente, las actividades habilitadas por estos mecanismos se denominan *comunicaciones entre procesos* (IPC). Algunas formas de IPC facilitan la división del trabajo entre varios procesos especializados. Otras formas de IPC facilitan la división del trabajo entre los equipos de una red.

Normalmente, las aplicaciones pueden usar IPC clasificadas como clientes o servidores. Un *cliente* es una aplicación o un proceso que solicita un servicio de otra aplicación o proceso. Un *servidor* es una aplicación o un proceso que responde a una solicitud de cliente. Muchas aplicaciones actúan como un cliente y un servidor, dependiendo de la situación. Por ejemplo, una aplicación de procesamiento de texto podría actuar como cliente al solicitar una tabla de Resumen de costos de fabricación desde una aplicación de hoja de cálculo que actúa como un servidor. La aplicación de hoja de cálculo, a su vez, puede actuar como un cliente al solicitar los niveles de inventario más recientes desde una aplicación de control de inventario automatizado.

Después de decidir que la aplicación se beneficiaría de IPC, debe decidir cuál de los métodos IPC disponibles usar. Es probable que una aplicación use varios mecanismos IPC. Las respuestas a estas preguntas determinan si una aplicación puede beneficiarse del uso de uno o varios mecanismos IPC.

-   ¿La aplicación puede comunicarse con otras aplicaciones que se ejecutan en otros equipos de una red o es suficiente para que la aplicación solo se comunique con las aplicaciones del equipo local?
-   ¿La aplicación debe poder comunicarse con aplicaciones que se ejecutan en otros equipos que pueden ejecutarse en sistemas operativos diferentes (por ejemplo, Windows de 16 bits o UNIX)?
-   ¿Debe el usuario de la aplicación elegir las otras aplicaciones con las que se comunica la aplicación, o puede que la aplicación encuentre implícitamente sus asociados cooperativos?
-   ¿La aplicación debe comunicarse con muchas aplicaciones diferentes de forma general, como permitir operaciones de cortar y pegar con cualquier otra aplicación, o si sus requisitos de comunicación se limitan a un conjunto restringido de interacciones con otras aplicaciones específicas?
-   ¿El rendimiento es un aspecto fundamental de la aplicación? Todos los mecanismos IPC incluyen una cantidad de sobrecarga.
-   ¿La aplicación debe ser una aplicación de GUI o una aplicación de consola? Algunos mecanismos IPC requieren una aplicación GUI.

Windows admite los siguientes mecanismos IPC:

-   [Portapapeles](#using-the-clipboard-for-ipc)
-   [COM](#using-com-for-ipc)
-   [Copia de datos](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Asignación de archivos](#using-a-file-mapping-for-ipc)
-   [Buzo](#using-a-mailslot-for-ipc)
-   [Pipes](#using-pipes-for-ipc) (Operaciones de canalización de .NET Framework)
-   [RPC](#using-rpc-for-ipc)
-   [Windows Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Usar el portapapeles para IPC

El portapapeles actúa como un depósito central para el uso compartido de datos entre aplicaciones. Cuando un usuario realiza una operación de cortar o copiar en una aplicación, la aplicación coloca los datos seleccionados en el portapapeles en uno o varios formatos estándar o definidos por la aplicación. Cualquier otra aplicación puede recuperar los datos del portapapeles y elegir entre los formatos disponibles que comprende. El portapapeles es un medio de intercambio de acoplamiento muy flexible, en el que las aplicaciones solo necesitan estar de acuerdo en el formato de los datos. Las aplicaciones pueden residir en el mismo equipo o en equipos diferentes de una red.

**Punto clave:** Todas las aplicaciones deben admitir el portapapeles para los formatos de datos que entienden. Por ejemplo, un editor de texto o procesador de textos debe ser capaz de generar y aceptar datos del portapapeles en formato de texto puro. Para obtener más información, vea [portapapeles](../dataxchg/clipboard.md).

## <a name="using-com-for-ipc"></a>Usar COM para IPC

Las aplicaciones que utilizan OLE administran *documentos compuestos*, es decir, documentos que se componen de datos de diferentes aplicaciones. OLE proporciona servicios que facilitan a las aplicaciones la llamada en otras aplicaciones para la edición de datos. Por ejemplo, un procesador de textos que utiliza OLE podría incrustar un gráfico de una hoja de cálculo. El usuario podría iniciar la hoja de cálculo automáticamente desde dentro del procesador de textos eligiendo el gráfico incrustado para su edición. OLE se encarga de iniciar la hoja de cálculo y presentar el gráfico para su edición. Cuando el usuario sale de la hoja de cálculo, el gráfico se actualiza en el documento original del procesador de textos. La hoja de cálculo parece ser una extensión del procesador de textos.

La base de OLE es el modelo de objetos componentes (COM). Un componente de software que usa COM puede comunicarse con una amplia variedad de componentes, incluso los que aún no se han escrito. Los componentes de interactúan como objetos y clientes. COM distribuido extiende el modelo de programación COM para que funcione a través de una red.

**Punto clave:** OLE admite documentos compuestos y permite que una aplicación incluya datos incrustados o vinculados que, cuando se eligen, inician automáticamente otra aplicación para la edición de datos. Esto permite que la aplicación sea ampliada por cualquier otra aplicación que use OLE. Los objetos COM proporcionan acceso a los datos de un objeto a través de uno o más conjuntos de funciones relacionadas, conocidas como *interfaces*. Para obtener más información, consulte COM y Servicios de objeto ActiveX.

## <a name="using-data-copy-for-ipc"></a>Uso de la copia de datos para IPC

La copia de datos permite a una aplicación enviar información a otra aplicación mediante el mensaje de [**\_ COPYDATA de WM**](../dataxchg/wm-copydata.md) . Este método requiere la cooperación entre la aplicación de envío y la aplicación receptora. La aplicación receptora debe conocer el formato de la información y poder identificar al remitente. La aplicación emisora no puede modificar la memoria a la que hacen referencia los punteros.

**Punto clave:** La copia de datos se puede usar para enviar información rápidamente a otra aplicación mediante mensajería de Windows. Para obtener más información, consulte [copia de datos](../dataxchg/data-copy.md).

## <a name="using-dde-for-ipc"></a>Usar DDE para IPC

DDE es un protocolo que permite a las aplicaciones intercambiar datos en diversos formatos. Las aplicaciones pueden utilizar DDE para intercambios de datos de un solo uso o para intercambios en curso en los que las aplicaciones se actualizan entre sí a medida que hay nuevos datos disponibles.

Los formatos de datos utilizados por DDE son los mismos que los utilizados por el portapapeles. DDE puede considerarse una extensión del mecanismo del portapapeles. El portapapeles se usa casi siempre para una respuesta única a un comando de usuario, como elegir el comando pegar en un menú. DDE también lo inicia normalmente un comando de usuario, pero a menudo sigue funcionando sin la interacción del usuario. También puede definir formatos de datos DDE personalizados para IPC de uso especial entre aplicaciones con requisitos de comunicaciones más acoplados.

Los intercambios DDE pueden producirse entre aplicaciones que se ejecutan en el mismo equipo o en equipos diferentes de una red.

**Punto clave:** DDE no es tan eficaz como las tecnologías más recientes. Sin embargo, puede seguir usando DDE si otros mecanismos IPC no son adecuados o si debe interactuar con una aplicación existente que solo admita DDE. Para obtener más información, consulte [intercambio dinámico de datos](../dataxchg/dynamic-data-exchange.md) y [intercambio dinámico de datos biblioteca de administración](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Uso de una asignación de archivos para IPC

La *asignación de archivos* permite que un proceso trate el contenido de un archivo como si fuera un bloque de memoria en el espacio de direcciones del proceso. El proceso puede utilizar operaciones de puntero simples para examinar y modificar el contenido del archivo. Cuando dos o más procesos tienen acceso a la misma asignación de archivos, cada proceso recibe un puntero a la memoria en su propio espacio de direcciones que puede usar para leer o modificar el contenido del archivo. Los procesos deben usar un objeto de sincronización, como un semáforo, para evitar daños en los datos en un entorno de multitarea.

Puede usar un caso especial de asignación de archivos para proporcionar la *memoria compartida con nombre* entre los procesos. Si especifica el archivo de intercambio del sistema al crear un objeto de asignación de archivos, el objeto de asignación de archivos se trata como un bloque de memoria compartida. Otros procesos pueden tener acceso al mismo bloque de memoria abriendo el mismo objeto de asignación de archivos.

La asignación de archivos es bastante eficaz y también proporciona atributos de seguridad compatibles con el sistema operativo que pueden ayudar a evitar daños en los datos no autorizados. La asignación de archivos solo se puede usar entre procesos en un equipo local; no se puede usar a través de una red.

**Punto clave:** La asignación de archivos es una manera eficaz de que dos o más procesos en el mismo equipo compartan datos, pero debe proporcionar sincronización entre los procesos. Para obtener más información, consulte asignación y [sincronización](/windows/desktop/Sync/synchronization)de [archivos](/windows/desktop/Memory/file-mapping) .

## <a name="using-a-mailslot-for-ipc"></a>Uso de un buzón de correo para IPC

Los procesadores de buzones proporcionan una comunicación unidireccional. Cualquier proceso que crea un buzón de correo es un *servidor de buzón*. Otros procesos, denominados *clientes de buzón de correo*, envían mensajes al servidor de buzón de correo escribiendo un mensaje en su buzón de correo. Los mensajes entrantes siempre se anexan al buzón de correo. El buzón de correo guarda los mensajes hasta que el servidor de buzón de correo los haya leído. Un proceso puede ser un servidor de buzón de correo y un cliente de buzón de correo, por lo que es posible la comunicación bidireccional mediante varios servidores de buzones.

Un cliente de buzón de correo puede enviar un mensaje a un buzón del sistema en su equipo local, a un buzón de correo en otro equipo o a todos los buzones de correo con el mismo nombre en todos los equipos de un dominio de red especificado. Los mensajes que se difunden a todos los buzones de correo en un dominio no pueden tener más de 400 bytes, mientras que los mensajes enviados a un solo buzón de correo solo están limitados por el tamaño de mensaje máximo especificado por el servidor de buzón de correo al crear el buzón de correo.

**Punto clave:** Los procesadores de mensajes ofrecen una forma sencilla de que las aplicaciones envíen y reciban mensajes cortos. También proporcionan la capacidad de difundir mensajes en todos los equipos de un dominio de red. Para obtener más información, consulte los [procesadores de buzones](mailslots.md).

## <a name="using-pipes-for-ipc"></a>Usar canalizaciones para IPC

Hay dos tipos de canalizaciones para la comunicación bidireccional: canalizaciones anónimas y canalizaciones con nombre. Las *canalizaciones anónimas* permiten que los procesos relacionados transfieran información entre sí. Normalmente, se usa una canalización anónima para redirigir la entrada o salida estándar de un proceso secundario para que pueda intercambiar datos con su proceso primario. Para intercambiar datos en ambas direcciones (operación dúplex), debe crear dos canalizaciones anónimas. El proceso primario escribe datos en una canalización mediante su identificador de escritura, mientras que el proceso secundario lee los datos de esa canalización con su identificador de lectura. Del mismo modo, el proceso secundario escribe datos en la otra canalización y el proceso primario los Lee de ella. Las canalizaciones anónimas no se pueden usar a través de una red, ni se pueden usar entre procesos no relacionados.

Las *canalizaciones con nombre* se usan para transferir datos entre procesos que no son procesos relacionados y entre procesos en equipos diferentes. Normalmente, un proceso de servidor de canalización con nombre crea una canalización con nombre con un nombre conocido o un nombre que se va a comunicar a sus clientes. Un proceso de cliente de canalización con nombre que conoce el nombre de la canalización puede abrir su otro extremo, sujeto a las restricciones de acceso especificadas por el proceso de servidor de canalización con nombre. Una vez que el servidor y el cliente se han conectado a la canalización, pueden intercambiar datos realizando operaciones de lectura y escritura en la canalización.

**Punto clave:** Las canalizaciones anónimas proporcionan una manera eficaz de redirigir la entrada o salida estándar a los procesos secundarios en el mismo equipo. Las canalizaciones con nombre proporcionan una interfaz de programación sencilla para transferir datos entre dos procesos, independientemente de que residan en el mismo equipo o a través de una red. Para obtener más información, consulte [canalizaciones](pipes.md).

## <a name="using-rpc-for-ipc"></a>Usar RPC para IPC

RPC permite que las aplicaciones llamen a funciones de forma remota. Por lo tanto, RPC hace que IPC sea tan sencillo como llamar a una función. RPC funciona entre procesos en un solo equipo o en equipos diferentes de una red.

El RPC proporcionado por Windows es compatible con el entorno de computación distribuida (DCE) de Open Software Foundation (OSF). Esto significa que las aplicaciones que usan RPC pueden comunicarse con las aplicaciones que se ejecutan con otros sistemas operativos que admiten DCE. RPC admite automáticamente la conversión de datos para tener en cuenta diferentes arquitecturas de hardware y para el orden de bytes entre entornos diferentes.

Los clientes y servidores RPC están estrechamente acoplados pero mantienen un alto rendimiento. El sistema hace un uso extensivo de RPC para facilitar una relación de cliente/servidor entre distintas partes del sistema operativo.

**Punto clave:** RPC es una interfaz de nivel de función, con compatibilidad para la conversión automática de datos y para la comunicación con otros sistemas operativos. Con RPC, puede crear aplicaciones distribuidas estrechamente acopladas y de alto rendimiento. Para obtener más información, vea [componentes de Microsoft RPC](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>Uso de Windows Sockets para IPC

Windows Sockets es una interfaz independiente del protocolo. Aprovecha las capacidades de comunicación de los protocolos subyacentes. En Windows Sockets 2, un identificador de socket se puede usar opcionalmente como un identificador de archivo con las funciones de e/s de archivo estándar.

Windows Sockets se basa en los sockets que se han usado por primera vez por la distribución de software de Berkeley (BSD). Una aplicación que usa Windows Sockets puede comunicarse con otra implementación de sockets en otros tipos de sistemas. Sin embargo, no todos los proveedores de servicios de transporte admiten todas las opciones disponibles.

**Punto clave:** Windows Sockets es una interfaz independiente del protocolo capaz de admitir las capacidades de red actuales y emergentes. Para obtener más información, consulte [Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
