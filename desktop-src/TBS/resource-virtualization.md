---
title: Virtualización de recursos
description: Virtualización de recursos
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243789"
---
# <a name="resource-virtualization"></a>Virtualización de recursos

La función principal del TBS es compartir eficazmente determinados recursos de TPM limitados: claves, autorización y sesiones de transporte.

Cuando se crea una instancia de uno de estos recursos, el TBS crea una instancia virtual del recurso y devuelve un identificador a esta instancia virtual en el flujo de comandos de resultados (en lugar de la instancia de identificador real devuelta por el TPM). El TBS mantiene una asignación entre el identificador virtual y el identificador real internamente. Si el TPM se queda sin espacio para contener más recursos de un tipo determinado, las instancias existentes del recurso se guardan y expulsa de forma selectiva hasta que el TPM pueda contener el nuevo recurso. Cuando los recursos antiguos se requieren de nuevo, el TBS carga los contextos guardados (guardar y expulsar otros recursos si es necesario) antes de enviar el comando.

Toda la virtualización de TBS se realiza en nombre de un contexto específico. Cada contexto solo tiene permiso para acceder a los recursos virtuales creados específicamente en su nombre, así como a los recursos físicos del TPM correspondientes a esos recursos virtuales. De forma predeterminada, el número total de todos los recursos virtualizados está limitado a 500. Este número se puede modificar creando o modificando un valor del Registro **DWORD** denominado **MaxResources** en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Tpm**. El uso de recursos de TBS en tiempo real se puede observar mediante la herramienta Monitor de rendimiento para realizar un seguimiento del número de recursos de TBS. Esta restricción ha quedado obsoleta con Windows 8 y Windows Server 2012.

Los recursos de TPM limitados que el TBS no virtualiza (como contadores y almacén de NV) deben compartirse de forma cooperativa entre las pilas de software.

> [!Note]  
> Esta virtualización de identificador hace que se produce un error en los comandos que incluyen identificadores de clave en el cálculo de parámetros de autorización HMAC. Como resultado, el software de la aplicación no puede usar muchos comandos en desuso en la versión 1.2 de TPM en el entorno de TBS.

 

## <a name="resource-limits"></a>Límites de recursos

El TPM permite a los autores de llamadas consultar sus funcionalidades para determinar cuánto espacio está disponible para determinados tipos de recursos. Algunos de estos límites de recursos, como la cantidad de espacio disponible para las claves, las sesiones de autorización y las sesiones de transporte, se extienden eficazmente por el TBS a través de la virtualización. Las limitaciones de TBS, controladas por la configuración del Registro **MaxResources,** suelen ser mucho mayores que las limitaciones reales del hardware de TPM subyacente. No se proporciona ningún mecanismo para consultar las limitaciones de TBS por separado de los límites de hardware de TPM. Esta limitación de TBS ha quedado obsoleta con Windows 8 y Windows Server 2012.

## <a name="keys"></a>Claves

TBS virtualiza los identificadores de clave para que las claves se puedan descargar de forma transparente del TPM cuando no se usen y se vuelvan a cargar en el TPM cuando sean necesarias. Cuando se crea una clave, el TBS asocia un identificador virtual a la clave cargada. El mismo identificador virtual se usa durante la duración del recurso. Los identificadores de clave virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la vida del contexto.

-   Creación de claves con TPM \_ LoadKey2

    Si se crea una clave mediante los comandos \_ LoadKey2, TPM2 \_ CreatePrimary, TPM2 \_ Load o TPM2 LoadExternal, el TBS reemplaza el identificador de la secuencia de bytes devuelto por un identificador de clave virtual de su \_ elección. Como resultado, el TBS garantiza que cada identificador virtual es único. Si el TBS detecta una colisión (un evento extremadamente improbable), este descarga la clave del TPM e informa al software que realiza la llamada. A continuación, el software puede volver a enviar la operación. Este proceso se puede repetir hasta que el TBS obtiene un identificador de clave único.

-   Borrar claves

    TBS invalida el identificador de clave virtual cuando recibe un mensaje FlushSpecific o TPM2 FlushContext de TPM para ese identificador virtual del \_ \_ contexto de cliente. Si la clave está físicamente presente en el TPM cuando se recibe el mensaje de vaciado, el TBS vacía la clave del TPM en ese momento.

-   Quitar temporalmente claves

    Al expulsar una clave del TPM para dar espacio a un nuevo elemento, el TBS ejecuta un comando SaveContext o TPM2 ContextSave de TPM en la clave antes de \_ \_ expulsarlo.

-   Restaurar claves

    Cuando se envía un comando que hace referencia a una clave cargada al TBS, se asegura de que la clave esté físicamente presente en el TPM. Si la clave no está presente, TBS la restaura con una llamada a LOADContext de TPM \_ o \_ a Tpm2 ContextLoad. Si no se puede restaurar una clave en el TPM, el TBS devuelve TPM \_ E \_ INVALID \_ KEYHANDLE como resultado del TPM.

