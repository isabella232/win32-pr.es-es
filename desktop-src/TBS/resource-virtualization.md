---
title: Virtualización de recursos
description: Virtualización de recursos
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777353"
---
# <a name="resource-virtualization"></a>Virtualización de recursos

La función principal de TBS es compartir eficazmente determinados recursos de TPM limitados: claves, autorización y sesiones de transporte.

Cuando se crea una instancia de uno de estos recursos, el TBS crea una instancia virtual del recurso y devuelve un identificador a esta instancia virtual en la secuencia de comandos de resultados (en lugar de la instancia de identificador real devuelta por el TPM). TBS mantiene una asignación entre el identificador virtual y el identificador real internamente. Si el TPM se queda sin espacio para contener más recursos de un tipo determinado, las instancias existentes del recurso se guardan y se expulsan de manera selectiva hasta que el TPM pueda contener el nuevo recurso. Cuando los recursos antiguos vuelven a ser necesarios, el TBS carga los contextos guardados (guardando y expulsando otros recursos, si es necesario) antes de enviar el comando.

Toda la virtualización en TBS se realiza en nombre de un contexto específico. Cada contexto solo tiene permiso para acceder a los recursos virtuales creados específicamente en su nombre, así como a los recursos físicos en el TPM que corresponden a esos recursos virtuales. De forma predeterminada, el número total de todos los recursos virtualizados está limitado a 500. Este número puede modificarse mediante la creación o modificación de un valor del registro **DWORD** denominado **MaxResources** en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. Se puede observar el uso de recursos de TBS en tiempo real mediante la herramienta Monitor de rendimiento para realizar el seguimiento del número de recursos de TBS. Esta restricción quedó obsoleta en Windows 8 y Windows Server 2012.

Los recursos de TPM limitados que no están virtualizados por TBS (como los contadores y el almacén NV) deben compartirse de forma cooperativa entre las pilas de software.

> [!Note]  
> Este identificador de virtualización hace que se produzca un error en los comandos que incluyen identificadores de clave en el cálculo de parámetros de autorización HMAC. Como resultado, el software de la aplicación no puede usar muchos comandos en desuso en la versión 1,2 de TPM en el entorno de TBS.

 

## <a name="resource-limits"></a>Límites de recursos

El TPM permite a los autores de llamadas consultar sus funciones para determinar cuánto espacio hay disponible para determinados tipos de recursos. Algunos de estos límites de recursos, como la cantidad de espacio disponible para las claves, las sesiones de autorización y las sesiones de transporte, se amplían eficazmente mediante TBS a través de virtualización. Las limitaciones de TBS, que están controladas por la configuración del registro **MaxResources** , suelen ser mucho mayores que las limitaciones reales del hardware TPM subyacente. No se proporciona ningún mecanismo para consultar las limitaciones de TBS por separado de los límites de hardware de TPM. Esta limitación de TBS quedó obsoleta en Windows 8 y Windows Server 2012.

## <a name="keys"></a>Claves

TBS Virtualiza los identificadores de clave para que las claves se puedan descargar de forma transparente desde el TPM cuando no se usan y se vuelven a cargar en el TPM cuando se necesitan. Cuando se crea una clave, TBS asocia un identificador virtual a la clave cargada. Se utiliza el mismo identificador virtual para la duración del recurso. Los identificadores de clave virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la vida del contexto.

-   Crear claves con LoadKey2 de TPM \_

    Si se crea una clave mediante el \_ comando LoadKey2 de TPM, TPM2 \_ CREATEPRIMARY, TPM2 \_ Load o TPM2 \_ LoadExternal, TBS reemplaza el identificador de la secuencia de bytes devuelta por un identificador de clave virtual de su elección. Como resultado, el TBS garantiza que cada identificador virtual sea único. Si el TBS detecta una colisión (un evento extremadamente improbable), el TBS descarga la clave de TPM e informa al software que realiza la llamada. Después, el software puede volver a enviar la operación. Este proceso puede repetirse hasta que el TBS obtenga un identificador de clave único.

-   Borrar claves

    TBS invalida el identificador de la clave virtual cuando recibe un \_ mensaje FlushSpecific de TPM o TPM2 \_ FlushContext para ese identificador virtual desde el contexto del cliente. Si la clave está físicamente presente en el TPM cuando se recibe el mensaje de vaciado, el TBS vacía la clave del TPM en ese momento.

-   Quitar claves temporalmente

    Al expulsar una clave de TPM para dejar espacio para un nuevo elemento, TBS ejecuta un \_ comando SaveContext de TPM o TPM2 \_ ContextSave en la clave antes de expulsarlo.

-   Restaurar claves

    Cuando un comando que hace referencia a una clave cargada se envía a TBS, garantiza que la clave está físicamente presente en el TPM. Si la clave no está presente, TBS la restaura con una llamada a LoadContext de TPM \_ o a TPM2 \_ ContextLoad. Si no se puede restaurar una clave en el TPM, el TBS devuelve \_ el \_ KEYHANDLE no válido de TPM \_ como resultado del TPM.

