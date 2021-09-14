---
description: El Windows operativo proporciona mecanismos para facilitar las comunicaciones y el uso compartido de datos entre aplicaciones. En conjunto, las actividades habilitadas por estos mecanismos se denominan comunicaciones entre procesos (IPC).
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Comunicaciones entre procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca9789da756ae5449e77237c1140386a6f5cfd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172325"
---
# <a name="interprocess-communications"></a>Comunicaciones entre procesos

El Windows operativo proporciona mecanismos para facilitar las comunicaciones y el uso compartido de datos entre aplicaciones. En conjunto, las actividades habilitadas por estos mecanismos se *denominan comunicaciones entre procesos* (IPC). Algunas formas de IPC facilitan la división del trabajo entre varios procesos especializados. Otras formas de IPC facilitan la división del trabajo entre equipos de una red.

Normalmente, las aplicaciones pueden usar IPC clasificado como clientes o servidores. Un *cliente* es una aplicación o un proceso que solicita un servicio de otra aplicación o proceso. Un *servidor* es una aplicación o un proceso que responde a una solicitud de cliente. Muchas aplicaciones actúan como un cliente y un servidor, en función de la situación. Por ejemplo, una aplicación de procesamiento de palabras podría actuar como cliente para solicitar una tabla de resumen de los costos de fabricación de una aplicación de hoja de cálculo que actúa como servidor. La aplicación de hoja de cálculo, a su vez, podría actuar como cliente para solicitar los niveles de inventario más recientes de una aplicación de control de inventario automatizada.

Después de decidir que la aplicación se beneficiaría de IPC, debe decidir cuáles de los métodos IPC disponibles usar. Es probable que una aplicación use varios mecanismos de IPC. Las respuestas a estas preguntas determinan si una aplicación puede beneficiarse mediante uno o varios mecanismos de IPC.

-   ¿La aplicación debe ser capaz de comunicarse con otras aplicaciones que se ejecutan en otros equipos de una red o es suficiente para que la aplicación se comunique solo con las aplicaciones del equipo local?
-   ¿La aplicación debe ser capaz de comunicarse con aplicaciones que se ejecutan en otros equipos que pueden ejecutarse en sistemas operativos diferentes (como sistemas operativos de 16 Windows o UNIX)?
-   ¿El usuario de la aplicación debe elegir las demás aplicaciones con las que se comunica la aplicación o puede encontrar implícitamente sus asociados colaboradores?
-   ¿Debe la aplicación comunicarse con muchas aplicaciones diferentes de forma general, como permitir operaciones de cortar y pegar con cualquier otra aplicación, o debe limitar sus requisitos de comunicaciones a un conjunto restringido de interacciones con otras aplicaciones específicas?
-   ¿El rendimiento es un aspecto crítico de la aplicación? Todos los mecanismos de IPC incluyen cierta sobrecarga.
-   ¿La aplicación debe ser una aplicación gui o una aplicación de consola? Algunos mecanismos de IPC requieren una aplicación gui.

Los siguientes mecanismos de IPC son compatibles con Windows:

-   [Portapapeles](#using-the-clipboard-for-ipc)
-   [COM](#using-com-for-ipc)
-   [Copia de datos](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Asignación de archivos](#using-a-file-mapping-for-ipc)
-   [Mailslots](#using-a-mailslot-for-ipc)
-   [Pipes](#using-pipes-for-ipc) (Operaciones de canalización de .NET Framework)
-   [RPC](#using-rpc-for-ipc)
-   [Windows Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Uso del Portapapeles para IPC

El Portapapeles actúa como depósito central para el uso compartido de datos entre aplicaciones. Cuando un usuario realiza una operación de cortar o copiar en una aplicación, la aplicación coloca los datos seleccionados en el Portapapeles en uno o varios formatos estándar o definidos por la aplicación. Cualquier otra aplicación puede recuperar los datos del Portapapeles, eligiendo entre los formatos disponibles que comprende. El Portapapeles es un medio de intercambio de acoplamiento flexible, donde las aplicaciones solo necesitan ponerse de acuerdo en el formato de datos. Las aplicaciones pueden residir en el mismo equipo o en equipos diferentes de una red.

**Punto clave:** Todas las aplicaciones deben admitir el Portapapeles para los formatos de datos que entiendan. Por ejemplo, un editor de texto o un procesador de texto debe ser capaz de generar y aceptar datos del Portapapeles en formato de texto puro. Para obtener más información, vea [Portapapeles.](../dataxchg/clipboard.md)

## <a name="using-com-for-ipc"></a>Uso de COM para IPC

Las aplicaciones que usan OLE *administran documentos compuestos,* es decir, documentos compuestos por datos de una variedad de aplicaciones diferentes. OLE proporciona servicios que hacen que sea fácil para las aplicaciones llamar a en otras aplicaciones para la edición de datos. Por ejemplo, un procesador de palabras que usa OLE podría insertar un gráfico desde una hoja de cálculo. El usuario podría iniciar la hoja de cálculo automáticamente desde el procesador de palabras eligiendo el gráfico incrustado para editarlo. OLE se encarga de iniciar la hoja de cálculo y presentar el gráfico para su edición. Cuando el usuario sale de la hoja de cálculo, el gráfico se actualizaría en el documento original del procesador de textos. La hoja de cálculo parece ser una extensión del procesador de palabras.

La base de OLE es el modelo de objetos componentes (COM). Un componente de software que usa COM puede comunicarse con una amplia variedad de otros componentes, incluso los que aún no se han escrito. Los componentes interactúan como objetos y clientes. COM distribuido amplía el modelo de programación COM para que funcione en una red.

**Punto clave:** OLE admite documentos compuestos y permite que una aplicación incluya datos incrustados o vinculados que, cuando se eligen, inician automáticamente otra aplicación para la edición de datos. Esto permite que cualquier otra aplicación que use OLE pueda ampliar la aplicación. Los objetos COM proporcionan acceso a los datos de un objeto a través de uno o varios conjuntos de funciones relacionadas, *conocidas como interfaces*. Para obtener más información, vea COM y ActiveX Servicios de objeto.

## <a name="using-data-copy-for-ipc"></a>Uso de la copia de datos para IPC

La copia de datos permite a una aplicación enviar información a otra aplicación mediante el [**mensaje \_ COPYDATA de WM.**](../dataxchg/wm-copydata.md) Este método requiere la cooperación entre la aplicación de envío y la aplicación receptora. La aplicación receptora debe conocer el formato de la información y poder identificar al remitente. La aplicación de envío no puede modificar la memoria a la que hace referencia ningún puntero.

**Punto clave:** La copia de datos se puede usar para enviar rápidamente información a otra aplicación mediante Windows mensajes. Para obtener más información, vea [Copia de datos.](../dataxchg/data-copy.md)

## <a name="using-dde-for-ipc"></a>Uso de DDE para IPC

DDE es un protocolo que permite a las aplicaciones intercambiar datos en diversos formatos. Las aplicaciones pueden usar DDE para intercambios de datos únicos o para intercambios continuos en los que las aplicaciones se actualizan entre sí a medida que están disponibles nuevos datos.

Los formatos de datos usados por DDE son los mismos que los que usa el Portapapeles. DDE se puede pensar en como una extensión del mecanismo del Portapapeles. Casi siempre se usa el Portapapeles para una respuesta única a un comando de usuario, como elegir el comando Pegar en un menú. DDE también suele iniciarse mediante un comando de usuario, pero a menudo sigue funcionando sin más interacción del usuario. También puede definir formatos de datos DDE personalizados para IPC de uso especial entre aplicaciones con requisitos de comunicaciones más estrechamente acoplados.

Los intercambios DDE pueden producirse entre aplicaciones que se ejecutan en el mismo equipo o en equipos diferentes de una red.

**Punto clave:** DDE no es tan eficaz como las tecnologías más recientes. Sin embargo, todavía puede usar DDE si otros mecanismos de IPC no son adecuados o si debe establecer una interfaz con una aplicación existente que solo admita DDE. Para obtener más información, [vea datos dinámicos Exchange](../dataxchg/dynamic-data-exchange.md) y datos dinámicos Exchange [Management Library](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Uso de una asignación de archivos para IPC

*La asignación* de archivos permite a un proceso tratar el contenido de un archivo como si fuera un bloque de memoria en el espacio de direcciones del proceso. El proceso puede usar operaciones de puntero sencillas para examinar y modificar el contenido del archivo. Cuando dos o más procesos acceden a la misma asignación de archivos, cada proceso recibe un puntero a la memoria en su propio espacio de direcciones que puede usar para leer o modificar el contenido del archivo. Los procesos deben usar un objeto de sincronización, como un semáforo, para evitar daños en los datos en un entorno multitarea.

Puede usar un caso especial de asignación de archivos para proporcionar *memoria compartida con nombre entre* procesos. Si especifica el archivo de intercambio del sistema al crear un objeto de asignación de archivos, el objeto de asignación de archivos se trata como un bloque de memoria compartida. Otros procesos pueden acceder al mismo bloque de memoria abriendo el mismo objeto de asignación de archivos.

La asignación de archivos es bastante eficaz y también proporciona atributos de seguridad compatibles con el sistema operativo que pueden ayudar a evitar daños en los datos no autorizados. La asignación de archivos solo se puede usar entre procesos de un equipo local; no se puede usar a través de una red.

**Punto clave:** La asignación de archivos es una manera eficaz de que dos o más procesos del mismo equipo compartan datos, pero debe proporcionar sincronización entre los procesos. Para obtener más información, vea [Asignación y](/windows/desktop/Memory/file-mapping) sincronización [de archivos.](/windows/desktop/Sync/synchronization)

## <a name="using-a-mailslot-for-ipc"></a>Uso de Mailslot para IPC

Los mailslots proporcionan comunicación uníunica. Cualquier proceso que crea un mailslot es un *servidor mailslot*. Otros procesos, *denominados clientes mailslot,* envían mensajes al servidor mailslot escribiendo un mensaje en su mailslot. Los mensajes entrantes siempre se anexan al mailslot. Mailslot guarda los mensajes hasta que el servidor mailslot los ha leído. Un proceso puede ser un servidor mailslot y un cliente mailslot, por lo que la comunicación bidireccional es posible mediante varios mailslots.

Un cliente mailslot puede enviar un mensaje a un mailslot en su equipo local, a un mailslot en otro equipo o a todos los mailslots con el mismo nombre en todos los equipos de un dominio de red especificado. Los mensajes difundidos a todos los mailslots de un dominio no pueden tener más de 400 bytes, mientras que los mensajes enviados a un solo mailslot solo están limitados por el tamaño máximo de mensaje especificado por el servidor mailslot cuando creó el mailslot.

**Punto clave:** Mailslots ofrece una manera fácil de que las aplicaciones envíen y reciban mensajes cortos. También proporcionan la capacidad de difundir mensajes entre todos los equipos de un dominio de red. Para obtener más información, vea [Mailslots](mailslots.md).

## <a name="using-pipes-for-ipc"></a>Uso de canalizaciones para IPC

Hay dos tipos de canalizaciones para la comunicación bidireccional: canalizaciones anónimas y canalizaciones con nombre. *Las canalizaciones* anónimas permiten a los procesos relacionados transferir información entre sí. Normalmente, se usa una canalización anónima para redirigir la entrada o salida estándar de un proceso secundario para que pueda intercambiar datos con su proceso primario. Para intercambiar datos en ambas direcciones (operación dúplex), debe crear dos canalizaciones anónimas. El proceso primario escribe datos en una canalización mediante su identificador de escritura, mientras que el proceso secundario lee los datos de esa canalización mediante su identificador de lectura. De forma similar, el proceso secundario escribe datos en la otra canalización y el proceso primario lee de ella. Las canalizaciones anónimas no se pueden usar a través de una red ni entre procesos no relacionados.

*Las canalizaciones* con nombre se usan para transferir datos entre procesos que no son procesos relacionados y entre procesos en equipos diferentes. Normalmente, un proceso de servidor de canalización con nombre crea una canalización con nombre con un nombre conocido o un nombre que se va a comunicar a sus clientes. Un proceso de cliente de canalización con nombre que conoce el nombre de la canalización puede abrir su otro extremo, sujeto a las restricciones de acceso especificadas por el proceso de servidor de canalización con nombre. Una vez que el servidor y el cliente se han conectado a la canalización, pueden intercambiar datos realizando operaciones de lectura y escritura en la canalización.

**Punto clave:** Las canalizaciones anónimas proporcionan una manera eficaz de redirigir la entrada o salida estándar a los procesos secundarios en el mismo equipo. Las canalizaciones con nombre proporcionan una interfaz de programación sencilla para transferir datos entre dos procesos, tanto si residen en el mismo equipo como a través de una red. Para obtener más información, vea [Canalizaciones](pipes.md).

## <a name="using-rpc-for-ipc"></a>Uso de RPC para IPC

RPC permite a las aplicaciones llamar a funciones de forma remota. Por lo tanto, RPC hace que IPC sea tan fácil como llamar a una función. RPC funciona entre procesos en un solo equipo o en equipos diferentes de una red.

La RPC proporcionada por Windows es compatible con el entorno de computación distribuida (DCE) de Open Software Foundation (OSF). Esto significa que las aplicaciones que usan RPC pueden comunicarse con aplicaciones que se ejecutan con otros sistemas operativos que admiten DCE. RPC admite automáticamente la conversión de datos para tener en cuenta diferentes arquitecturas de hardware y para el orden de bytes entre entornos diferentes.

Los clientes y servidores RPC están estrechamente acoplados, pero siguen manteniendo un alto rendimiento. El sistema hace un uso amplio de RPC para facilitar una relación cliente-servidor entre diferentes partes del sistema operativo.

**Punto clave:** RPC es una interfaz de nivel de función, compatible con la conversión automática de datos y las comunicaciones con otros sistemas operativos. Con RPC, puede crear aplicaciones distribuidas de alto rendimiento y estrechamente acopladas. Para obtener más información, vea [Componentes rpc de Microsoft](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>Uso de Windows sockets para IPC

Windows Sockets es una interfaz independiente del protocolo. Aprovecha las funcionalidades de comunicación de los protocolos subyacentes. En Windows Sockets 2, un identificador de socket se puede usar opcionalmente como identificador de archivo con las funciones de E/S de archivo estándar.

Windows Los sockets se basan en los sockets popularizados por primera vez por La distribución de software de Berkeley (BSD). Una aplicación que usa Windows Sockets puede comunicarse con otra implementación de socket en otros tipos de sistemas. Sin embargo, no todos los proveedores de servicios de transporte admiten todas las opciones disponibles.

**Punto clave:** Windows sockets es una interfaz independiente del protocolo capaz de admitir las funcionalidades de red actuales y emergentes. Para obtener más información, [vea Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