El TBS reemplaza cada identificador virtual asociado a una clave en una secuencia de comandos por el identificador físico de la clave cargada en el TPM. Si se envía un comando con un identificador virtual que el TBS no reconoce en el contexto del autor de la llamada, el TBS da formato a una secuencia de errores para el autor de la llamada con TPM \_ E \_ INVALID \_ KEYHANDLE.

## <a name="authorization-sessions"></a>Sesiones de autorización

Las sesiones de autorización se crean mediante una llamada a \_ TPM OIAP, TPM \_ OSAP o TPM \_ DSAP. En cada caso, la secuencia de bytes de retorno contiene el identificador de TPM físico de la sesión de autorización recién creada. El TBS lo reemplaza por un identificador virtual. Cuando se hace referencia posteriormente a la sesión de autorización, el TBS reemplaza el identificador virtual en el flujo de comandos por el identificador físico de la sesión de autorización. El TBS garantiza que la duración de la sesión de autorización virtual coincide con la de la sesión de autorización física. Si un cliente intenta usar un identificador virtual expirado, el TBS da formato a una secuencia de errores con el error TPM \_ INVALIDAUTHHANDLE.

Las ranuras de sesión son limitadas y el TBS puede que se queme de las ranuras externas en las que guardar los contextos de la sesión de autorización. Si esto sucede, el TBS elige una sesión de autorización para invalidar para que el nuevo contexto se pueda guardar correctamente. Una aplicación que intente usar el contexto anterior deberá volver a crear la sesión de autorización.

El TBS invalida la sesión de autorización virtual cuando se produce cualquiera de los siguientes casos:

-   La marca continue-use asociada a la sesión de autorización en el flujo de comandos devuelto del TPM es **FALSE.**
-   Se produce un error en un comando que usa una sesión de autorización.
-   Se ejecuta un comando que invalida la sesión de autorización asociada al comando (por ejemplo, TPM \_ CreateWrapKey).
-   Una clave asociada a una sesión de OSAP o DSAP se expulsa del TPM con una llamada a TPM \_ FlushSpecific o TPM2 FlushContext (sin tener en cuenta si este comando se originó con el TBS o con software de nivel \_ superior).

    El TBS volverá a sincronizar automáticamente las sesiones de autorización después de la ejecución correcta de determinados comandos no deterministas para asegurarse de que el estado de TBS sigue siendo coherente con el estado de TPM. Los comandos afectados son:

    -   Administración \_ de delegados ORD \_ de TPM \_
    -   \_ \_ \_ CreateOwnerDelegation del delegado ORD de TPM
    -   LoadOwnerDelegation del delegado \_ ORD \_ de TPM \_

En cada uno de los siguientes casos, el TPM vacía automáticamente la sesión de autorización en el TPM:

-   Creación de sesiones de autorización

    Los identificadores de sesión de autorización virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la vida del contexto asociado.

-   Borrar sesiones de autorización

    TBS invalida la sesión de autorización virtual si recibe un comando FlushSpecific o TPM2 FlushContext de TPM para el identificador virtual del \_ \_ contexto de cliente. Si la sesión de autorización está físicamente presente en el TPM cuando se recibe el comando flush, el TBS vacía la sesión física del TPM inmediatamente.

-   Eliminación temporal de sesiones de autorización

    Al expulsar una sesión de autorización del TPM para dar espacio a una nueva entidad, el TBS ejecuta TPM SaveContext o TPM2 ContextSave en esa sesión \_ \_ de autorización.

-   Restaurar sesiones de autorización

    Cuando se envía un comando DE TPM autorizado al TBS, este garantiza que todas las sesiones de autorización virtual a las que se hace referencia en el comando están físicamente presentes en el TPM. Si alguna de las sesiones de autorización no está presente, el TBS las restaura con una llamada a LoadContext de TPM o \_ \_ a ContextLoad de TPM2. Si no se puede restaurar una sesión de autorización en el TPM, el TBS devuelve TPM \_ E INVALID HANDLE como resultado del \_ \_ TPM.

El TBS reemplaza cada identificador virtual asociado a una sesión de autorización en una secuencia de comandos por el identificador físico de la sesión de autorización cargada en el TPM.

Si se envía un comando con un identificador virtual que el TBS no reconoce en el contexto del autor de la llamada, el TBS da formato a una secuencia de errores para el autor de la llamada con el error TPM \_ E \_ INVALID \_ HANDLE.

## <a name="transport-sessions"></a>Sesiones de transporte

> [!Note]  
> El control de las sesiones de transporte como se describe aquí es específico de Windows Vista y Windows Server 2008.

 

Las sesiones de transporte son un mecanismo proporcionado por el TPM que permite que una pila de software cifre los datos en un comando a medida que pasa entre el software y el TPM. Esto evita que un adversario intercepte los datos a medida que pasa por el bus de hardware.

> [!IMPORTANT]
> Solo se cifran los datos de carga. Los comandos que se ejecutan todavía se pueden identificar.

 