TBS reemplaza cada identificador virtual asociado a una clave en una secuencia de comandos con el identificador físico de la clave cargada en el TPM. Si un comando se envía con un identificador virtual que no es reconocido por TBS en el contexto del autor de la llamada, TBS da formato a una secuencia de error para el autor de la llamada con el TPM \_ E \_ KEYHANDLE no válidos \_ .

## <a name="authorization-sessions"></a>Sesiones de autorización

Las sesiones de autorización se crean mediante una llamada a \_ OIAP de TPM, TPM \_ OSAP o TPM \_ DSAP. En cada caso, la secuencia de bytes devuelta contiene el identificador de TPM físico de la sesión de autorización recién creada. TBS lo reemplaza por un identificador virtual. Cuando se hace referencia a la sesión de autorización posteriormente, el TBS reemplaza el identificador virtual en la secuencia de comandos con el identificador físico de la sesión de autorización. El TBS garantiza que la duración de la sesión de autorización virtual coincide con la de la sesión de autorización física. Si un cliente intenta usar un identificador virtual expirado, TBS da formato a una secuencia de error con el error TPM \_ INVALIDAUTHHANDLE.

Las ranuras de sesión están limitadas y es posible que se agoten las ranuras externas en las que se guardan los contextos de la sesión de autorización. Si esto ocurre, el TBS elige una sesión de autorización para invalidar de modo que el nuevo contexto se pueda guardar correctamente. Una aplicación que intente usar el contexto anterior tendrá que volver a crear la sesión de autorización.

El TBS invalida la sesión de autorización virtual cuando se produce cualquiera de los siguientes casos:

-   La marca de uso continuado asociada a la sesión de autorización en la secuencia de comandos devuelta desde el TPM es **falsa**.
-   Se produce un error en un comando que usa una sesión de autorización.
-   Se ejecuta un comando que invalida la sesión de autorización asociada al comando (como CreateWrapKey de TPM \_ ).
-   Una clave asociada a una sesión de OSAP o DSAP se expulsa del TPM con una llamada a TPM \_ FlushSpecific o TPM2 \_ FlushContext (sin tener en cuenta si este comando se originó con TBS o con software de nivel superior).

    Los TBS volverán a sincronizar automáticamente las sesiones de autorización después de la ejecución correcta de determinados comandos no deterministas para asegurarse de que el estado de TBS sigue siendo coherente con el estado de TPM. Los comandos afectados son:

    -   \_Administración de \_ delegado de Ord de TPM \_
    -   \_ \_ CreateOwnerDelegation delegado de Ord de TPM \_
    -   \_ \_ LoadOwnerDelegation delegado de Ord de TPM \_

En cada uno de los casos siguientes, el TPM vacía automáticamente la sesión de autorización en el TPM:

-   Crear sesiones de autorización

    Los identificadores de sesión de autorización virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la duración del contexto asociado.

-   Borrar sesiones de autorización

    El TBS invalida la sesión de autorización virtual si recibe un \_ comando FlushSpecific de TPM o TPM2 \_ FlushContext para el identificador virtual desde el contexto del cliente. Si la sesión de autorización está físicamente presente en el TPM cuando se recibe el comando de vaciado, el TBS vacía inmediatamente la sesión física desde el TPM.

-   Quitar temporalmente sesiones de autorización

    Al expulsar una sesión de autorización del TPM para dejar espacio para una nueva entidad, TBS ejecuta SaveContext de TPM \_ o TPM2 \_ ContextSave en esa sesión de autorización.

-   Restaurar sesiones de autorización

    Cuando se envía un comando de TPM autorizado a TBS, el TBS garantiza que todas las sesiones de autorización virtual a las que se hace referencia en el comando estén físicamente presentes en el TPM. Si alguna de las sesiones de autorización no está presente, TBS las restaura con una llamada a \_ LoadContext o TPM2 ContextLoad de TPM \_ . Si no se puede restaurar una sesión de autorización en el TPM, el TBS devuelve un \_ \_ identificador no válido de TPM \_ como resultado de TPM.

TBS reemplaza cada identificador virtual asociado a una sesión de autorización en una secuencia de comandos con el identificador físico de la sesión de autorización cargada en el TPM.

Si un comando se envía con un identificador virtual que no reconoce TBS en el contexto del autor de la llamada, TBS da formato a una secuencia de error para el autor de la llamada con el error TPM \_ E \_ identificador no válido \_ .

## <a name="transport-sessions"></a>Sesiones de transporte

> [!Note]  
> El control de las sesiones de transporte como se describe aquí es específico de Windows Vista y Windows Server 2008.

 

Las sesiones de transporte son un mecanismo proporcionado por el TPM que permite a una pila de software cifrar los datos en un comando a medida que pasa entre el software y el TPM. Esto evita que un adversario intercepte los datos a medida que pasan por el bus de hardware.

> [!IMPORTANT]
> Solo se cifran los datos de carga. Todavía se pueden identificar los comandos que se están ejecutando.

 

