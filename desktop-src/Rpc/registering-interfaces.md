---
title: Registrar interfaces
description: Registro de una interfaz de llamada a procedimiento remoto (RPC).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268251"
---
# <a name="registering-interfaces"></a>Registrar interfaces

En esta sección se ofrece una explicación detallada del proceso de registro de una interfaz RPC.

La información de esta sección se presenta en los temas siguientes:

-   [Funciones de registro de interfaz](#interface-registration-functions)
-   [Vectores de punto de entrada](#entry-point-vectors)
-   [EPVs Manager](#manager-epvs)
-   [Registrar una única implementación de una interfaz](#registering-a-single-implementation-of-an-interface)
-   [Registro de varias implementaciones de una interfaz](#registering-multiple-implementations-of-an-interface)
-   [Reglas para invocar rutinas de administrador](#rules-for-invoking-manager-routines)
-   [Enviar una llamada a un procedimiento remoto a una rutina de Server-Manager](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Proporcionar su propia Object-Inquiry función](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Funciones de registro de interfaz

Los servidores registran sus interfaces mediante una llamada a la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) . Los programas de servidor complejos suelen admitir más de una interfaz. Las aplicaciones de servidor deben llamar a esta función una vez para cada interfaz que admitan.

Además, los servidores pueden admitir varias versiones de la misma interfaz, cada una con su propia implementación de las funciones de la interfaz. Si el programa de servidor lo hace, debe proporcionar un conjunto de puntos de entrada. Un punto de entrada es una rutina de administrador que envía llamadas para una versión de una interfaz. Debe haber un punto de entrada para cada versión de la interfaz. El grupo de puntos de entrada se denomina vector de punto de entrada. Para obtener más información, consulte [vectores de punto de entrada](#entry-point-vectors).

Además de la función estándar [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), RPC también admite otras funciones de registro de la interfaz. La función [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) amplía las capacidades de **RpcServerRegisterIf** al permitirle especificar un conjunto de marcas de registro (consulte [marcas de registro](interface-registration-flags.md)de la interfaz), el número máximo de solicitudes simultáneas de llamada a procedimiento remoto que el servidor puede aceptar y el tamaño máximo en bytes de los bloques de datos entrantes.

La biblioteca RPC también contiene una función denominada [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex). Al igual que la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , esta función registra una interfaz. El programa del servidor también puede usar esta función para especificar un conjunto de marcas de registro (vea [marcas de registro](interface-registration-flags.md)de la interfaz), el número máximo de solicitudes simultáneas de llamada a procedimiento remoto que el servidor puede aceptar y una función de devolución de llamada de seguridad.

Las funciones [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)y [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) establecen valores en la tabla interna del registro de la interfaz. Esta tabla se usa para asignar el UUID de interfaz y el UUID de objeto a un administrador EPV. EPV Manager es una matriz de punteros de función que contiene exactamente un puntero de función para cada prototipo de función en la interfaz especificada en el archivo IDL.

Para obtener información sobre cómo proporcionar varios EPVs para proporcionar varias implementaciones de la interfaz, vea [varias implementaciones de interfaz](#registering-multiple-implementations-of-an-interface).

La biblioteca en tiempo de ejecución utiliza la tabla del registro de la interfaz (establecida mediante llamadas a la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) y la tabla del registro de objetos (establecida mediante llamadas a la función [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) para asignar el UUID de interfaz y objeto al puntero de función.

Si desea que el programa de servidor Quite una interfaz del registro de la biblioteca en tiempo de ejecución de RPC, llame a la función [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) . Después de quitar la interfaz del registro, la biblioteca en tiempo de ejecución de RPC ya no aceptará nuevas llamadas para esa interfaz.

## <a name="entry-point-vectors"></a>Vectores de punto de entrada

El vector de punto de entrada (EPV) del administrador es una matriz de punteros de función que apunta a las implementaciones de las funciones especificadas en el archivo IDL. El número de elementos de la matriz se corresponde con el número de funciones especificadas en el archivo IDL. RPC admite varios vectores de punto de entrada que representan varias implementaciones de las funciones especificadas en la interfaz.

El compilador MIDL genera automáticamente un tipo de datos Manager EPV para su uso en la creación de EPVs Manager. El tipo de datos se denomina * if-name ***\_ Server \_ EPV**, donde *-Name* especifica el identificador de interfaz en el archivo IDL.

El compilador MIDL crea e inicializa automáticamente un administrador predeterminado EPV en el supuesto de que existe una rutina de administrador con el mismo nombre para cada procedimiento de la interfaz y se especifica en el archivo IDL.

Cuando un servidor ofrece varias implementaciones de la misma interfaz, el servidor debe crear un EPV de administrador adicional para cada implementación. Cada EPV debe contener exactamente un punto de entrada (dirección de una función) para cada procedimiento definido en el archivo IDL. La aplicación de servidor declara e inicializa una variable EPV de administrador de tipo *If-name * * * \_ Server \_ EPV** para cada implementación adicional de la interfaz. Para registrar EPVs, llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) una vez por cada tipo de objeto que admite.

Cuando el cliente realiza una llamada a procedimiento remoto al servidor, el EPV que contiene el puntero de función se selecciona basándose en el UUID de la interfaz y el tipo de objeto. El tipo de objeto se deriva del UUID del objeto mediante la función de consulta de objeto o la asignación controlada por tabla controlada por [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).

## <a name="manager-epvs"></a>EPVs Manager

De forma predeterminada, el compilador MIDL usa los nombres de procedimiento del archivo IDL de una interfaz para generar un administrador EPV, que el compilador coloca directamente en el código auxiliar del servidor. Este EPV predeterminado se inicializa estáticamente mediante los nombres de procedimiento declarados en la definición de interfaz.

Para registrar un administrador mediante el EPV predeterminado, especifique **null** como el valor del parámetro *MgrEpv* en una llamada a la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) . Si los nombres de rutina utilizados por un administrador se corresponden con los de la definición de interfaz, puede registrar este administrador mediante el EPV predeterminado de la interfaz generada por el compilador de MIDL. También puede registrar un administrador mediante un EPV que proporciona la aplicación de servidor.

Un servidor puede (y a veces debe) crear y registrar un EPV de administrador que no sea **nulo** para una interfaz. Para seleccionar un EPV proporcionado por una aplicación de servidor, pase la dirección de un EPV cuyo valor se ha declarado por el servidor como el valor del parámetro *MgrEpv* a. Un valor no **null** para *MgrEpv* un parámetro siempre invalida un EPV predeterminado en el código auxiliar del servidor.

El compilador MIDL genera automáticamente un tipo de datos Manager EPV ( \_ \_ EPV de administración de RPC) para que una aplicación de servidor lo use en la creación de EPVs Manager. Un administrador EPV debe contener exactamente un punto de entrada (dirección de función) para cada procedimiento definido en el archivo IDL.

Un servidor debe proporcionar un EPV que no sea **null** en los casos siguientes:

-   Cuando los nombres de las rutinas de administrador difieren de los nombres de procedimiento declarados en la definición de interfaz
-   Cuando el servidor usa el valor predeterminado de EPV para registrar otra implementación de la interfaz

Un servidor declara un administrador EPV inicializando una variable de tipo *If-name * * * \_ Server \_ EPV** para cada implementación de la interfaz.

## <a name="registering-a-single-implementation-of-an-interface"></a>Registrar una única implementación de una interfaz

Cuando un servidor solo ofrece una implementación de una interfaz, el servidor llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) solo una vez. En el caso estándar, el servidor utiliza el administrador predeterminado EPV. (La excepción es cuando el administrador usa nombres de rutina que difieren de los declarados en la interfaz).

Para el caso estándar, proporcione los siguientes valores para las llamadas a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2):

-   EPVs Manager

    Para usar el valor predeterminado de EPV, especifique un valor **null** para el parámetro *MgrEpv* .

-   UUID de tipo de administrador

    Al usar el valor predeterminado de EPV, registre la interfaz con un UUID de tipo de administrador Nil proporcionando un valor **null** o un UUID nulo para el parámetro *MgrTypeUuid* a. En este caso, todas las llamadas a procedimientos remotos, independientemente del UUID del objeto en su identificador de enlace, se envían al valor predeterminado de EPV, suponiendo que no se ha realizado ninguna llamada a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    También puede proporcionar un UUID de tipo de administrador que no sea Nil. En este caso, también debe llamar a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

## <a name="registering-multiple-implementations-of-an-interface"></a>Registro de varias implementaciones de una interfaz

Puede proporcionar más de una implementación de los procedimientos remotos especificados en el archivo IDL. La aplicación de servidor llama a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para asignar el UUID del objeto al tipo UUID y llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar el administrador EPVs con un UUID de tipo. Cuando una llamada a procedimiento remoto llega con su UUID de objeto, la biblioteca en tiempo de ejecución del servidor RPC asigna el UUID del objeto a un tipo UUID. A continuación, la aplicación de servidor usa el tipo UUID y el UUID de la interfaz para seleccionar el administrador EPV.

También puede especificar su propia función para resolver la asignación desde el UUID del objeto al tipo de administrador UUID. La función de asignación se especifica cuando se llama a [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn).

Para ofrecer varias implementaciones de una interfaz, un servidor debe registrar cada implementación llamando a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) por separado. Para cada implementación que un servidor registra, proporciona el mismo *IfSpec* un parámetro, pero un par diferente de *MgrTypeUuid* y *MgrEpv* a los parámetros.

En el caso de varios administradores, use [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) de la siguiente manera:

-   EPVs Manager

    Para ofrecer varias implementaciones de una interfaz, un servidor debe:

    -   Cree un EPV de administrador que no sea **nulo** para cada implementación adicional.
    -   Especifique un valor distinto de **null** para el *parámetro MgrEpv* en [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

    Tenga en cuenta que el servidor también se puede registrar con el administrador predeterminado EPV.

-   UUID de tipo de administrador

    Proporcione un UUID de tipo de administrador para cada EPV de la interfaz. El UUID de tipo Nil (o valor **null** ) para *MgrTypeUuid* se puede especificar un parámetro para una de las EPVs de administración. Cada UUID de tipo debe ser diferente.

## <a name="rules-for-invoking-manager-routines"></a>Reglas para invocar rutinas de administrador

La biblioteca en tiempo de ejecución de RPC envía una llamada de procedimiento remoto entrante a un administrador que ofrece la interfaz RPC solicitada. Cuando se registran varios administradores para una interfaz, la biblioteca en tiempo de ejecución de RPC debe seleccionar uno de ellos. Para seleccionar un administrador, la biblioteca en tiempo de ejecución de RPC utiliza el UUID del objeto especificado por el identificador de enlace de la llamada.

La biblioteca en tiempo de ejecución aplica las siguientes reglas al interpretar el UUID del objeto de una llamada a procedimiento remoto:

-   UUID de objeto Nil

    A un UUID de objeto Nil se le asigna automáticamente el UUID de tipo Nil (no es válido especificar un UUID de objeto Nil en la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) ). Por lo tanto, una llamada a procedimiento remoto cuyo identificador de enlace contiene un UUID de objeto Nil se envía automáticamente al administrador registrado con el UUID de tipo Nil, si existe.

-   UUID de objeto no Nil

    En principio, una llamada a procedimiento remoto cuyo identificador de enlace contiene un UUID de objeto distinto de Nil debe ser procesada por un administrador cuyo tipo UUID coincida con el tipo del UUID del objeto. Sin embargo, la identificación del administrador correcto requiere que el servidor haya especificado el tipo de UUID del objeto llamando a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    Si un servidor no llama a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para un UUID de objeto que no sea Nil, una llamada a procedimiento remoto para ese UUID de objeto va al administrador EPV que da servicio a las llamadas a procedimientos remotos con un UUID de objeto nulo (es decir, el UUID de tipo Nil).

    No se pueden ejecutar llamadas a procedimientos remotos con un UUID de objeto que no sea Nil en el identificador de enlace si el servidor asignado a ese UUID de objeto no Nil es un UUID de tipo llamando a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) , pero no registró también un EPV de administrador para ese UUID de tipo llamando a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

En la tabla siguiente se resumen las acciones que utiliza la biblioteca en tiempo de ejecución para seleccionar la rutina Manager.



| UUID del objeto de la llamada | Tipo de conjunto de servidores para el UUID del objeto | ¿EPV el tipo de servidor registrado? | Enviando acción                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nulo                 | No aplicable                   | Sí                         | Utiliza el administrador con el UUID de tipo Nil.                                                                                                           |
| Nulo                 | No es aplicable                   | No                          | Error ( \_ no se \_ admite el tipo de RPC S \_ ); rechaza la llamada a procedimiento remoto.                                                                              |
| No Nil             | Sí                              | Sí                         | Utiliza el administrador con el mismo tipo UUID.                                                                                                          |
| No Nil             | No                               | Omitido                     | Utiliza el administrador con el UUID de tipo Nil. Si no hay ningún administrador con el tipo Nil UUID, error (RPC \_ S \_ UNSUPPORTEDTYPE); rechaza la llamada a procedimiento remoto. |
| No Nil             | Sí                              | No                          | Error (RPC \_ S \_ UNSUPPORTEDTYPE); rechaza la llamada a procedimiento remoto.                                                                                |



 

El UUID del objeto de la llamada es el UUID del objeto encontrado en un identificador de enlace para una llamada a procedimiento remoto.

El servidor establece el tipo del UUID del objeto mediante una llamada a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para especificar el UUID del tipo de un objeto.

El servidor registra el tipo para el administrador EPV llamando a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) con el mismo UUID de tipo.

> [!Note]  
> Al UUID del objeto Nil siempre se le asigna automáticamente el UUID de tipo Nil. No es válido especificar un UUID de objeto Nil en la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Enviar una llamada a procedimiento remoto a una rutina del administrador de servidores

En las tablas siguientes se muestran los pasos que la biblioteca en tiempo de ejecución de RPC toma para enviar una llamada a procedimiento remoto a una rutina del administrador de servidores.

En las tablas siguientes se describe un caso simple en el que el servidor registra el administrador predeterminado EPV.

**Tabla del registro de la interfaz**



| UUID de interfaz | UUID de tipo de administrador | Vector de punto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Nulo               | EPV predeterminado        |



 

**Tabla del registro de objetos**



| UUID del objeto             | Tipo de objeto |
|-------------------------|-------------|
| Nulo                     | Nulo         |
| (Cualquier otro UUID del objeto) | Nulo         |



 

**Asignar el identificador de enlace a un vector de punto de entrada (EPV)**



| UUID de interfaz (desde el identificador de enlace del cliente) | UUID del objeto (desde el identificador de enlace del cliente) | Tipo de objeto (de la tabla del registro de objetos) | Manager EPV (de la tabla del registro de la interfaz) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nulo                                      | Nulo                                      | EPV predeterminado                                 |
| Lo mismo que antes.                               | *uuidA*                                  | Nulo                                      | EPV predeterminado                                 |



 

En los pasos siguientes se describen las acciones que toma la biblioteca en tiempo de ejecución del servidor RPC, tal como se muestra en las tablas anteriores, cuando un cliente con la interfaz UUID *uuid1* la llama.

1.  El servidor llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar una interfaz que ofrece con el UUID del tipo de administrador Nil y con el administrador predeterminado generado por MIDL EPV. Esta llamada agrega una entrada en la tabla del registro de la interfaz. El UUID de la interfaz se encuentra en el parámetro *IfSpec* a.
2.  De forma predeterminada, la tabla del registro de objetos asocia todos los UUID de objeto con el tipo nulo UUID. En este ejemplo, el servidor no llama a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).
3.  La biblioteca en tiempo de ejecución del servidor recibe un código de procedimiento remoto que contiene el UUID de interfaz al que pertenece la llamada y el UUID del objeto del identificador de enlace de la llamada.

    Vea las siguientes entradas de referencia de función para obtener información sobre cómo se establece un UUID de objeto en un controlador de enlace:

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  Mediante el UUID de la interfaz de la llamada a procedimiento remoto, la biblioteca en tiempo de ejecución del servidor ubica el UUID de la interfaz en la tabla del registro de la interfaz.

    Si el servidor no registró la interfaz con [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2), la llamada a procedimiento remoto vuelve al autor de la llamada con una RPC \_ \_ desconocida si el código de estado es \_ .

5.  Mediante el UUID del objeto del identificador de enlace, la biblioteca en tiempo de ejecución del servidor ubica ese UUID del objeto en la tabla del registro de objetos. En este ejemplo, todos los objetos UUID se asignan al tipo de objeto Nil.
6.  La biblioteca en tiempo de ejecución del servidor ubica el tipo de administrador Nil en la tabla del registro de la interfaz.
7.  La combinación de la interfaz UUID y el tipo Nil en la tabla del registro de la interfaz se resuelve como el valor predeterminado de EPV, que contiene las rutinas del administrador de servidores que se ejecutarán para el UUID de interfaz encontrado en la llamada a procedimiento remoto.

Suponga que el servidor ofrece varias interfaces y varias implementaciones de cada interfaz, tal y como se describe en las tablas siguientes.

**Tabla del registro de la interfaz**



| UUID de interfaz | IDENTIFICADOR de tipo de administrador | Vector de punto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Nulo               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Tabla del registro de objetos**



| UUID del objeto      | Tipo de objeto |
|------------------|-------------|
| *uuidA*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *uuidD*          | *uuid3*     |
| *uuidE*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| Nulo              | Nulo         |
| (Cualquier otro UUID) | Nulo         |



 

**Asignar el identificador de enlace a un vector de punto de entrada**



| UUID de interfaz (desde el identificador de enlace del cliente) | UUID del objeto (desde el identificador de enlace del cliente) | Tipo de objeto (de la tabla del registro de objetos) | Manager EPV (de la tabla del registro de la interfaz) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nulo                                      | Nulo                                      | *epv1*                                      |
| *uuid1*                                     | *uuidA*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidD*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidE*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

En los pasos siguientes se describen las acciones que toma la biblioteca en tiempo de ejecución del servidor, como se muestra en las tablas anteriores cuando un cliente con la interfaz UUID *uuid2* y el UUID del objeto *uuidC* la llama.

1.  El servidor llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar las interfaces que ofrece con la EPVs de administrador diferente. Las entradas de la tabla del registro de la interfaz reflejan cuatro llamadas a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para ofrecer dos interfaces, con dos implementaciones (EPVs) para cada interfaz.
2.  El servidor llama a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para establecer el tipo de cada objeto que ofrece. Además de la Asociación predeterminada del objeto Nil a un tipo Nil, el otro UUID del objeto no encontrado explícitamente en la tabla del registro de objetos también se asigna al UUID de tipo Nil.

    En este ejemplo, el servidor llama a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) seis veces.