Desafortunadamente, este mecanismo también impide que el TBS examine los datos de carga. En la mayoría de los casos, esto no es un problema porque el TBS solo modifica los identificadores, no los datos de carga. Sin embargo, en el caso de LOADContext de TPM, por ejemplo, el identificador de recursos devuelto \_ está cubierto por el cifrado. Por lo tanto, el TBS impide los intentos de realizar una operación LoadContext de TPM \_ cubierta por una sesión de transporte.

El TBS bloquea los siguientes comandos en la sesión de transporte:

-   TPM \_ EstablishTransport
-   TPM \_ ExecuteTransport
-   Controlador de \_ terminación de TPM \_
-   TPM \_ LoadKey
-   TPM \_ EvictKey
-   TPM \_ SaveKeyContext
-   TPM \_ LoadKeyContext
-   TPM \_ SaveAuthContext
-   LoadAuthContext de TPM \_
-   TPM \_ SaveContext
-   TPM \_ LoadContext
-   TPM \_ FlushSpecific

Cuando cualquiera de estos comandos está cubierto por una sesión de transporte, el TBS devuelve TPM \_ E \_ EMBEDDED COMMAND \_ \_ UNSUPPORTED como resultado de TPM.

Los identificadores de sesión de transporte se virtualizan de forma similar a los identificadores de clave y de autorización. Hay un número limitado de ranuras de contexto de sesión de transporte guardadas disponibles en el TPM.

El TBS invalida la sesión de transporte virtual si se produce alguno de los siguientes casos:

-   La marca continue-use asociada a la sesión de transporte en el flujo de comandos de devolución del TPM es **FALSE.**

    Al igual que con las sesiones de autorización anteriores, el TBS volverá a sincronizar automáticamente las sesiones de transporte después de la ejecución correcta de determinados comandos no deterministas para asegurarse de que el estado de TBS sigue siendo coherente con el estado de TPM. Los comandos afectados son:

    -   Administración \_ de delegados ORD \_ de TPM \_
    -   TPM \_ ORD \_ Delegate \_ CreateOwnerDelegation
    -   TPM \_ ORD \_ Delegate \_ LoadOwnerDelegation

En cada uno de estos casos, el TPM vaciará automáticamente la sesión de transporte en el TPM:

-   Crear sesiones de transporte

    El TBS crea un identificador virtual para cada sesión de transporte creada por un cliente. Los identificadores de transporte virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la vida del contexto asociado.

-   Borrar sesiones de transporte

    El TBS invalida la sesión de transporte virtual si recibe un comando FlushSpecific de TPM para el \_ identificador virtual del contexto de cliente. Si la sesión de transporte está físicamente presente en el TPM cuando se recibe el comando flush, el TBS vacía la sesión física del TPM inmediatamente.

-   Quitar temporalmente sesiones de transporte

    Al expulsar una sesión de transporte del TPM para hacer espacio para una nueva entidad, el TBS ejecuta \_ TPM SaveContext en esa sesión de transporte.

-   Restaurar sesiones de transporte

    Cuando se envía un comando ExecuteTransport de TPM al TBS, el TBS garantiza que la sesión de transporte a la que se hace referencia en el comando está físicamente \_ presente en el TPM. Si la sesión de transporte no está presente, el TBS la restaura con una llamada a \_ LoadContext de TPM.

El TBS reemplaza el identificador virtual asociado a la sesión de transporte en una secuencia de comandos por el identificador físico de la sesión de transporte cargada en el TPM. Si se envía un comando con un identificador virtual que el TBS no reconoce en el contexto del autor de la llamada, el TBS da formato a un flujo de errores para el autor de la llamada mediante TPM \_ E \_ INVALID \_ HANDLE.

## <a name="exclusive-transport-sessions"></a>Sesiones de transporte exclusivo

Las sesiones de transporte encapsuladas exclusivas son una manera de que el software de nivel superior determine si algún otro software ha accedido al TPM durante una cadena de comandos. No impiden que otro software acceda al TPM, simplemente dan al creador de la sesión de transporte un medio para determinar que se ha producido algún otro acceso. El TBS no hace nada específico para entorpecer las sesiones de transporte exclusivo, pero es algo incompatible con ellas. El TBS intenta duplicar el comportamiento natural del TPM al ser transparente, por lo que no favorece los comandos de los contextos que establecen una sesión de transporte exclusiva. Por ejemplo, si el cliente B envía un comando cuando el cliente A está en una sesión de transporte exclusiva, invalidará la sesión de transporte exclusivo del cliente A.

Los comandos iniciados por TBS también pueden finalizar la sesión de transporte exclusivo. Esto sucede cuando el cliente A está en una sesión de transporte exclusivo y un comando ejecutado por el cliente A llama a un recurso que no está físicamente presente en el TPM. Esta situación desencadena que el administrador de virtualización de TBS ejecute un comando loadContext de TPM para proporcionar ese recurso, lo que finaliza la sesión de \_ transporte exclusivo del cliente A.

 

 




