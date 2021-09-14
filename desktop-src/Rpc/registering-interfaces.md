---
title: Registrar interfaces
description: Registrar una interfaz de llamada a procedimiento remoto (RPC).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea9e851e8c9663c8f66d983d3400b1ee398a9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361902"
---
# <a name="registering-interfaces"></a>Registrar interfaces

En esta sección se presenta una explicación detallada del proceso de registro de una interfaz RPC.

La información de esta sección se presenta en los temas siguientes:

-   [Funciones de registro de interfaz](#interface-registration-functions)
-   [Vectores de punto de entrada](#entry-point-vectors)
-   [EPV de administrador](#manager-epvs)
-   [Registrar una implementación única de una interfaz](#registering-a-single-implementation-of-an-interface)
-   [Registrar varias implementaciones de una interfaz](#registering-multiple-implementations-of-an-interface)
-   [Reglas para invocar rutinas de administrador](#rules-for-invoking-manager-routines)
-   [Envío de una llamada a procedimiento remoto a una rutina Server-Manager ejecución](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Proporcionar su propia función Object-Inquiry aplicación](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Funciones de registro de interfaz

Los servidores registran sus interfaces mediante una llamada a [**la función RpcServerRegisterIf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) Los programas de servidor complejos suelen admitir más de una interfaz. Las aplicaciones de servidor deben llamar a esta función una vez para cada interfaz que admitan.

Además, los servidores pueden admitir varias versiones de la misma interfaz, cada una con su propia implementación de las funciones de la interfaz. Si el programa de servidor lo hace, debe proporcionar un conjunto de puntos de entrada. Un punto de entrada es una rutina de administrador que envía llamadas para una versión de una interfaz. Debe haber un punto de entrada para cada versión de la interfaz. El grupo de puntos de entrada se denomina vector de punto de entrada. Para obtener más información, [vea Vectores de punto de entrada](#entry-point-vectors).

Además de la función estándar [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)RPC también admite otras funciones de registro de interfaz. La función [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) amplía las funcionalidades de **RpcServerRegisterIf** al permitirle especificar un conjunto de marcas de registro (consulte Marcas de registro de interfaz), el número máximo de solicitudes de llamadas a procedimiento remoto simultáneas que el servidor puede aceptar y el tamaño máximo en bytes de bloques de datos [entrantes.](interface-registration-flags.md)

La biblioteca RPC también contiene una función denominada [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex). Al igual [**que la función RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) esta función registra una interfaz. El programa de servidor también puede usar esta función para especificar un conjunto de marcas de registro (vea Interface [Registration Flags](interface-registration-flags.md)), el número máximo de solicitudes de llamada simultáneas a procedimientos remotos que el servidor puede aceptar y una función de devolución de llamada de seguridad.

Las [**funciones RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)y [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) establecen valores en la tabla del Registro de interfaz interna. Esta tabla se usa para asignar el UUID de interfaz y los UUID de objeto a un EPV de administrador. El administrador EPV es una matriz de punteros de función que contiene exactamente un puntero de función para cada prototipo de función en la interfaz especificada en el archivo IDL.

Para obtener información sobre cómo proporcionar varios EPV para proporcionar varias implementaciones de la interfaz, vea [Implementaciones de varias interfaces](#registering-multiple-implementations-of-an-interface).

La biblioteca en tiempo de ejecución usa la tabla del Registro de interfaz (establecida por llamadas a la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2)**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)y la tabla del Registro de objetos (establecida por llamadas a la [**función RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) para asignar uuids de interfaz y objeto al puntero de función.

Si desea que el programa de servidor quite una interfaz del registro de biblioteca en tiempo de ejecución de RPC, llame a la [**función RpcServerUnregisterIf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) Después de quitar la interfaz del Registro, la biblioteca en tiempo de ejecución de RPC ya no aceptará nuevas llamadas para esa interfaz.

## <a name="entry-point-vectors"></a>Vectores de punto de entrada

El vector de punto de entrada (EPV) del administrador es una matriz de punteros de función que apuntan a implementaciones de las funciones especificadas en el archivo IDL. El número de elementos de la matriz corresponde al número de funciones especificadas en el archivo IDL. RPC admite varios vectores de punto de entrada que representan varias implementaciones de las funciones especificadas en la interfaz .

El compilador MIDL genera automáticamente un tipo de datos EPV de administrador para su uso en la construcción de EPV del administrador. El tipo de datos se denomina *if-name***\_ SERVER \_ EPV,** donde *if-name* especifica el identificador de interfaz en el archivo IDL.

El compilador MIDL crea e inicializa automáticamente un EPV de administrador predeterminado en la suposición de que existe una rutina de administrador con el mismo nombre para cada procedimiento de la interfaz y se especifica en el archivo IDL.

Cuando un servidor ofrece varias implementaciones de la misma interfaz, el servidor debe crear un EPV de administrador adicional para cada implementación. Cada EPV debe contener exactamente un punto de entrada (dirección de una función) para cada procedimiento definido en el archivo IDL. La aplicación de servidor declara e inicializa una variable EPV de administrador de tipo *if-name** \_ SERVER \_ EPV** para cada implementación adicional de la interfaz. Para registrar los EPV, llama a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) una vez para cada tipo de objeto que admita.

Cuando el cliente realiza una llamada a procedimiento remoto al servidor, el EPV que contiene el puntero de función se selecciona en función del UUID de interfaz y el tipo de objeto. El tipo de objeto se deriva del UUID del objeto mediante la función object-inquiry o la asignación controlada por tabla controlada por [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).

## <a name="manager-epvs"></a>EPV de administrador

De forma predeterminada, el compilador MIDL usa los nombres de procedimiento del archivo IDL de una interfaz para generar un EPV de administrador, que el compilador coloca directamente en el código auxiliar del servidor. Esta EPV predeterminada se inicializa estáticamente con los nombres de procedimiento declarados en la definición de interfaz.

Para registrar un administrador mediante el EPV predeterminado, especifique **NULL** como valor del parámetro *MgrEpv* en una llamada a la función [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) Si los nombres de rutina usados por un administrador corresponden a los de la definición de interfaz, puede registrar este administrador mediante el EPV predeterminado de la interfaz generada por el compilador MIDL. También puede registrar un administrador mediante un EPV que la aplicación de servidor proporciona.

Un servidor puede (y a veces debe) crear y registrar un EPV de **administrador** que no sea null para una interfaz. Para seleccionar una EPV proporcionada por una aplicación de servidor, pase la dirección de un EPV cuyo valor haya declarado el servidor como el valor de *MgrEpv* como parámetro. Un valor **distinto de NULL** para *MgrEpv,* un parámetro siempre invalida un EPV predeterminado en el código auxiliar del servidor.

El compilador MIDL genera automáticamente un tipo de datos EPV de administrador (RPC MGR EPV) para que una aplicación de servidor la use en la construcción \_ \_ de EPV del administrador. Un EPV de administrador debe contener exactamente un punto de entrada (dirección de función) para cada procedimiento definido en el archivo IDL.

Un servidor debe proporcionar un EPV que no sea **nulo** en los casos siguientes:

-   Cuando los nombres de las rutinas de administrador difieren de los nombres de procedimiento declarados en la definición de interfaz
-   Cuando el servidor usa el EPV predeterminado para registrar otra implementación de la interfaz

Un servidor declara un EPV de administrador inicializando una variable de tipo *if-name** \_ SERVER \_ EPV** para cada implementación de la interfaz.

## <a name="registering-a-single-implementation-of-an-interface"></a>Registrar una implementación única de una interfaz

Cuando un servidor ofrece solo una implementación de una interfaz, el servidor llama a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) solo una vez. En el caso estándar, el servidor usa el EPV de administrador predeterminado. (La excepción es cuando el administrador usa nombres de rutina que difieren de los declarados en la interfaz ).

En el caso estándar, proporcione los siguientes valores para las llamadas a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2):

-   EPV de administrador

    Para usar el EPV predeterminado, especifique un **valor NULL** para el *parámetro MgrEpv.*

-   UUID de tipo administrador

    Al usar el EPV predeterminado, registre la interfaz con un UUID de tipo administrador nulo; para ello, proporcione un valor **NULL** o un UUID nulo para *el parámetro MgrTypeUuid.* En este caso, todas las llamadas a procedimiento remoto, independientemente del UUID del objeto en su identificador de enlace, se envían al EPV predeterminado, suponiendo que no se haya realizado ninguna llamada [**RpcObjectSetType.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)

    También puede proporcionar un UUID de tipo administrador no nulo. En este caso, también debe llamar a la [**rutina RpcObjectSetType.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)

## <a name="registering-multiple-implementations-of-an-interface"></a>Registrar varias implementaciones de una interfaz

Puede proporcionar más de una implementación de los procedimientos remotos especificados en el archivo IDL. La aplicación de servidor llama a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para asignar UUID de objeto al tipo UUID y llama a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar los EPV del administrador a un UUID de tipo. Cuando llega una llamada a procedimiento remoto con su UUID de objeto, la biblioteca en tiempo de ejecución del servidor RPC asigna el UUID del objeto a un UUID de tipo. A continuación, la aplicación de servidor usa el tipo UUID y el UUID de interfaz para seleccionar el EPV del administrador.

También puede especificar su propia función para resolver la asignación del UUID del objeto al tipo de administrador UUID. La función de asignación se especifica al llamar a [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn).

Para ofrecer varias implementaciones de una interfaz, un servidor debe registrar cada implementación llamando a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2 por**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) separado. Para cada implementación que registra un servidor, proporciona el mismo *parámetro IfSpec,* pero un par diferente de *parámetros MgrTypeUuid* y *MgrEpv.*

En el caso de varios administradores, use [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) como se indica a continuación:

-   EPV de administrador

    Para ofrecer varias implementaciones de una interfaz, un servidor debe:

    -   Cree un EPV **de** administrador que no sea null para cada implementación adicional.
    -   Especifique un valor distinto de **NULL** para *MgrEpv,* un parámetro en [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)

    Tenga en cuenta que el servidor también puede registrarse con el EPV del administrador predeterminado.

-   UUID de tipo administrador

    Proporcione un UUID de tipo administrador para cada EPV de la interfaz. El UUID de tipo  nulo (o valor NULL) para *MgrTypeUuid,* se puede especificar un parámetro para uno de los EPV del administrador. Cada UUID de tipo debe ser diferente.

## <a name="rules-for-invoking-manager-routines"></a>Reglas para invocar rutinas de administrador

La biblioteca rpc en tiempo de ejecución envía una llamada a procedimiento remoto entrante a un administrador que ofrece la interfaz RPC solicitada. Cuando se registran varios administradores para una interfaz, la biblioteca en tiempo de ejecución de RPC debe seleccionar uno de ellos. Para seleccionar un administrador, la biblioteca en tiempo de ejecución de RPC usa el UUID del objeto especificado por el identificador de enlace de la llamada.

La biblioteca en tiempo de ejecución aplica las siguientes reglas al interpretar el UUID del objeto de una llamada a procedimiento remoto:

-   UUID de objeto nulo

    A un UUID de objeto nulo se le asigna automáticamente el UUID de tipo nulo (no es posible especificar un UUID de objeto nulo en la [**rutina RpcObjectSetType).**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) Por lo tanto, una llamada a procedimiento remoto cuyo identificador de enlace contiene un UUID de objeto nulo se envía automáticamente al administrador registrado con el UUID de tipo nulo, si existe.

-   UUID de objeto no nulo

    En principio, un administrador debe procesar una llamada a procedimiento remoto cuyo identificador de enlace contiene un UUID de objeto no nulo cuyo tipo UUID coincide con el tipo del UUID del objeto. Sin embargo, la identificación del administrador correcto requiere que el servidor haya especificado el tipo de UUID de ese objeto llamando a la [**rutina RpcObjectSetType.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)

    Si un servidor no puede llamar a la [**rutina RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para un UUID de objeto no nulo, una llamada a procedimiento remoto para ese UUID de objeto va al EPV del administrador que proporciona llamadas a procedimiento remoto con un UUID de objeto nulo (es decir, el UUID de tipo nulo).

    Las llamadas a procedimiento remoto con un UUID de objeto no nulo en el identificador de enlace no se pueden ejecutar si el servidor asignó a ese UUID de objeto no nulo un UUID de tipo llamando a la rutina [**RpcObjectSetType,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pero no registró también un EPV de administrador para ese tipo UUID llamando a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) [**o RpcServerRegisterIf2.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)

En la tabla siguiente se resumen las acciones que usa la biblioteca en tiempo de ejecución para seleccionar la rutina de administrador.



| UUID de objeto de la llamada | ¿Tipo de conjunto de servidores para el UUID del objeto? | ¿Tipo EPV registrado en el servidor? | Acción de distribución                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nula                 | No aplicable                   | Sí                         | Usa el administrador con el UUID de tipo nulo.                                                                                                           |
| Nula                 | No es aplicable                   | No                          | Error (RPC \_ S \_ UNSUPPORTED \_ TYPE); rechaza la llamada a procedimiento remoto.                                                                              |
| No nulo             | Sí                              | Sí                         | Usa el administrador con el mismo tipo UUID.                                                                                                          |
| No nulo             | No                               | Omitido                     | Usa el administrador con el UUID de tipo nulo. Si no hay ningún administrador con el UUID de tipo nulo, error (RPC \_ S \_ UNSUPPORTEDTYPE); rechaza la llamada a procedimiento remoto. |
| No nulo             | Sí                              | No                          | Error (RPC \_ S \_ UNSUPPORTEDTYPE); rechaza la llamada a procedimiento remoto.                                                                                |



 

El UUID del objeto de la llamada es el UUID del objeto que se encuentra en un identificador de enlace para una llamada a procedimiento remoto.

El servidor establece el tipo del UUID del objeto llamando a [**RpcObjectSetType para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) especificar el tipo UUID de un objeto.

El servidor registra el tipo para el EPV del administrador mediante una llamada a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) con el mismo uuid de tipo.

> [!Note]  
> Al UUID de objeto nulo siempre se le asigna automáticamente el UUID de tipo nulo. No es posible especificar un UUID de objeto nulo en la [**rutina RpcObjectSetType.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Envío de una llamada a procedimiento remoto a una rutina del administrador del servidor

En las tablas siguientes se muestran los pasos que realiza la biblioteca rpc en tiempo de ejecución para enviar una llamada a procedimiento remoto a una rutina de administrador del servidor.

Un caso sencillo en el que el servidor registra el EPV del administrador predeterminado, se describe en las tablas siguientes.

**Tabla del Registro de interfaz**



| UUID de interfaz | UUID de tipo de administrador | Vector de punto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Nula               | EPV predeterminada        |



 

**Tabla del Registro de objetos**



| UUID de objeto             | Tipo de objeto |
|-------------------------|-------------|
| Nula                     | Nula         |
| (Cualquier otro UUID de objeto) | Nula         |



 

**Asignación del identificador de enlace a un vector de punto de entrada (EPV)**



| UUID de interfaz (desde el identificador de enlace de cliente) | UUID de objeto (desde el identificador de enlace de cliente) | Tipo de objeto (de la tabla del Registro de objetos) | EPV de administrador (desde la tabla del Registro de interfaz) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nula                                      | Nula                                      | EPV predeterminada                                 |
| Lo mismo que antes.                               | *uuidA*                                  | Nula                                      | EPV predeterminada                                 |



 

En los pasos siguientes se describen las acciones que la biblioteca en tiempo de ejecución del servidor RPC lleva a cabo, como se muestra en las tablas anteriores, cuando un cliente con *uuid1 uuid1* de interfaz lo llama.

1.  El servidor llama a [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar una interfaz que ofrece con el UUID de tipo de administrador nulo y con el EPV del administrador predeterminado generado por MIDL. Esta llamada agrega una entrada en la tabla del Registro de interfaz. El UUID de la interfaz se encuentra en el *parámetro IfSpec.*
2.  De forma predeterminada, la tabla del Registro de objetos asocia todos los UUID de objeto con el UUID de tipo nulo. En este ejemplo, el servidor no llama a [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).
3.  La biblioteca en tiempo de ejecución del servidor recibe un código de procedimiento remoto que contiene el UUID de interfaz al que pertenece la llamada y el UUID del objeto del identificador de enlace de la llamada.

    Vea las siguientes entradas de referencia de función para obtener información sobre cómo se establece un UUID de objeto en un identificador de enlace:

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  Mediante el UUID de la interfaz de la llamada a procedimiento remoto, la biblioteca en tiempo de ejecución del servidor busca ese UUID de interfaz en la tabla del Registro de interfaz.

    Si el servidor no registró la interfaz mediante [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2), la llamada al procedimiento remoto devuelve al autor de la llamada con un código de estado IF DESCONOCIDO de \_ \_ \_ RPC.

5.  Con el UUID del objeto del identificador de enlace, la biblioteca en tiempo de ejecución del servidor busca ese UUID de objeto en la tabla del Registro de objetos. En este ejemplo, todos los UUD de objeto se asignan al tipo de objeto nulo.
6.  La biblioteca en tiempo de ejecución del servidor busca el tipo de administrador nulo en la tabla del Registro de interfaz.
7.  La combinación del UUID de interfaz y el tipo nulo en la tabla del Registro de interfaz se resuelve en el EPV predeterminado, que contiene las rutinas del administrador del servidor que se van a ejecutar para el UUID de interfaz que se encuentra en la llamada a procedimiento remoto.

Suponga que el servidor ofrece varias interfaces y varias implementaciones de cada interfaz, como se describe en las tablas siguientes.

**Tabla del Registro de interfaz**



| UUID de interfaz | UUID de tipo administrador | Vector de punto de entrada |
|----------------|-------------------|--------------------|
| *uuid1*        | Nula               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Tabla del Registro de objetos**



| UUID de objeto      | Tipo de objeto |
|------------------|-------------|
| *uuidA*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *uuidD*          | *uuid3*     |
| *uuidE*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| Nula              | Nula         |
| (Cualquier otro UUID) | Nula         |



 

**Asignación del identificador de enlace a un vector de punto de entrada**



| UUID de interfaz (desde el identificador de enlace de cliente) | UUID de objeto (desde el identificador de enlace de cliente) | Tipo de objeto (de la tabla del Registro de objetos) | EPV de administrador (desde la tabla del Registro de interfaz) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Nula                                      | Nula                                      | *epv1*                                      |
| *uuid1*                                     | *uuidA*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidD*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *uuidE*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

En los pasos siguientes se describen las acciones que la biblioteca en tiempo de ejecución del servidor lleva a cabo, como se muestra en las tablas anteriores cuando un cliente con *uuid2* de interfaz y *uuidC* de objeto lo llama.

1.  El servidor llama [**a RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para asociar las interfaces que ofrece a los diferentes EPV de administrador. Las entradas de la tabla del Registro de interfaz reflejan cuatro llamadas de [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para ofrecer dos interfaces, con dos implementaciones (EPV) para cada interfaz.
2.  El servidor llama [**a RpcObjectSetType para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) establecer el tipo de cada objeto que ofrece. Además de la asociación predeterminada del objeto nulo a un tipo nulo, todos los demás UUID de objeto no encontrados explícitamente en la tabla del Registro de objetos también se asignan al UUID de tipo nulo.

    En este ejemplo, el servidor llama a la [**rutina RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) seis veces.

3.  La biblioteca en tiempo de ejecución del servidor recibe una llamada a procedimiento remoto que contiene el UUID de interfaz al que pertenece la llamada y un UUID de objeto del identificador de enlace de la llamada.
4.  Con el UUID de interfaz de la llamada a procedimiento remoto, la biblioteca en tiempo de ejecución del servidor busca el UUID de interfaz en la tabla del Registro de interfaz.
5.  Con *el UUID del objeto uuidC* del identificador de enlace, la biblioteca en tiempo de ejecución del servidor busca el UUID del objeto en la tabla del Registro de objetos y encuentra que se asigna al tipo *uuid7*.
6.  Para buscar el tipo de administrador, la biblioteca en tiempo de ejecución del servidor combina la interfaz UUID, *uuid2* y el tipo *uuid7* en la tabla del Registro de interfaz. Esto se resuelve en *epv3,* que contiene la rutina del administrador del servidor que se va a ejecutar para la llamada a procedimiento remoto.

Las rutinas de *epv2* nunca se ejecutarán porque el servidor no ha llamado a la [**rutina RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para agregar objetos con un UUID de tipo *uuid4* a la tabla del Registro de objetos.

Una llamada a procedimiento remoto con la interfaz UUID *uuid2 y uuidF* del objeto *uuidF* devuelve al autor de la llamada con un código de estado RPC S UNKNOWN MGR TYPE porque el servidor no llamó \_ a \_ \_ \_ [**RpcServerRegisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)o [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) para registrar la interfaz con un tipo de administrador *de uuid8.*

## <a name="return-values"></a>Valores devueltos

Esta función devuelve uno de los valores siguientes.



| Value                             | Significado                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ OK                        | Correcto                      |
| TIPO \_ RPC S YA \_ \_ \_ REGISTRADO | Tipo UUID ya registrado |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Proporcionar su propia función de consulta de objetos

Considere un servidor que administra miles de objetos de muchos tipos diferentes. Cada vez que se inicia el servidor, la aplicación de servidor tendría que llamar a la función [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) para cada uno de los objetos, aunque los clientes solo pudieran hacer referencia a algunos de ellos (o tardar mucho tiempo en hacer referencia a ellos). Es probable que estos miles de objetos estén en el disco, por lo que recuperar sus tipos requeriría mucho tiempo. Además, la tabla interna que asigna el UUID del objeto al tipo de administrador UUID básicamente duplicaría la asignación mantenida con los propios objetos.

Para mayor comodidad, el conjunto de funciones RPC incluye la [**función RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn). Con esta función, proporciona su propia función de consulta de objetos.

Por ejemplo, puede proporcionar su propia función de consulta de objetos al asignar objetos del 100 al 199 al tipo número 1, 200-299 al tipo número 2, y así sucesivamente. La función de consulta de objetos también se puede extender a un sistema de archivos distribuido, donde la aplicación de servidor no tiene una lista de todos los archivos (UUID de objeto) disponibles, o cuando los UUD del objeto nombren archivos en el sistema de archivos y no desea cargar previamente todas las asignaciones entre UUD de objeto y UUD de tipo.

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

 

 