3.  La biblioteca en tiempo de ejecución del servidor recibe una llamada a procedimiento remoto que contiene el UUID de interfaz al que pertenece la llamada y un UUID del objeto desde el identificador de enlace de la llamada.
4.  Con la interfaz UUID de la llamada a procedimiento remoto, la biblioteca en tiempo de ejecución del servidor ubica el UUID de la interfaz en la tabla del registro de la interfaz.
5.  Con el UUID del objeto *uuidC* del identificador de enlace, la biblioteca en tiempo de ejecución del servidor busca el UUID del objeto en la tabla del registro de objetos y encuentra que se asigna al tipo *uuid7*.
6.  Para buscar el tipo de administrador, la biblioteca en tiempo de ejecución del servidor combina la interfaz UUID, *uuid2* y el tipo *uuid7* en la tabla del registro de la interfaz. Se resuelve como *epv3*, que contiene la rutina del administrador del servidor que se va a ejecutar para la llamada a procedimiento remoto.

Las rutinas de *epv2* nunca se ejecutarán porque el servidor no ha llamado a la rutina [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para agregar objetos con un tipo UUID de *uuid4* a la tabla del registro de objetos.

Una llamada a procedimiento remoto con la interfaz UUID *uuid2* y el UUID del objeto *uuidF* vuelve al autor de la llamada con un código de estado de tipo de admin. RPC \_ \_ desconocido \_ \_ porque el servidor no llama a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para registrar la interfaz con un tipo de administrador de *uuid8*.

## <a name="return-values"></a>Valores devueltos

Esta función devuelve uno de los valores siguientes.



| Value                             | Significado                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ correcto                        | Correcto                      |
| el \_ tipo de RPC S \_ \_ ya está \_ registrado | Tipo UUID ya registrado |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Proporcionar su propia función de consulta de objeto

Considere un servidor que administra miles de objetos de muchos tipos diferentes. Cada vez que se inicia el servidor, la aplicación de servidor tendría que llamar a la función [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para cada uno de los objetos, aunque los clientes pueden hacer referencia a solo algunos de ellos (o tardan mucho tiempo en hacer referencia a ellos). Es probable que estos miles de objetos estén en el disco, por lo que recuperar sus tipos llevaría mucho tiempo. Además, la tabla interna que asigna el UUID del objeto al tipo de administrador UUID básicamente duplicaría la asignación que se mantiene con los propios objetos.

Para mayor comodidad, el conjunto de funciones RPC incluye la función [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn). Con esta función, debe proporcionar su propia función de consulta de objetos.

Por ejemplo, puede proporcionar su propia función de consulta de objeto al asignar los objetos 100 – 199 al tipo número 1, 200 – 299 al tipo número 2, y así sucesivamente. La función de consulta de objeto también se puede extender a un sistema de archivos distribuido, donde la aplicación de servidor no tiene una lista de todos los archivos (UUID de objeto) disponibles, o cuando el objeto UUID de objeto tiene archivos en el sistema de archivos y no desea cargar previamente todas las asignaciones entre el UUID de objeto y el tipo UUID.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 