Desafortunadamente, este mecanismo también impide que el TB examine los datos de carga. En la mayoría de los casos, esto no es un problema porque TBS solo modifica los identificadores, no los datos de carga. Sin embargo, en el caso de \_ LoadContext de TPM por ejemplo, el identificador de recursos devuelto está incluido en el cifrado. Por lo tanto, el TBS impide que se intente realizar una operación LoadContext de TPM que esté \_ incluida en una sesión de transporte.

TBS bloquea los siguientes comandos en la sesión de transporte:

-   EstablishTransport de TPM \_
-   ExecuteTransport de TPM \_
-   \_Identificador de finalización de TPM \_
-   LoadKey de TPM \_
-   EvictKey de TPM \_
-   SaveKeyContext de TPM \_
-   LoadKeyContext de TPM \_
-   SaveAuthContext de TPM \_
-   LoadAuthContext de TPM \_
-   SaveContext de TPM \_
-   LoadContext de TPM \_
-   FlushSpecific de TPM \_

Cuando uno de estos comandos está incluido en una sesión de transporte, el TBS devuelve el \_ \_ comando incrustado de TPM E incrustado \_ \_ como resultado de TPM.

Los identificadores de sesión de transporte se virtualizan de una manera similar a los identificadores de clave y de autorización. Hay un número limitado de ranuras de contexto de la sesión de transporte guardadas disponibles en el TPM.

El TBS invalida la sesión de transporte virtual si se produce alguno de los siguientes casos:

-   La marca de uso continuado asociada a la sesión de transporte en la secuencia de comandos devuelta del TPM es **falsa**.

    Al igual que con las sesiones de autorización anteriores, TBS volverá a sincronizar automáticamente las sesiones de transporte después de la ejecución correcta de determinados comandos no deterministas para asegurarse de que el estado de TBS sigue siendo coherente con el estado de TPM. Los comandos afectados son:

    -   \_Administración de \_ delegado de Ord de TPM \_
    -   \_ \_ CreateOwnerDelegation delegado de Ord de TPM \_
    -   \_ \_ LoadOwnerDelegation delegado de Ord de TPM \_

En cada uno de estos casos, el TPM vaciará automáticamente la sesión de transporte en el TPM:

-   Crear sesiones de transporte

    El TBS crea un identificador virtual para cada sesión de transporte creada por un cliente. Los identificadores de transporte virtual solo son válidos en el contexto que los creó y los recursos asociados no se conservan más allá de la duración del contexto asociado.

-   Borrar sesiones de transporte

    El TBS invalida la sesión de transporte virtual si recibe un \_ comando FlushSpecific de TPM para el identificador virtual desde el contexto del cliente. Si la sesión de transporte está físicamente presente en el TPM cuando se recibe el comando de vaciado, el TBS vacía inmediatamente la sesión física desde el TPM.

-   Quitar temporalmente las sesiones de transporte

    Al expulsar una sesión de transporte del TPM para dejar espacio para una nueva entidad, TBS ejecuta \_ SaveContext de TPM en esa sesión de transporte.

-   Restaurar sesiones de transporte

    Cuando \_ se envía un comando ExecuteTransport de TPM a TBS, el TBS garantiza que la sesión de transporte a la que se hace referencia en el comando esté físicamente presente en el TPM. Si la sesión de transporte no está presente, TBS la restaura con una llamada a LoadContext de TPM \_ .

TBS reemplaza el identificador virtual asociado a la sesión de transporte en una secuencia de comandos con el identificador físico de la sesión de transporte cargada en el TPM. Si un comando se envía con un identificador virtual que no reconoce TBS en el contexto del autor de la llamada, TBS da formato a una secuencia de error para el autor de la llamada mediante el uso de un \_ \_ identificador no válido de TPM E \_ .

## <a name="exclusive-transport-sessions"></a>Sesiones de transporte exclusivas

Las sesiones de transporte ajustadas exclusivas son una manera de que el software de nivel superior determine si cualquier otro software ha tenido acceso al TPM durante una cadena de comandos. No impiden que otro software tenga acceso al TPM, simplemente proporcionan al creador de la sesión de transporte un medio para determinar que se ha producido algún otro acceso. TBS no hace nada específico para entorpecer las sesiones de transporte exclusivas, pero es algo incompatible con ellos. TBS intenta duplicar el comportamiento natural del TPM por ser transparente, por lo que no favorece los comandos de los contextos que establecen una sesión de transporte exclusiva. Por ejemplo, si el cliente B envía un comando cuando el cliente A está en una sesión de transporte exclusiva, se invalidará la sesión de transporte exclusiva del cliente A.

Los comandos iniciados por TBS también pueden finalizar la sesión de transporte exclusiva. Esto sucede cuando el cliente A está en una sesión de transporte exclusiva y un comando ejecutado por el cliente A llama a un recurso que no está presente físicamente en el TPM. Esta situación desencadena que el administrador de virtualización de TBS ejecute un \_ comando LoadContext de TPM para proporcionar ese recurso, que finaliza la sesión de transporte exclusiva del cliente a.

 

 




