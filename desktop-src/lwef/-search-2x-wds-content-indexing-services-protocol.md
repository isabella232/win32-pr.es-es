---
title: Protocolo de servicios de indexación de contenido
description: Este documento es una especificación del protocolo content indexing Service.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df48db5dd1b19983b12daeb6747dce92eedcd78674553f11af2e335f08e7de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481145"
---
# <a name="content-indexing-services-protocol"></a>Protocolo de servicios de indexación de contenido

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Especificación de protocolo, versión 0.12

-   [1 Introducción](#1-introduction)
    -   [1.1 Glosario](#11-glossary)
    -   [1.2 Referencias](#12-references)
    -   [Introducción al protocolo 1.3 (Synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Relación con otros protocolos](#14-relationship-to-other-protocols)
    -   [1.5 Requisitos previos y condiciones previas](#15-prerequisites-and-preconditions)
    -   [1.6 Declaración de aplicabilidad](#16-applicability-statement)
    -   [1.7 Control de versiones y negociación de funcionalidad](#17-versioning-and-capability-negotiation)
    -   [1.8 Campos extensibles por el proveedor](#18-vendor-extensible-fields)
    -   [1.9 Asignaciones de estándares](#19-standards-assignments)
-   [2 Mensajes](#2-messages)
    -   [2.1 Transporte](#21-transport)
    -   [2.2 Sintaxis de mensajes](#22-message-syntax)
-   [3 Detalles del protocolo](#3-protocol-details)
    -   [3.1 Detalles del servidor](#31-server-details)
    -   [3.2 Detalles del cliente](#32-client-details)
-   [4 Ejemplos de protocolo](#4-protocol-examples)
    -   [4.1 Ejemplo 1](#41-example-1)
    -   [4.2 Ejemplo 2](#42-example-2)
-   [5 Seguridad](#5-security)
    -   [5.1 Consideraciones de seguridad para los implementadores](#51-security-considerations-for-implementers)
    -   [5.2 Índice de parámetros de seguridad](#52-index-of-security-parameters)
-   [6 Índice del comportamiento específico de la versión](#6-index-of-version-specific-behavior)

Este documento es una especificación del protocolo content indexing Service.

La documentación del Programa de protocolo de servidor de grupo de trabajo (WSPP) está pensada para usarse junto con la documentación de estándares públicos, el arte de programación de red y los conceptos de sistemas distribuidos de grupo de trabajo de Windows, y supone que el lector está familiarizado con el material mencionado anteriormente o tiene acceso inmediato a él.

Una especificación del protocolo WSPP no requiere el uso de herramientas de programación o entornos de programación de Microsoft para que un licenciado desarrolle una implementación. Los licencias que tienen acceso a entornos y herramientas de programación de Microsoft son libres de aprovecharlas.

## <a name="1-introduction"></a>1 Introducción

-   [1.1 Glosario](#11-glossary)
-   [1.2 Referencias](#12-references)
-   [Introducción al protocolo 1.3 (Synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Relación con otros protocolos](#14-relationship-to-other-protocols)
-   [1.5 Requisitos previos y condiciones previas](#15-prerequisites-and-preconditions)
-   [1.6 Declaración de aplicabilidad](#16-applicability-statement)
-   [1.7 Control de versiones y negociación de funcionalidad](#17-versioning-and-capability-negotiation)
-   [1.8 Campos extensibles por el proveedor](#18-vendor-extensible-fields)
-   [1.9 Asignaciones de estándares](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glosario

> [!Note]  
> Los términos siguientes se definen en la sección Glosario de \[ MS-SYS \] :
>
> -   GUID
> -   Little Endian
> -   Canalización con nombre
> -   Ruta de acceso

 

**Enlace:** solicitud para incluir una columna determinada **en** un conjunto de **filas devuelto.** El **enlace** especifica una propiedad que se va a incluir en los resultados de búsqueda.

**Marcador:** marcador que identifica de forma única una fila dentro de un conjunto de filas.

**Catálogo:** unidad de nivel superior de la organización en el servicio de indexación. Representa un conjunto de documentos indexados en los que se pueden ejecutar consultas mediante el protocolo content indexing Service.

**Categoría:** una agrupación jerárquica de filas. Por ejemplo, un resultado de consulta que contiene columnas de autor y título se puede clasificar en función del autor. Cada grupo de filas que contiene el mismo valor para author constituiría una categoría.

**Capítulo:** intervalo de **filas dentro** de un conjunto de **filas** .

**Columna**: contenedor de un único tipo de información de una **fila.** Las columnas se asignan a nombres de propiedad y especifican qué propiedades se usan para los elementos del árbol **de** comandos de la consulta **de** búsqueda.

**Árbol de comandos:** combinación de **restricciones,** **categorías** **y** criterios de ordenación especificados para la consulta de búsqueda.

**Cursor:** una entidad que se usa como  mecanismo para trabajar  con una fila o un pequeño bloque de filas a la vez en un conjunto de datos devuelto en un conjunto de resultados. Un **cursor** se coloca en una sola **fila dentro** del conjunto de resultados. Una vez **que el cursor** se coloca en una fila, se pueden realizar operaciones en esa fila o en un bloque de filas a partir de esa posición.  

**Identificador:** token que se puede usar para identificar y acceder a **cursores,** **capítulos** y **marcadores.**

**Índice:** estructura persistente que contiene el contenido de texto que un servicio de indexación extrayó de **los archivos.** Esto incluye la lista de palabras, que se almacenan junto con el nombre de archivo que contiene, la ubicación de la palabra y **la configuración regional.**

**Indexación:** proceso de extracción de texto y propiedades de archivos y almacenamiento de los valores extraídos en los índices **(para** texto) y la caché de propiedades **(para** propiedades).

**Servicio de indexación:** servicio que crea **catálogos indexados** para el contenido y las propiedades de los sistemas de archivos. Las aplicaciones pueden buscar en los catálogos información de los archivos del sistema de archivos indizado.

**Configuración regional:** identificador, como se especifica en el Apéndice A de \[ MS-GPSI, que especifica \] las preferencias relacionadas con el idioma. Estas preferencias indican cómo se va a dar formato a las fechas y horas, los elementos se ordenan alfabéticamente, las cadenas se van a comparar, y así sucesivamente.

**Consulta de lenguaje natural:** consulta construida con lenguaje humano en lugar de sintaxis de consulta.

**Palabra ruido:** palabra que el servicio de indexación omite cuando está presente en las **restricciones especificadas** para la consulta de búsqueda porque tiene poco valor discriminatorio. Entre los ejemplos en inglés se incluyen "a", "and" y "the".

**Caché de propiedades:** caché de propiedades de archivo extraídas por un **servicio de indexación.**

**Indexación de** propiedades: proceso  de  creación de un índice de propiedades de tipo de valor de un documento, incluidos el autor, el asunto, el tipo, el recuento de palabras, el recuento de páginas impresas y cualquier otra propiedad.

**Restricción:** conjunto de condiciones que un archivo debe cumplir para incluirse en los resultados de búsqueda devueltos por el servicio **de indexación** en respuesta a una consulta de búsqueda. Una **restricción** limita el foco de una consulta de búsqueda, limitando los archivos que el servicio de **indexación** incluirá en los resultados de búsqueda a solo aquellos que coincidan con las condiciones.

**Fila:** colección de columnas **que** contiene los valores de propiedad que describen un único archivo del conjunto de archivos que coincidieron con las **restricciones especificadas** en la consulta de búsqueda enviada al servicio **de indexación.**

**Conjunto de filas:** conjunto de **filas devuelto en** los resultados de la búsqueda.

**Criterio de** ordenación: conjunto de reglas de una consulta de búsqueda que definen el orden de las filas en el resultado de la búsqueda. Cada regla consta de una propiedad (nombre, tamaño, etc.) y una dirección para la ordenación (ascendente o descendente). Varias reglas se aplican secuencialmente

**Propiedad de tipo de texto:** propiedad que describe el contenido de un documento y solo tiene texto sin formato asociado a su nombre.

**Propiedad de tipo de valor:** propiedad que describe un único atributo de un documento completo. Una propiedad de tipo de valor tiene un identificador de tipo de datos y un valor de ese tipo de datos asociado a su nombre.

**Raíz virtual:** ruta de acceso alternativa a una carpeta. Una carpeta física puede tener cero o más raíces virtuales. Las rutas de acceso que comienzan con una raíz virtual se denominan rutas de acceso virtuales. Por ejemplo, /server/vanityroot podría ser una raíz virtual de C: \\ carpeta \\ web de \\ IIS1. A continuación, el archivo C: carpeta web de IIS1default.htm una ruta de acceso \\ \\ virtual de \\ \\ /server/vanityroot/default.htm.

**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** estos términos (en todos los límites) se usan como se describe en \[ RFC2119 \] . Todas las instrucciones de comportamiento opcional utilizan MAY, SHOULD o SHOULD NOT.

### <a name="12-references"></a>1.2 Referencias

### <a name="121-normative-references"></a>1.2.1 Referencias de normativa

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, octubre de 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", junio de 2006.

\[MS-GPSI \] Microsoft Corporation, "Directiva de grupo de Instalación de software Extension", junio de 2006.

\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", mayo de 2006.

\[MS-SYS \] Microsoft Corporation, "System Overview v4", julio de 2006.

\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.

\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Referencias informativas

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>Introducción al protocolo 1.3 (Synopsis)

Un servicio **de indexación de contenido** ayuda a organizar de forma eficaz las características extraídas de una colección de documentos. El Protocolo de servicio de indexación de contenido (CISP) permite a un cliente comunicarse con un servidor que hospeda un servicio de indexación para emitir consultas y permitir que un administrador administre el servidor de indexación.

Al procesar archivos, un servicio de indexación analiza un conjunto de documentos  y reorganiza su contenido de forma que las propiedades de esos documentos se puedan devolver de forma eficaz en respuesta a las consultas. Una colección de documentos que se pueden consultar consta de un **catálogo .** Un catálogo puede contener un **índice (para** referencia rápida al texto) y una caché de **propiedades** (para la recuperación rápida de valores de propiedad).

Conceptualmente, un catálogo consta de una "tabla" lógica de propiedades con el texto o el valor y la configuración regional correspondiente almacenada en **columnas** de la tabla. Cada "fila" de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada "columna" de la tabla corresponde a una propiedad .

Las tareas específicas realizadas por CISP se agrupan en dos áreas funcionales:

-   Administración remota de catálogos de servicios de indexación,
-   Consulta remota de catálogos de servicios de indexación.

### <a name="131-remote-administration-tasks"></a>1.3.1 Tareas de administración remota

CISP habilita las siguientes tareas de administración del catálogo de servicios de indexación desde un cliente:

-   Consulte el estado actual de un catálogo de servicios de indexación en el servidor.
-   Actualice el estado de un catálogo de servicios de indexación.
-   Inicie el proceso de indexación para un conjunto determinado de archivos.
-   Inicie la optimización de un índice para mejorar el rendimiento de las consultas.

Todas las tareas de administración remota siguen un modelo sencillo de solicitud/respuesta. No se mantiene ningún estado en el cliente para ninguna llamada de administración y se pueden realizar llamadas administrativas en cualquier orden.

### <a name="132-remote-querying"></a>1.3.2 Consulta remota

CISP permite a los clientes realizar consultas de búsqueda en un servidor remoto que hospeda un servicio de indexación.

El envío de una consulta de búsqueda es un proceso de varios pasos iniciado por el cliente. Los pasos son los siguientes:

1.  El cliente solicita una conexión a un servidor que hospeda un servicio de indexación.
2.  El cliente envía los parámetros para la consulta de búsqueda, que incluyen:
    -   Restricciones para especificar qué documentos se van a incluir o excluir de los **resultados** de la búsqueda.
    -   Orden en el que se van a devolver los resultados de la búsqueda.
    -   Columnas que se devolverán en el conjunto de resultados.
    -   Número máximo de **filas que** se deben devolver para la consulta.
    -   Tiempo máximo para la ejecución de consultas.

        Una vez que el servidor ha reconocido la solicitud del cliente para iniciar la consulta, el cliente puede solicitar información de estado sobre la consulta, pero este no es un paso necesario.

3.  A continuación, el cliente especifica qué propiedades debe incluir el servidor en los resultados de la búsqueda.
4.  El cliente solicita un conjunto de resultados del servidor y el servidor responde enviando al cliente los valores de propiedad de los archivos incluidos en los resultados de la consulta de búsqueda del cliente. Si el valor de una propiedad es demasiado grande para caber en un búfer de respuesta único, el servidor no enviará la propiedad, sino que establecerá el estado de la propiedad en diferido. A continuación, el cliente solicita el valor de propiedad por separado mediante una serie de solicitudes para fragmentos sucesivos del valor y, a continuación, reanuda la solicitud de otros valores.
5.  Una vez que el cliente ha finalizado con la consulta de búsqueda y ya no requiere resultados adicionales, el cliente se pone en contacto con el servidor para liberar la consulta.
6.  Una vez que el servidor ha publicado la consulta, el cliente puede enviar una solicitud para desconectarse del servidor. A continuación, se cierra la conexión. Como alternativa, el cliente puede emitir otra consulta y repetir la secuencia del paso 2.

Windows Comportamiento: este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relación con otros protocolos

CISP se basa en el protocolo \[ SMB MS-SMB \] para el transporte de mensajes. Ningún otro protocolo depende directamente del protocolo del servicio de indexación de contenido.

*Windows Comportamiento: las aplicaciones normalmente interactúan con un contenedor de interfaz OLE DB \[ MSDN-OLEDB (por ejemplo, un cliente de protocolo) y no directamente \] con el protocolo.*

### <a name="15-prerequisites-and-preconditions"></a>1.5 Requisitos previos y condiciones previas

Se supone que el cliente ha obtenido el nombre del servidor y un nombre de catálogo antes de invocar este protocolo. La forma en que un cliente lo hace está fuera del ámbito de esta especificación.

También se supone que el cliente y el servidor tienen una asociación de seguridad que se puede usar con canalizaciones con \[ nombre MS-SMB. \]

### <a name="16-applicability-statement"></a>1.6 Declaración de aplicabilidad

CISP está diseñado para consultar y administrar catálogos en un servidor remoto desde un cliente. CISP está en desuso en Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Control de versiones y negociación de funcionalidad

Este protocolo no tiene mecanismos de control de versiones ni de negociación de funcionalidades.

### <a name="18-vendor-extensible-fields"></a>1.8 Campos extensibles por el proveedor

Este protocolo usa HULT que son extensibles por el proveedor. Los proveedores pueden elegir sus propios valores para este campo, siempre que el bit C (0x20000000) se establezca como se especifica en la sección 4.1.1 de MS-SYS, lo que indica que es un código de \[ \] cliente.

Este protocolo también usa valores NTSTATUS tomados del espacio numérico NTSTATUS definido en \[ MS-SYS \] . Los proveedores DEBEN reutilizar esos valores con su significado indicado. La elección de cualquier otro valor corre el riesgo de colisión en el futuro.

*Windows Comportamiento: Windows solo usa los valores especificados en la sección 4.1.3 \[ de MS-SYS \] .*

### <a name="181-property-ids"></a>1.8.1 IDs de propiedad

Las propiedades se representan mediante los ID conocidos como los de propiedad. Cada propiedad debe tener un identificador único global. Este identificador consta de un **GUID** que representa una colección de propiedades denominada conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto. Si se usa la forma de entero de id., los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE se consideran no válidos.

Los proveedores pueden garantizar que sus propiedades se definen de forma única colocándolas en un conjunto de propiedades definido por su propio GUID.

### <a name="19-standards-assignments"></a>1.9 Asignaciones de estándares

Este protocolo no tiene asignaciones de estándares, solo asignaciones privadas realizadas por Microsoft mediante procedimientos de asignación especificados en otros protocolos.

Microsoft ha asignado a este protocolo una canalización con nombre como se especifica \[ en MS-SMB. \] La asignación es:



| Parámetro | Valor             | Referencia  |
|-----------|-------------------|------------|
| Nombre de canalización | \\pipe \\ CI \_ PIPEDS | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 Mensajes

-   [2.1 Transporte](#21-transport)
-   [2.2 Sintaxis de mensajes](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transporte

Todos los mensajes DEBEN transportarse mediante una canalización con nombre, tal y como se especifica en \[ MS-SMB. \] Se usa el siguiente nombre de canalización:

-   \\pipe \\ CI \_ PIPEDS

Este protocolo usa el protocolo de canalización con nombre SMB subyacente para recuperar la identidad del autor de la llamada que realizó la conexión como se especifica en la sección 2.2.8 de MS-SMB; el cliente DEBE establecer SECURITY IDENTIFICATION como \[ \] ImpersonationLevel en la solicitud para abrir la canalización con \_ nombre.

### <a name="22-message-syntax"></a>2.2 Sintaxis de mensajes

Varias estructuras y mensajes de las secciones siguientes hacen referencia a los identificadores de capítulos o marcadores. Un identificador es una estructura opaca de 32 bits de longitud que identifica de forma única un capítulo o marcador. Normalmente, las aplicaciones cliente reciben valores de identificador a través de llamadas a métodos. sin embargo, hay varios valores conocidos que no es necesario obtener de un servidor, cuyo significado se especifica en la tabla siguiente:



| Valor                         | Significado                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| Db \_ NULL \_ HCHAPTER 0x00000000 | Identificador de capítulo para el conjunto de filas sin cadena que contiene todos los resultados de la consulta.    |
| DBBMK \_ FIRST 0x00000001       | Identificador de marcador de un marcador que identifica la primera fila del conjunto de filas. |
| DBBMK \_ LAST 0x00000002        | Identificador de marcador de un marcador que identifica la última fila del conjunto de filas.  |



 

### <a name="221-structures"></a>2.2.1 Estructuras

En esta sección se detallan las estructuras de datos definidas y usadas por CISP.

Todos los enteros de 2, 4 y 8 bytes con signo y sin signo de las estructuras siguientes DEBEN transferirse en orden de bytes little-endian.

En la tabla siguiente se resumen las estructuras de datos definidas en esta sección.



| Estructura                    | Descripción                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en una estructura CPropertyRestriction. |
| SAFEARRAY, SAFEARRAY2        | Contiene una matriz multidimensional.                                                                                     |
| SAFEARRAYBOUND               | Representa los límites de una dimensión de una matriz especificada en una estructura SAFEARRAY.                                  |
| CFullPropSpec                | Contiene una especificación de propiedad.                                                                                     |
| CContentRestriction          | Contiene una cadena que debe coincidir con un valor de propiedad en la caché de propiedades.                                                 |
| CKey                         | Contiene un valor de propiedad.                                                                                             |
| CInternalPropertyRestriction | Contiene un valor de propiedad que debe coincidir con una operación.                                                                  |
| CNatLanguageRestriction      | Contiene una coincidencia de consulta de lenguaje natural para una propiedad.                                                                |
| CNodeRestriction             | Contiene una matriz de nodos de árbol de comandos que especifican las restricciones de una consulta.                                       |
| COccRestriction              | Contiene la ubicación de una palabra en una frase.                                                                           |
| CPropertyRestriction         | Contiene un valor de propiedad que debe coincidir con una operación.                                                                  |
| CRangeRestriction            | Contiene una restricción en un intervalo de valores.                                                                           |
| CScopeRestriction            | Contiene una restricción en los archivos que se buscarán.                                                                    |
| CSort                        | Identifica una columna que se debe ordenar.                                                                                           |
| CSynRestriction              | Contiene una palabra o sus sinónimos para una frase de consulta.                                                                    |
| CVectorRestriction           | Contiene una operación OR ponderada en un nodo de árbol de comandos.                                                               |
| CWordRestriction             | Contiene una palabra para una frase de consulta.                                                                                    |
| CRestriction                 | Contiene un nodo de un árbol de comandos de consulta.                                                                               |
| CColumnSet                   | Indica el número de columnas que se devolverán.                                                                             |
| CCategorizationSet           | Contiene información sobre la agrupación de un conjunto de resultados de consulta.                                                     |
| CCategorizationSpec          | Contiene una definición de categorías en las que se clasificarán los resultados de la consulta.                                      |
| CDbColId                     | Contiene una columna.                                                                                                     |
| CDbProp                      | Contiene una propiedad .                                                                                                   |
| CDbPropSet                   | Contiene un conjunto de propiedades.                                                                                          |
| CPidMapper                   | Contiene una matriz de los nombres de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.                                     |
| CRowSeekAt                   | Contiene el desplazamiento en el que se van a recuperar las filas de un mensaje CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifica los marcadores de los que se van a recuperar filas para un mensaje CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.                                                         |
| CRowsetProperties            | Contiene la información de configuración de una consulta.                                                                    |
| CSortSet                     | Contiene el criterio de ordenación de una consulta.                                                                                   |
| CTableColumn                 | Contiene una columna para el mensaje CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contiene un valor serializado.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

La estructura CBaseStorageVariant contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en la estructura CPropertyRestriction.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (variable)



 

**vType:** un indicador de tipo que indica el tipo de vValue. DEBE ser uno de los valores VARENUM especificados en la tabla siguiente.



| Valor                 | Significado                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY (0x0000)    | vValue no está presente.                                                                                                               |
| VT \_ NULL (0x0001)     | vValue no está presente.                                                                                                               |
| VT \_ I1 (0x0010)       | Entero de 1 byte con signo.                                                                                                             |
| VT \_ UI1 (0x0011)      | Entero de 1 byte sin signo.                                                                                                           |
| VT \_ I2 (0x0002)       | Entero de 2 bytes con signo.                                                                                                             |
| VT \_ UI2 (0x0012)      | Entero de 2 bytes sin signo.                                                                                                           |
| VT \_ BOOL (0x000B)     | Valor booleano; entero de 2 bytes que contiene 0x0000 (FALSE) o 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Entero de 4 bytes con signo.                                                                                                             |
| VT \_ UI4 (0x0013)      | Entero de 4 bytes sin signo.                                                                                                           |
| VT \_ R4 (0x0004)       | Número de punto flotante ieee de 32 bits, tal como se define en \[ IEEE754. \]                                                                     |
| VT \_ INT (0x0016)      | Entero de 4 bytes con signo.                                                                                                             |
| VT \_ UINT (0x0017)     | Entero de 4 bytes sin signo.                                                                                                           |
| \_ERROR DE VT (0x000A)    | Entero de 4 bytes sin signo que contiene un valor HRESULT, tal como se especifica en \[ MS-SYS \] .                                                         |
| VT \_ I8 (0x0014)       | Entero de 8 bytes con signo.                                                                                                            |
| VT \_ UI8 (0x0015)      | Entero de 8 bytes sin signo.                                                                                                          |
| VT \_ R8 (0x0005)       | Número de punto flotante IEEE de 64 bits tal como se define en \[ IEEE754. \]                                                                      |
| VT \_ CY (0x0006)       | Entero complementario de dos bytes de 8 bytes (escalado en 10 000).                                                                               |
| VT \_ DATE (0x0007)     | Número de punto flotante de 64 bits que representa el número de días desde las 00:00:00 del 31 de diciembre de 1899 (hora universal coordinada).     |
| VT \_ FILETIME (0x0040) | Entero de 64 bits que representa el número de intervalos de 100 nanosegundos desde las 00:00:00 del 1 de enero de 1601 (hora universal coordinada). |
| VT \_ DECIMAL (0x000E)  | Estructura DECIMAL especificada en la sección 2.2.1.1.1.1.                                                                             |
| VT \_ CLSID (0x0048)    | Valor binario de 16 bytes que contiene un GUID.                                                                                            |
| \_BLOB DE VT (0x0041)     | Número entero sin signo de 4 bytes en el blob, seguido de muchos bytes de datos.                                           |
| VT \_ BSTR (0x0008)     | Número entero sin signo de 4 bytes de la cadena, seguido de una cadena, como se especifica a continuación en vValue.                       |
| VT \_ LPSTR (0x001E)    | Cadena ANSI terminada en NULL.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Cadena Unicode terminada en \[ \] NULL.                                                                                        |
| VT \_ VARIANT (0x000C)  | CBaseStorageVariant. DEBE combinarse con un modificador de tipo de VT \_ ARRAY o VT \_ VECTOR.                                               |



 

En la tabla siguiente se especifican los modificadores de tipo para vType. Los modificadores de tipo pueden ser binarios ORed con vType, para cambiar el significado de vValue para indicar que es uno de los dos tipos de matriz posibles.



| Valor               | Significado                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ VECTOR (0x1000) | Si el indicador de tipo se combina con VT VECTOR mediante un operador OR, vValue es una matriz con recuento de valores \_ del tipo indicado. Consulte la sección 2.2.1.1.1.2 para obtener más información. <br/> Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.<br/>                                    |
| VT \_ ARRAY (0x2000)  | Si un operador OR combina el indicador de tipo con VT ARRAY, el valor es SAFEARRAY (como se especifica en la sección \_ 2.2.1.1.1.3) que contiene valores del tipo indicado. <br/> Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR. <br/> |



 

**vData1:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Escala en la sección \_ 2.2.1.1.1.1. Para todos los demás vTypes, el valor DEBE establecerse en 0x00.

**vData2:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Sign en la sección \_ 2.2.1.1.1.1. Para todos los demás vTypes, el valor DEBE establecerse en 0x00.

**vValue:** el valor de la operación de coincidencia. La sintaxis DEBE ser como se indica en el campo vType.

En la tabla siguiente se resumen los tamaños del campo vValue, en función del campo vType para los tipos de datos de longitud fija. El tamaño es en bytes.



| vType                                                   | Size |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ BOOL                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME | 8    |
| VT \_ DECIMAL, VT \_ CLSID                                  | 16   |



 

Si vType se establece en \_ VT BLOB, VT BSTR o VT LPSTR, la estructura de vValue se \_ especifica en el diagrama \_ siguiente:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (variable, opcional)



 

**cbSize:** entero de 32 bits sin signo, que indica el tamaño del campo blobData en bytes. Si vType se establece en VT BSTR o \_ VT LPSTR, cbSize DEBE establecerse en 0x00000000 cuando la cadena representada \_ es una cadena vacía.

**blobData:** DEBE tener la longitud cbSize en bytes.

Para vType establecido en VT \_ BLOB, este campo son datos de blob binario opacos.

Para vType establecido en VT BSTR, este campo es un conjunto de caracteres en un \_ juego de caracteres seleccionado por OEM. El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo). No es necesario que se termine en null.

Para vType establecido en VT LPSTR, este campo es una cadena de caracteres terminada en NULL en un juego de caracteres \_ seleccionado por OEM. El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo).

Si vType se establece en VT \_ LPWSTR, la estructura de vValue se especifica en el diagrama siguiente:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

string (variable, opcional)



 

**ccLen:** entero de 32 bits sin signo, que indica el tamaño del campo de cadena en caracteres Unicode. DEBE establecerse en 0x00000000 para una cadena vacía.

**string**: cadena Unicode terminada en null.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 Estructuras CBaseStorageVariant

Las estructuras siguientes se usan en la estructura CBaseStorageVariant.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL se usa para representar un valor numérico exacto con una precisión fija y una escala fija.

Cuando vType se establece en VT DECIMAL (0x0000E), los campos \_ vData1 y vData2 de CBaseStorageVariant DEBEN interpretarse de la siguiente manera:

**vData1:** número de dígitos a la derecha del separador decimal. DEBE estar en el intervalo de 0 a 28.

**vData2:** signo del valor numérico. Establezca en 0x00 si es positivo, 0x80 si es negativo.

El formato del campo vValue es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mid32



 

**Hi32:** los 32 bits más altos del entero de 96 bits.

**Lo32:** los 32 bits más bajos del entero de 96 bits.

**Mid32:** los 32 bits centrales del entero de 96 bits.

### <a name="221112-vt_vector"></a>2.2.1.1.1.2 VECTOR DE VT \_

Vt \_ Vector se usa para pasar matrices unidimensionales.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements:** entero de 32 bits sin signo, que indica el número de elementos del campo vVectorData.

**vVectorData:** matriz de elementos que tienen un tipo indicado por vType con el 0x1000 bits desactivado. El tamaño de un elemento de longitud fija individual se puede obtener de la tabla de tipo de datos de longitud fija, como se especifica en la sección 2.2.1.1. La longitud de este campo, en bytes, se puede calcular multiplicando vVectorElements por el tamaño de un elemento individual.

Para los tipos de datos de longitud variable, vVectorData contiene una secuencia de tipos simples serializados consecutivamente donde vType indica el tipo con el 0x1000 bits desactivado. Esto incluye un caso especial indicado por vType VT \_ ARRAY \| VT VARIANT \_ (es decir, 0x100C).

Los elementos del campo vVectorData DEBEN estar separados por 0 a 3 bytes de relleno, de forma que cada elemento comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si hay bytes de relleno, el valor que contienen es arbitrario. El receptor DEBE omitir el contenido de los bytes de relleno.

Para un vType establecido en VT ARRAY VT VARIANT, el tipo para los elementos de \_ \| esta secuencia es \_ CBaseStorageVariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY se usa para pasar matrices multidimensionales. La estructura contiene información de tamaño de matriz, así como los datos de la matriz.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (variable)

vData (variable)



 

**cDims:** entero de 16 bits sin signo, que indica el número de dimensiones de la matriz multidimensional.

**fFeatures:** campo de bits de 16 bits. Los valores representan características, definidas por aplicaciones de capa superior y DEBEN omitirse.

**cbElements:** entero de 32 bits sin signo que especifica el tamaño de cada elemento de la matriz.

**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4, por dimensión en SAFEARRAY. Esta matriz tiene la dimensión más a la izquierda en primer lugar y la dimensión más a la derecha en último lugar.

**vData:** vector de elementos serializados de un tipo determinado, indicado por el vType del elemento que contiene CBaseStorageVariant, con el bit 0x2000 borrado.

vData se serializa de forma similar a VT VECTOR, como se especifica en la sección 2.2.1.1.1.2, con la diferencia de que el número de elementos no se almacena delante del \_ vector. En su lugar, el número de elementos se calcula multiplicando el valor cElements por todos los límites de matriz seguros especificados en el campo Rgsabound. Los elementos se almacenan en un vector en orden de dimensiones, iterando a partir de la dimensión más a la derecha.

El diagrama siguiente representa visualmente una matriz bidimensional de ejemplo. La primera dimensión tiene cElements igual a 4 (representado horizontalmente) y lLbound igual a 0, y la segunda dimensión tiene cElements igual a 2 (representado verticalmente) y lLbound igual a 0.

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

::row:::
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

Con el diagrama anterior, vData contendrá la siguiente secuencia: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterando primero por la dimensión situada más a la derecha y, a continuación, incrementando la dimensión siguiente). El Rgsabound anterior (que registra cElements y Lbound) sería: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

La estructura SAFEARRAYBOUND representa los límites de una dimensión de SAFEARRAY o SAFEARRAY2. Su formato es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements:** entero de 32 bits sin signo que especifica el número de elementos de la dimensión.

**lLbound:** entero de 32 bits sin signo que especifica el límite inferior de la dimensión.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 se usa para pasar matrices multidimensionales en SERIALIZEDPROPERTYVALUE. La estructura contiene información de límites, así como los datos.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (variable)

vData (variable)



 

**cDims:** entero de 32 bits sin signo, que indica el número de dimensiones de SAFEARRAY2.

**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4 por dimensión en SAFEARRAY2. Esta matriz tiene la dimensión más a la izquierda en primer lugar y la dimensión más a la derecha en último lugar.

**vData:** vector de elementos serializados de un tipo determinado, indicado por el dwType de que contiene SERIALIZEDPROPERTYVALUE, con valores de 0x2000 borrados. El formato de vData es el mismo que el especificado para el campo vData de SAFEARRAY en la sección 2.2.1.1.1.3.

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

La estructura CFullPropSpec contiene un GUID del conjunto de propiedades y un identificador de propiedad para identificar de forma única la propiedad.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

Nombre de propiedad (variable)



 

**\_ guidPropSet:** GUID del conjunto de propiedades al que pertenece la propiedad.

**ulKind:** entero de 32 bits sin signo. Uno de los siguientes valores, que indica el contenido de PrSpec.



| Valor                                            | Significado                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWSTR<br/> 0x00000000<br/> | El campo PrSpec especifica el número de caracteres que no son NULL en el campo Nombre de propiedad. |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | El campo PrSpec especifica el identificador de propiedad (PROPID).                                     |



 

**PrSpec:** entero de 32 bits sin signo con un significado indicado por el campo ulKind.

**Nombre de** propiedad: si ulKind se establece en PRSPEC \_ PROPID, este campo NO DEBE estar presente. Si ulKind se establece en PRSPEC LPWSTR, este campo DEBE contener una matriz sin mayúsculas y minúsculas de caracteres Unicode prSpec que no son null, que contiene el nombre de la \_ propiedad.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

La estructura CContentRestriction contiene una cadena que debe coincidir con una propiedad de la caché de propiedades.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Propiedad (variable)

...

Padding1 (variable)

CC

\_pwcsPhrase (variable)

...

Padding2 (variable)

lcid

\_ulGenerateMethod



 

**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.2. Este campo indica la propiedad en la que se va a realizar una operación de coincidencia.

**Padding1:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**Cc:** entero de 32 bits sin signo que especifica el número de caracteres en el \_ campo pwcsPhrase.

**\_ pwcsPhrase:** cadena Unicode no terminada en NULL que representa la palabra o frase que se debe coincidir con la propiedad . Este campo NO DEBE estar vacío. El campo Cc contiene la longitud de la cadena.

**Padding2:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**Lcid:** entero de 32 bits sin signo, que indica la configuración regional de pwcsPhrase, como se especifica en el Apéndice A de \_ \[ MS-GPSI. \]

**\_ ulGenerateMethod:** entero de 32 bits sin signo que especifica el método que se usará al generar formularios de palabras alternativos



| Valor                                                       | Significado                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GENERATE \_ METHOD \_ EXACT<br/> 0x00000000<br/>    | Coincidencia exacta.                                                                                                                                                                                                                                                                                      |
| GENERAR \_ PREFIJO DE \_ MÉTODO<br/> 0x00000001 <br/>  | Coincidencia de prefijo.                                                                                                                                                                                                                                                                                     |
| GENERATE \_ METHOD \_ INFLECT <br/> 0x00000002<br/> | Coincide con las inflexiones de una palabra. Una inflexión de una palabra es una variante de la palabra raíz en la misma parte de la voz que se ha modificado según las reglas lingüísticas de un idioma determinado. Por ejemplo, las inflexiones del verbo "nado" en inglés incluyen "nada", "nada", "nada" y "nada". |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

La estructura CKey contiene un valor de propiedad.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PROPID

Cb

buf (variable)



 

**PROPID:** entero de 32 bits sin signo que representa el identificador de propiedad como se describe en la sección 1.8.1. Los valores conocidos son:



| Valor      | Significado                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Representa un identificador de propiedad no válido y NO SE DEBE usar. |
| 0xFFFFFFFE | Representa un identificador de propiedad no válido y NO SE DEBE usar. |
| 0x00000000 | Representa cualquier identificador de propiedad.                             |



 

**Cb:** entero de 32 bits sin signo que contiene la longitud de buf, en bytes.

**buf:** secuencia de bytes que representa el valor de la propiedad .

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

La estructura CInternalPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_reeste

\_Pid

\_prval (variable)

restrictionPresent

nextRestriction (variable)



 

**\_ rehard:** entero de 32 bits que especifica la relación que se va a realizar en la propiedad . DEBE ser uno de los siguientes valores:



| Valor                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Una comparación menor que.                                                                                           |
| Prle 0x00000001       | Una comparación menor o igual que.                                                                               |
| PrGT 0x00000002       | Una comparación mayor que.                                                                                        |
| PRGE 0x00000003       | Una comparación mayor o igual que.                                                                            |
| Preq 0x00000004       | Comparación de igualdad.                                                                                           |
| PRNE 0x00000005       | Comparación no igual.                                                                                           |
| PRRE 0x00000006       | Comparación de expresiones regulares.                                                                                  |
| PRAllBits 0x00000007  | AND bit a bit que devuelve el operando derecho.                                                                     |
| PRSomeBits 0x00000008 | AND bit a bit que devuelve un valor distinto de cero.                                                                       |
| PRAll 0x00000100      | La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas. |
| PRAny 0x00000200      | La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.       |



 

**\_ pid:** entero de 32 bits sin signo que representa el identificador de propiedad (vea PROPID en la sección 2.2.1.4).

**\_ prval:** CBaseStorageVariant que contiene el valor que se debe relacionar con la propiedad .

**restrictionPresent:** valor de byte que indica si el campo nextRestriction está presente. DEBE establecerse en 0x00 o 0x01. Si se establece en 0x01, restrictionPresent indica que el campo nextRestriction está presente. Si se establece en 0x00, restrictionPresent indica que el campo nextRestriction no está presente.

**nextRestriction:** una estructura CRestriction, como se especifica en la sección 2.2.1.16, especificando una restricción adicional.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

La estructura CNatLanguageRestriction contiene una **coincidencia de consulta de lenguaje natural** para una propiedad.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Propiedad (variable)

...

\_padding \_ cc (variable)

CC

\_pwcsPhrase (variable)

...

\_padding \_ lcid (variable)

Lcid



 

**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.3. Este campo indica la propiedad en la que se va a realizar la operación de coincidencia.

**\_ padding \_ cc:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**Cc:** entero de 32 bits sin signo. Número de caracteres del campo \_ pwcsPhrase.

**\_ pwcsPhrase:** cadena Unicode no terminada en NULL que representa la palabra o frase que se debe coincidir con la propiedad . NO DEBE estar vacío. El campo Cc contiene la longitud de la cadena.

**\_ padding \_ lcid:** este campo DEBE tener entre 0 y 3 bytes de longitud. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**Lcid:** entero de 32 bits sin signo que indica la configuración regional de pwcsPhrase, como se especifica en el Apéndice A de \_ \[ MS-GPSI. \]

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

La estructura CNodeRestriction contiene una matriz de **nodos de árbol** de comandos que especifican las restricciones para la consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (variable)



 

**\_ cNode:** entero de 32 bits sin signo que especifica el número de estructuras de CRestriction contenidas en el \_ campo paNode.

**\_ paNode:** una matriz de estructuras de CRestriction. Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si hay bytes de relleno, el valor que contienen es arbitrario. El receptor DEBE omitir el contenido de los bytes de relleno.

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

La estructura COccRestriction contiene la ubicación de una palabra en una frase.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Occ

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ occ:** entero de 32 bits sin signo que especifica el desplazamiento de la palabra en una cadena de consulta, en unidades de palabras. Una palabra, como se usa en esta especificación, es una unidad de idioma en cualquier configuración regional que lleva significado.

**\_ cPrevNoiseWords:** entero de 32 bits sin signo  que contiene el número de palabras que se producen entre esta palabra y la palabra anterior de la frase.

**\_ cNextNoiseWords:** entero de 32 bits sin signo que contiene el número de palabras que se producen entre esta palabra y la siguiente palabra de la frase.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

La estructura CPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_volver a reestechar

\_Propiedad (variable)

\_prval (variable)



 

**\_ rehard:** entero de 32 bits sin signo que especifica la relación que se va a realizar en la propiedad . DEBE ser uno de los siguientes valores.



| Valor                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PrLT 0x00000000       | Una comparación menor que.                                                                                           |
| PRLE 0x00000001       | Comparación menor o igual que.                                                                               |
| PrGT 0x00000002       | Una comparación mayor que.                                                                                        |
| PRGE 0x00000003       | Una comparación mayor o igual que.                                                                            |
| Requisitos previos 0x00000004       | Comparación de igualdad.                                                                                           |
| PRNE 0x00000005       | Comparación no igual.                                                                                           |
| PRRE 0x00000006       | Comparación de expresiones regulares.                                                                                  |
| PRAllBits 0x00000007  | AND bit a bit que devuelve el operando derecho.                                                                     |
| PRSomeBits 0x00000008 | AND bit a bit que devuelve un valor distinto de cero.                                                                       |
| PRAll 0x00000100      | La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas. |
| PRAny 0x00000200      | La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.       |



 

**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.2, que indica la propiedad en la que se va a realizar una operación de coincidencia.

**\_ prval:** una estructura CBaseStorageVariant, como se especifica en la sección 2.2.1.1, que contiene el valor que se debe relacionar con la propiedad.

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

La estructura CRangeRestriction contiene una restricción en un intervalo de valores.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keyStart (variable)

\_keyEnd (variable)



 

**\_ keyStart:** estructura CKey, como se especifica en la sección 2.2.1.4, que contiene el principio del intervalo.

**\_ keyEnd:** estructura CKey que contiene el final del intervalo.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

La estructura CScopeRestriction contiene una restricción en los archivos que se buscarán.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (variable)

...

\_padding (variable)

\_length

\_fRecursive

\_fVirtual



 

**CcLowerPath:** entero de 32 bits sin signo que contiene el número de caracteres Unicode en el \_ campo lowerPath.

**\_ lowerPath:** cadena Unicode no terminada en NULL que representa la **ruta** de acceso a la que se debe restringir la consulta. El campo CcLowerPath contiene la longitud de la cadena.

**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**\_ length:** entero de 32 bits sin signo que contiene la longitud \_ de lowerPath, en caracteres Unicode. Debe ser el mismo valor que CcLowerPath.

**\_ fRecursive:** entero de 32 bits sin signo. DEBE establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, el servidor examinará de forma recursiva todos los subdirectorios de la ruta de acceso. Si se establece en 0x00000000, el servidor no examinará ningún subdirectorio.

**\_ fVirtual:** entero de 32 bits sin signo. DEBE establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, lowerPath es una ruta de acceso virtual (el localizador uniforme de recursos (URL) asociado a un directorio físico en el sistema de \_ archivos) para un sitio web. Si se establece en 0x00000000, \_ lowerPath es una ruta de acceso del sistema de archivos.

### <a name="22112-csort"></a>2.2.1.12 CSort

La estructura CSort identifica una columna que se debe ordenar.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

dwOrder

locale



 

**pidColumn:** entero de 32 bits sin signo. Número de la columna por la que se ordenará.

**dwOrder:** entero de 32 bits sin signo. DEBE ser uno de los siguientes valores, especificando cómo ordenar en función de la columna.



| Valor                        | Significado                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| QUERY \_ SORTASCEND 0x00000000 | Las filas se ordenarán en orden ascendente en función de los valores de la columna especificada.  |
| Query \_ DESCEND 0x00000001    | Las filas se ordenan en orden descendente en función de los valores de la columna especificada. |



 

**configuración regional:** entero de 32 bits sin signo que indica la configuración regional, como se especifica en el Apéndice A de \[ MS-GPSI, \] de la columna.

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

La estructura CSynRestriction contiene una palabra o sus sinónimos para una frase de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Restricción

...

...

cKey

\_keyArray (variable)

\_isRange



 

**Restricción:** estructura COccRestriction que especifica la ubicación de la palabra.

**cKey:** entero de 32 bits sin signo que especifica el número de elementos de la \_ matriz keyArray.

**\_ keyArray:** matriz de estructuras CKey que especifican una palabra y sus sinónimos.

**\_ isRange:** si se establece en 0x01, las claves son prefijos para coincidir. Si se establece en 0x00, las claves son valores exactos que se van a coincidir. \_isRange NO DEBE establecerse en ningún otro valor.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

La estructura CVectorRestriction contiene una operación OR ponderada en un nodo de árbol de comandos.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_pres (variable)

...

\_padding (variable)

\_ulRankMethod



 

**\_ pres:** árbol de comandos CNodeRestriction en el que se va a realizar una operación OR clasificada.

**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**\_ ulRankMethod:** entero de 32 bits sin signo que especifica un algoritmo de clasificación. DEBE establecerse en uno de los valores siguientes.



| Valor                            | Significado                                       |
|----------------------------------|-----------------------------------------------|
| VECTOR \_ RANK \_ MIN 0x00000000     | Use el algoritmo \[ mínimo SALTON \] .             |
| VECTOR \_ RANK \_ MAX 0x00000001     | Use el algoritmo \[ máximo SALTON \] .             |
| VECTOR \_ RANK \_ INNER 0x00000002   | Use el algoritmo de producto \[ interno SALTON \] .       |
| Vector \_ RANK \_ DICE 0x00000003    | Use el algoritmo de coeficiente de \[ dados SALTON \] .    |
| Vector \_ RANK \_ 0X00000004 | Use el algoritmo de coeficiente de Card \[ salton \] . |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

La estructura CWordRestriction contiene una palabra para una frase de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

restricción

...

...

\_key (variable)

\_isRange



 

**restriction:** estructura COccRestriction que especifica la ubicación de la palabra.

**\_ key:** estructura CKey que especifica una palabra.

**\_ isRange:** si se establece en 0x01, la clave es un prefijo para coincidir. Si se establece en 0x00, la clave es un valor exacto que debe coincidir. \_isRange NO DEBE establecerse en ningún otro valor.

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

La estructura CRestriction contiene un nodo de un árbol de comandos de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Peso

Restricción



 

**\_ ulType:** entero de 32 bits sin signo que indica el tipo de restricción utilizado para el nodo de árbol de comandos. DEBE establecerse en uno de los valores siguientes.



| Valor                    | Significado                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | El nodo representa una palabra ruidosa en una consulta vectorial.                                         |
| RTAnd 0x00000001         | El nodo contiene una CNodeRestriction en la que se va a realizar una operación AND lógica. |
| RTOr 0x00000002          | El nodo contiene una CNodeRestriction en la que se va a realizar una operación OR lógica.  |
| RTNot 0x00000003         | El nodo contiene una CRestriction en la que se va a realizar una operación NOT.             |
| RTContent 0x00000004     | El nodo contiene un CContentRestriction.                                                    |
| RtProperty 0x00000005    | El nodo contiene una CPropertyRestriction.                                                   |
| RtProximity 0x00000006   | El nodo contiene una CNodeRestriction en la que se va a realizar una clasificación de proximidad.     |
| RTVector 0x00000007      | El nodo contiene un CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | El nodo contiene una CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | El nodo contiene una CScopeRestriction.                                                      |
| PRAny 0xFFFFFFFA         | El nodo contiene una CInternalPropertyRestriction.                                           |
| RtRange 0xFFFFFFFC       | El nodo contiene una CRangeRestriction.                                                      |
| RTPhrase 0xFFFFFFFD      | El nodo contiene una CNodeRestriction en la que se va a realizar una coincidencia de frases.          |
| RTSynonym 0xFFFFFFFE     | El nodo contiene una CSynRestriction.                                                        |
| RtWord 0xFFFFFFFF        | El nodo contiene una CWordRestriction.                                                       |



 

**Peso:** entero de 32 bits sin signo que representa el peso del nodo. Peso indica la importancia del nodo con respecto a otros nodos del árbol de comandos de consulta. Los valores de peso más altos son más importantes.

**Restricción:** tipo de restricción para el nodo de árbol de comandos. La sintaxis DEBE ser tal como se indica en el \_ campo ulType.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

La estructura CColumnSet especifica los números de columna que se devolverán. Esta estructura siempre se usa en referencia a una estructura CPidMapper específica (sección 2.2.1.23).



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

recuento

índices (variable)



 

**count:** entero de 32 bits sin signo que especifica el número de elementos de la matriz de índices.

**indexes:** matriz de enteros sin signo de 4 bytes que representan índices de base cero en la matriz aPropSpec de la estructura CPidMapper correspondiente.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

La estructura CCategorizationSet contiene información sobre la agrupación de un conjunto de resultados de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

recuento

categories (variable)



 

**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz categories.

**categories**: matriz de estructuras CCategorizationSpec que especifican la agrupación de la consulta.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

La estructura CCategorizationSpec contiene una agrupación para un conjunto de resultados de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (variable)

\_ulCategType



 

**\_ csColumns:** estructura CColumnSet que indica las columnas por las que se va a agrupar la consulta.

**\_ ulCategType:** entero de 32 bits sin signo. DEBE establecerse en 0x00000000.

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

La estructura CDbColId contiene una columna.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (variable)



 

**eKind:** DEBE establecerse en uno de los valores siguientes que indica el contenido de GUID y vValue.



| Valor                            | Significado                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Nombre del GUID de DBKIND \_ \_ 0x00000000    | vString contiene un nombre de propiedad.                                                                               |
| DBKIND \_ GUID \_ PROPID 0x00000001  | ulId contiene un entero de 4 bytes que indica el identificador de propiedad.                                                      |
| Nombre \_ de PGUID de DBKIND \_ 0x00000003   | vString contiene un nombre de propiedad. Este valor DEBE tratarse igual que DBKIND \_ GUID \_ NAME.                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId contiene un entero de 4 bytes que indica el identificador de propiedad. Este valor DEBE ser el mismo que DBKIND \_ GUID \_ PROPID. |



 

**GUID:** GUID de propiedad.

**ulId:** si eKind es DBKIND GUID PROPID o \_ \_ DBKIND \_ PGUID PROPID, este campo contiene un entero sin signo y especifica el identificador \_ de propiedad. Si eKind es DBKIND GUID NAME o \_ \_ DBKIND PGUID NAME, este campo contiene un entero sin signo que especifica el número de caracteres Unicode contenidos en el \_ \_ campo vString.

**vString:** cadena Unicode no terminada en NULL que representa el nombre de propiedad. Debe omitirse a menos que el campo eKind esté establecido en DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

La estructura CDbProp contiene una propiedad .



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

yd (variable)

vValue (variable)



 

**DBPROPID:** entero de 32 bits sin signo que indica el identificador de propiedad.

**DBPROPOPTIONS:** DEBE establecerse en 0x00000000.

**DBPROPSTATUS:** DEBE establecerse en 0x00000000.

**: estructura** CDbColId, como se especifica en la sección 2.2.1.20, que indica la columna a la que se aplica la propiedad.

**vValue:** CBaseStorageVariant que contiene el valor de propiedad.

### <a name="221211-properties"></a>2.2.1.21.1 Propiedades

En esta sección se detallan las propiedades que usa CISP. Estas propiedades se agrupan en tres conjuntos de propiedades, ident2.2.1.21.1, en el campo guidPropertySet de la estructura CDbPropSet (sección 2.2.1.22).

En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ FSCIFRMWRK \_ EXT.



| Valor                                  | Significado                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| NOMBRE DEL CATÁLOGO DE CI de DBPROP \_ \_ \_ 0x00000002   | Especifica el nombre del catálogo o catálogos que se consultan. El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.                                   |
| ÁMBITOS \_ DE INCLUIR DE DBPROP CI \_ \_ 0x00000003 | Especifica una o varias rutas de acceso que se incluirán en la consulta. El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.                                 |
| MARCAS DE ÁMBITO DE CI DE DBPROP \_ \_ \_ 0x00000004    | Especifica cómo se tratarán las rutas de acceso especificadas por la propiedad \_ DBPROP CI \_ INCLUDE \_ SCOPES. El valor DEBE ser VT \_ I4 o VT \_ VECTOR VT \| \_ I4. |
| TIPO DE \_ CONSULTA CI \_ DBPROP \_ 0x00000007     | Especifica el tipo de consulta. CDbColId DEBE establecerse en NULLID de base \_ de datos.                                                                               |



 

En la tabla siguiente se enumeran las marcas de la propiedad DBPROP \_ CI \_ SCOPE \_ FLAGS:



| Valor                     | Significado                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consulta \_ en profundidad 0x01          | Si se establece, indica que los archivos del directorio de ámbito y todos los subdirectorios se incluyen en los resultados. Si está claro, solo los archivos del directorio de ámbito se incluyen en los resultados. NO DEBE combinarse con QUERY \_ DEEP. |
| CONSULTA \_ DE RUTA DE ACCESO VIRTUAL \_ 0x02 | Si se establece, indica que el ámbito es una ruta de acceso virtual. Si está claro, indica que el ámbito es un directorio físico.                                                                                                         |



 

En la tabla siguiente se enumeran los tipos de consulta para la propiedad DBPROP \_ CI \_ QUERY \_ TYPE:



| Valor                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Una consulta normal.                                                                                                   |
| CiVirtualRoots 0x00000001 | La consulta solicita una lista de las raíces virtuales del catálogo. Este valor requiere privilegios administrativos. |
| CiProperties 0x00000003   | La consulta solicita una lista de todas las propiedades admitidas por el servicio de indexación.                            |
| CiAdminOp 0x00000004      | La consulta es una operación administrativa. Este valor requiere privilegios administrativos.                           |



 

En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ QUERYEXT.



| Valor                                      | Significado                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Especifica cómo el servicio de indexación debe controlar consultas lentas. El valor DEBE ser un \_ VT BOOL. Si es TRUE, el servidor puede producir un error en estas consultas.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indica si el servicio de indexación va a realizar el recorte de resultados. Si es TRUE, el servidor debe considerar la posibilidad de realizar el recorte de resultados de una manera que optimice el tiempo de respuesta al cliente. El valor DEBE ser un \_ VT BOOL.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indica si el cliente admite tipos de datos VT \_ VECTOR. Si es TRUE, el cliente admite VT VECTOR; si es FALSE, el servidor va a convertir tipos de datos VT VECTOR en tipos de datos \_ \_ VT \_ ARRAY.  El valor DEBE ser VT \_ BOOL. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indica las coincidencias de fila que se devolverán. Si es TRUE, el servidor devolverá el primer conjunto de filas coincidentes. Si es FALSE, se deben devolver las mejores filas coincidentes. El valor DEBE ser un \_ VT BOOL.                                             |



 

En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ CIFRMWRKCORE \_ EXT.



| Valor/DBPROPID                 | Significado                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DbPROP \_ MACHINE 0x00000002       | Especifica los nombres de los equipos en los que se va a procesar una consulta. El valor DEBE ser VT \_ BSTR o VT \_ ARRAY VT \| \_ BSTR. |
| DBPROP \_ CLIENT \_ CLSID 0x00000003 | Especifica una constante de conexión para el servicio de indexación. El valor DEBE ser un \_ CLSID VT que contenga 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

La estructura CDbPropSet contiene un conjunto de propiedades. Tenga en cuenta que el primer campo es de tamaño fijo, pero puede que no esté alineado en un desplazamiento que sea un múltiplo de 4 bytes desde el inicio del mensaje que contiene esta estructura. Sin embargo, el campo cProperties se alinea como tal y, por lo tanto, el formato se representa de la siguiente manera:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

guidPropertySet

...

...

...

...

\_padding (variable)

cProperties

aProps (variable)



 

**guidPropertySet:** GUID que identifica el conjunto de propiedades. DEBE establecerse en el formulario binario correspondiente a uno de los siguientes valores (mostrados en el formulario de representación de cadena), identificando el conjunto de propiedades de las propiedades contenidas en el campo aProps.



| Valor/GUID                                                                              | Nombre                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ EXT<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Conjunto de propiedades del marco de índice de contenido del sistema de archivos |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Conjunto de propiedades de extensión de consulta                     |
| DBPROPSET \_ CIFRMWRKCORE \_ EXT<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Conjunto de propiedades de Content Index Framework Core        |



 

**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes. La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario. El receptor DEBE omitir el contenido de este campo.

**cProperties:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aProps.

**aProps:** una matriz de estructuras CDbProp, como se especifica en la sección 0, que contiene propiedades. Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si hay bytes de relleno, el valor que contienen es arbitrario. El receptor DEBE omitir el contenido de los bytes de relleno.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

La estructura CPidMapper contiene una matriz de los IDs de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

recuento

aPropSpec

... (variable)



 

**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aPropSpec.

**aPropSpec:** matriz de estructuras CFullPropSpec que indican las propiedades que se devolverán. Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

La estructura CRowSeekAt contiene el desplazamiento en el que se van a recuperar las filas de un mensaje CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.

**\_ cskip:** entero de 32 bits sin signo que contiene el número de filas que se omitirán en el conjunto de filas.

**\_ bmkOffset:** valor de 32 bits que  representa el identificador del marcador que indica la posición inicial desde la que se omite el número de filas especificadas en cskip, antes de comenzar la \_ recuperación.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

La estructura CRowSeekAtRatio identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt:** entero de 32 bits sin signo que indica el capítulo del conjunto de filas del que se recuperan las filas.

**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.

**\_ ulNumerator:** entero de 32 bits sin signo que representa el numerador de la proporción de filas del capítulo en el que se va a iniciar la recuperación.

**\_ ulDenominator:** entero de 32 bits sin signo que representa el denominador de la proporción de filas del capítulo en el que se va a iniciar la recuperación. DEBE ser mayor que cero.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

La estructura CRowSeekByBookmark identifica los marcadores desde los que empezar a recuperar filas para un mensaje CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (variable)

\_ascRet (variable)



 

**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.

**\_ cBookmarks:** entero de 32 bits sin signo que representa el número de elementos de \_ una matriz aBookmarks.

**\_ maxRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet.

**\_ cValidRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet que son válidos. Se han definido elementos válidos en la matriz, mientras que los elementos no válidos no están definidos.

**\_ aBookmarks:** matriz de identificadores de marcador (cada uno representado por 4 bytes), como se obtiene de un mensaje CPMGetRowsOut.

**\_ ascRet:** matriz de valores HRESULT. Cuando se envía CRowSeekByBookMark como parte de la solicitud CPMGetRowsIn, el número de entradas de la matriz DEBE ser igual a \_ cBookMarks. Cuando el cliente los envía, los valores DEBEN establecerse en cero y el servidor DEBE omitir el contenido de la matriz. Cuando el servidor lo envía (como parte del mensaje CPMGetRowsOut), los valores de la matriz indican el estado del resultado de cada recuperación de fila.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

La estructura CRowSeekNext contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_cskip



 

**CiTblChapt:** entero de 32 bits sin signo que especifica el capítulo del conjunto de filas del que se recuperarán las filas.

**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.

**\_ cskip:** entero de 32 bits sin signo que representa el número de filas que se omitirán en el conjunto de filas.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

La estructura CRowsetProperties contiene información de configuración para una consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions:** los 3 bits menos significativos de este campo DEBEN contener uno de los tres valores siguientes:



| Valor                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | El cursor solo se puede mover hacia delante.                              |
| eLocatable 0x00000003  | El cursor se puede mover a cualquier posición.                            |
| eScrollable 0x00000007 | El cursor se puede mover a cualquier posición y capturar en cualquier dirección. |



 

Los bits restantes pueden ser claros o establecerse en cualquier combinación de los siguientes valores de forma lógica o conjunta:



| Valor                     | Significado                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | El cliente no esperará a que finalice la ejecución.                                                          |
| eFirstRows 0x00000080     | Devuelve las primeras filas encontradas, no las mejores coincidencias.                                                    |
| eHoldRows 0x00000200      | El servidor NO DEBE descartar filas hasta que el cliente se realiza con una consulta.                                     |
| eChaptered 0x00000800     | El conjunto de filas admite capítulos.                                                                               |
| eUseCI 0x00001000         | Responda solo a la consulta desde el índice, no desde el sistema de archivos.                                                  |
| eDeferTrimming 0x00002000 | El servicio de indexación debe considerar la posibilidad de optimizar el tiempo de respuesta al cliente al realizar la eliminación de resultados. |



 

**\_ ulMaxOpenRows:** entero de 32 bits sin signo. Debe establecerse en 0x00000000. No se usa y DEBE omitirse.

**\_ ulMemoryUsage:** entero de 32 bits sin signo. Debe establecerse en 0x00000000. No se usa y DEBE omitirse.

**\_ cMaxResults:** entero de 32 bits sin signo que especifica el número máximo de filas que se van a devolver para la consulta.

**\_ cCmdTimeout:** entero de 32 bits sin signo, que especifica el número de segundos en los que se va a finalizar automáticamente una consulta, contando desde el momento en que la consulta comienza a ejecutarse en el servidor. Un valor de 0x00000000 significa que la consulta no debe hacer tiempo de espera.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

La estructura CRowVariant contiene la parte de tamaño fijo de un tipo de datos de longitud variable almacenado en el mensaje CPMGetRowsOut.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

reserved1

reserved2

Desplazamiento (opcional)



 

**vType:** un indicador de tipo que indica el tipo de vValue. DEBE ser uno de los valores VARENUM especificados en la sección 2.2.1.1.

**reserved1:** no se usa. El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.

**reserved2:** no se usa. El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.

**Offset:** desplazamiento a datos de longitud variable (por ejemplo, una cadena).  DEBE ser un valor de 32 bits (4 bytes de longitud) si se usan desplazamientos de 32 bits (según las reglas de la sección 2.2.3.16) o un valor de 64 bytes (8 bytes de longitud) si se usan desplazamientos de 64 bits.

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

La estructura CSortSet contiene el criterio de ordenación de la consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Count

sortArray (variable)



 

**count:** entero de 32 bits sin signo que especifica el número de elementos de sortArray.

**sortArray:** matriz de estructuras de CSort que describen el orden en el que se ordenan los resultados de la consulta. Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

La estructura CTableColumn contiene una columna de un mensaje CPMSetBindingsIn



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... (variable)

vType

ValueUsed

\_padding1 (opcional)

ValueOffset (opcional)

ValueSize (opcional)

StatusUsed

\_padding2 (opcional)

StatusOffset (opcional)

LengthUsed

\_padding3 (opcional)

LengthOffset (opcional)



 

**PropSpec:** una estructura CFullPropSpec tal como se especifica en la sección 2.2.1.3.

**vType:** especifica el tipo de valor de datos contenido en la columna. Consulte el campo vType de la sección 2.2.1.1 para obtener la lista de valores de este campo.

**ValueUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00. Si se establece en 0x01, la columna se transfiere dentro de la fila de tamaño fijo. Si se establece en 0x00, el valor de la columna se transfiere en la sección de longitud variable al final del búfer.

**\_ padding1:** campo de un byte que SE DEBE insertar antes de ValueOffset si, sin él, ValueOffset no comenzaría con un desplazamiento par desde el principio del mensaje. El valor de este byte es arbitrario y DEBE omitirse. Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.

**ValueOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del valor de columna de la fila. Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.

**ValueSize:** entero de 2 bytes sin signo que especifica el tamaño del valor de columna en bytes. Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.

**StatusUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00. Si se establece en 0x01, el estado de la columna se transfiere dentro de la fila. Si 0x00, el estado de la columna no se transfiere dentro de la fila.

**\_ padding2:** campo de un byte que SE DEBE insertar antes de StatusOffset si, sin él, el campo StatusOffset no comenzaría con un desplazamiento par desde el principio del mensaje. El valor de este byte es arbitrario y DEBE omitirse. Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.

**StatusOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del estado de la columna en la fila. Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.

**LengthUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00. Si se establece en 0x01, la longitud de la columna se transfiere dentro de la fila. Si 0x00, la longitud de la columna NO SE DEBE transferir dentro de la fila.

**\_ padding3:** campo de un byte que SE DEBE insertar antes de LengthOffset si, sin él, LengthOffset no comenzaría con un desplazamiento par desde el principio de un mensaje. El valor de este byte es arbitrario y DEBE omitirse. Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.

**LengthOffset:** entero de 2 bytes sin signo que especifica el desplazamiento de la longitud de columna de la fila. Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

La estructura SERIALIZEDPROPERTYVALUE contiene un valor serializado.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

rgb (variable)



 

**dwType:** uno de los tipos de variante, definidos en la sección 2.2.1.1, que se puede combinar con modificadores de tipo variant. Para todos los tipos de variante, excepto los combinados con VT ARRAY, SERIALIZEDPROPERTYVALUE tiene el mismo diseño que CBaseStorageVariant, tal como se especifica en la sección \_ 2.2.1.1. Si el tipo de variante se combina con el modificador de tipo VT ARRAY, se usa SAFEARRAY2, especificado en la sección \_ 2.2.1.2.1.1, en lugar de SAFEARRAY en el campo vValue de CBaseStorageVariant.

**rgb:** valor serializado. Vea los detalles de serialización de vValue en 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 Encabezados de mensaje

Todos los mensajes de Content Indexing Service Protocol tienen un encabezado de 16 bytes.

A continuación se muestra un diagrama que muestra el formato de encabezado de mensaje del Protocolo de indexación de contenido.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Msg

\_Estado

\_ulChecksum

\_ulReserved2



 

\_**msg:** entero de 32 bits que identifica el tipo de mensaje que sigue al encabezado. En la tabla siguiente se enumeran los mensajes del Protocolo de servicio de indexación de contenido y los valores enteros especificados para cada mensaje. Como se muestra en la tabla, algunos valores identifican dos mensajes en la tabla. En esos casos, el mensaje que sigue al encabezado se puede identificar por la dirección del flujo de mensajes. Si la dirección es cliente a servidor, se indica el mensaje con "In" anexado al nombre del mensaje. Si la dirección es de servidor a cliente, se indica el mensaje con "Out" anexado al nombre del mensaje.



| Valor      | Significado                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn o CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn o CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn o CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn o CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn o CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn o CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn o CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| 0x000000D1 | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn o CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn o CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn o PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn o CPMSetCatStateOut                       |



 

\_**status:** HRESULT \[ MS-SYS \] , que indica el estado de la operación solicitada.

\* *

*Windows Comportamiento: el cliente siempre establece el \_ campo de estado en 0x00000000.*

**\_ ulChecksum:** ulChecksum DEBE calcularse según lo especificado en la sección \_ 3.2.4 para los mensajes siguientes:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Para todos los demás mensajes, \_ ulChecksum DEBE establecerse en 0x00000000. Un cliente DEBE omitir el \_ campo ulChecksum.

**\_ ulReserved2:** DEBE establecerse en 0 y el receptor debe omitirlo.

### <a name="223-messages"></a>2.2.3 Mensajes

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

El mensaje CPMCiStateInOut contiene información sobre el estado del servicio de indexación. El formato del mensaje CPMCiStateInOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

eState

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct:** entero de 32 bits sin signo. Tamaño en bytes de este mensaje (excepto el encabezado común). DEBE establecerse en 0x0000003C.

**cWordList:** entero de 32 bits sin signo que indica el recuento de índices iniciales creados para documentos indexados recientemente.

**cPersistentIndex:** entero de 32 bits sin signo que indica el recuento de índices persistentes.

**cQueries:** entero de 32 bits sin signo que indica un número de consultas que se ejecutan activamente.

**cDocuments:** entero de 32 bits sin signo que indica el número total de documentos en espera de indexación.

**cFreshTest:** entero de 32 bits sin signo que indica el número de documentos únicos con información en índices que no están totalmente optimizados para el rendimiento.

**dwMergeProgress:** entero de 32 bits sin signo que especifica el porcentaje de finalización de la optimización completa actual de los índices, si la optimización está actualmente en curso. DEBE ser menor o igual que 100.

**eState:** estado de indexación de contenido tal como lo indican una o varias de las constantes DE CI \_ \_ \* STATE, definidas en la tabla siguiente.



| Valor                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMBINACIÓN \_ DE \_ \_ SOMBRAS DE ESTADO DE CI 0x00000001           | El servicio de indexación está en proceso de optimizar algunos de los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.                                                                                                                                                                                                                                                                                                                                                                |
| Ci \_ STATE MASTER MERGE \_ \_ 0x00000002           | El servicio de indexación está en proceso de optimización completa para todos los índices.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SE \_ REQUIERE ANÁLISIS DE CONTENIDO DE ESTADO DE CI \_ \_ \_ 0x00000004 | Algunos documentos del índice han cambiado y el servicio de indexación debe determinar cuáles se han agregado, cambiado o eliminado.                                                                                                                                                                                                                                                                                                                                                              |
| Combinación \_ de \_ RECOCI STATE \_ RECOCIDO 0x00000008        | El servicio de indexación está en proceso de optimizar los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas. Este proceso es más completo que el identificado por el valor DE CI STATE SHADOW MERGE, pero no es tan completo como se especifica en el valor \_ DE CI STATE MASTER \_ \_ \_ \_ \_ MERGE. Estas optimizaciones son específicas de la implementación, ya que dependen de la forma en que los datos se almacenan internamente; las optimizaciones no afectan al protocolo de ninguna manera que no sea el tiempo de respuesta. |
| Análisis \_ de ESTADO DE CI \_ 0x00000010                | El servicio de indexación está examinando un directorio o un conjunto de directorios para ver si se ha agregado, eliminado o actualizado algún archivo desde la última vez que se indexó el directorio.                                                                                                                                                                                                                                                                                                                 |
| RECUPERACIÓN \_ DE ESTADO DE CI \_ 0x00000020              | El servicio se inicia desde el último estado guardado y está en proceso de recuperación.                                                                                                                                                                                                                                                                                                                                                                                                        |
| ESTADO \_ DE CI MEMORIA BAJA \_ \_ 0x00000080             | La mayor parte de la memoria virtual del servidor está en uso.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CI \_ STATE HIGH IO \_ \_ 0x00000100                | El nivel de actividad de entrada/salida (E/S) en el servidor es relativamente alto.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| COMBINACIÓN MAESTRA DE ESTADO DE CI \_ \_ EN PAUSA \_ \_ 0X00000200   | Se ha pausado el proceso de optimización completa para todos los índices que se encontraban en curso. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                                  |
| Ci \_ STATE READ ONLY \_ \_ 0x00000400              | Se ha pausado la parte del servicio de indexación que recoge nuevos documentos para indexar. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                               |
| Ci \_ STATE BATTERY POWER \_ \_ 0x00000800          | La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado para conservar la duración de la batería, pero sigue respondiendo a las consultas. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                 |
| USUARIO \_ DE ESTADO DE CI activo \_ \_ 0x00001000            | La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado debido a la alta actividad del usuario (teclado o mouse), pero sigue respondiendo a las consultas. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                         |
| CI \_ STATE \_ STARTING 0x00002000                | El servicio está iniciándose. Las consultas se pueden ejecutar, pero el examen y la notificación aún no se han habilitado. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                   |
| ESTADO \_ DE CI LEYENDO \_ \_ USNS 0x00004000           | El servicio no ha leído el registro que mantiene el sistema de archivos para realizar un seguimiento de los cambios en los archivos o directorios de un volumen, por lo que es posible que el índice no esté actualizado.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos indexados desde que se inició la indexación de contenido.

**cTotalDocuments:** entero de 32 bits sin signo que indica el número total de documentos del sistema.

**cPendingScans:** entero de 32 bits sin signo que indica el número de operaciones de indexación de alto nivel pendientes. El significado de este valor es específico del proveedor, pero se espera que los números más grandes indiquen que queda más indexación.

*Windows comportamiento:* este valor suele ser cero, excepto inmediatamente después de que se haya iniciado la indexación o después de que se desborde una cola de notificaciones.

**dwIndexSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, del índice (excepto la caché de propiedades).

**cUniqueKeys:** entero de 32 bits sin signo que indica el número aproximado de claves únicas del catálogo.

**cSecQDocuments:** entero de 32 bits sin signo que indica el número de documentos que el servicio de indexación volverá a intentar indexar debido a un error durante el intento de indexación inicial.

**dwPropCacheSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, de la caché de propiedades.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

El mensaje CPMSetCatStateIn establece el estado de un catálogo. El formato del mensaje CPMSetCatStateIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (variable, opcional)



 

**\_ partID:** DEBE establecerse en 0x00000001.

**\_ dwNewState:** debe establecerse en uno de los valores siguientes, lo que indica el nuevo estado del catálogo.



| Valor                         | Significado                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ STOPPED 0x00000001     | El catálogo se detiene. Este estado significa que no se van a indexar nuevos archivos y que no se procesarán consultas de búsqueda.                                                     |
| CICAT \_ READONLY 0x00000002    | El catálogo es de solo lectura. No se van a indexar nuevos archivos.                                                                                                               |
| CiCAT \_ WRITABLE 0x00000004    | El catálogo se puede escribir. Se pueden indexar nuevos archivos y se procesarán las consultas de búsqueda.                                                                              |
| CICAT \_ NO \_ QUERY 0x00000008   | El catálogo no está disponible para realizar consultas.                                                                                                                              |
| CICAT \_ GET \_ STATE 0x00000010  | El estado del catálogo no se va a cambiar, solo se recupera.                                                                                                          |
| CICAT \_ ALL \_ OPENED 0x00000020 | Una comprobación para ver si se han iniciado todos los catálogos. Si es así, el campo dwOldState enviado en la respuesta CPMSetCatStateOut a este mensaje se notifica \_ como distinto de cero. |



 

**\_ CatName:** el nombre del catálogo que va a modificar su estado. El nombre DEBE ser una cadena Unicode terminada en NULL. Este campo DEBE omitirse si \_ dwNewState está establecido en CICAT \_ ALL \_ OPENED.

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

El mensaje CPMSetCatStateOut es una respuesta a un mensaje CPMSetCatStateIn con el estado anterior del catálogo. El formato del mensaje CPMSetCatStateOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState:** uno de los valores siguientes, que indica el estado anterior del catálogo.



| Valor                       | Significado                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ STOPPED 0x00000001   | El catálogo se detiene.                    |
| CICAT \_ READONLY 0x00000002  | El catálogo es de solo lectura.                  |
| CICAT \_ WRITABLE 0x00000004  | El catálogo se puede escribir.                   |
| CICAT \_ NO \_ QUERY 0x00000008 | El catálogo no está disponible para realizar consultas. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

El mensaje CPMUpdateDocumentsIn indica al servidor que indexe la ruta de acceso especificada.

El servidor responderá con el encabezado de mensaje del mensaje CPMUpdateDocumentsOut, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado del mensaje.

El formato del mensaje CPMUpdateDocumentsIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_flag (opcional)

\_fRootPath (opcional)

RootPath (variable, opcional)



 

**\_ flag**: tipo de actualización que se va a realizar. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje. Este campo DEBE establecerse en uno de los siguientes valores:



| Valor                  | Significado                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | Se va a realizar una actualización incremental. |
| UPD \_ FULL 0x00000001   | Se va a realizar una actualización completa.         |
| Upd \_ INIT 0x00000002   | Se va a realizar una nueva inicialización.  |



 

**\_ fRootPath:** valor booleano que indica si el campo RootPath especifica una ruta de acceso en la que realizar la actualización. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje. Este campo DEBE establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, se incluye una ruta de acceso en la que realizar la actualización en RootPath. Si se establece en 0x00000000, la actualización se realizará en todas las rutas de acceso indexadas.

**RootPath:** nombre de la ruta de acceso que se va a actualizar. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje. El nombre DEBE ser una cadena Unicode terminada en NULL. Este campo DEBE omitirse si \_ fRootPath está establecido en 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

El mensaje CPMForceMergeIn solicita a un servidor que realice el mantenimiento necesario para mejorar el rendimiento de las consultas. El servidor responderá con el encabezado de mensaje del mensaje CPMForceMergeIn, con los resultados de la solicitud contenida en el \_ campo de estado.

El formato del mensaje CPMForceMergeIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID (opcional)



 

**\_ partID:** este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje. Cuando este campo está presente, debe establecerse en 0x00000001.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

El mensaje CPMConnectIn inicia una sesión entre el cliente y el servidor.

El formato del mensaje CPMConnectIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_Acolchado

...

...

MachineName

... (variable)

UserName

... (variable)

\_paddingcPropSets (opcional, variable)

cPropSets

PropertySet1 (variable)

PropertySet2 (variable)

\_paddingExtPropset (opcional, variable)

cExtPropSet

aPropertySets (variable)



 

**\_ iClientVersion:** entero de 32 bits que indica si el servidor va a validar el valor de suma de comprobación especificado en el campo ulChecksum de los encabezados de mensaje para los mensajes enviados por el \_ cliente. Si el campo iClientVersion está establecido en 0x00000008 o superior, el servidor DEBE validar el valor del campo \_ \_ ulChecksum para los mensajes siguientes:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Para obtener más información sobre cómo el servidor valida el valor especificado por el cliente en el campo ulChecksum para los mensajes enumerados anteriormente, consulte la sección 3.2.5.

Si el valor es mayor que 0x00000008, se supone que el cliente es capaz de controlar desplazamientos de 64 bits en mensajes CPMGetRowsOut. Consulte la sección 2.2.3.16 para obtener más información.

*Windows comportamiento: en Windows cliente, iClientVersion se establece de la siguiente manera:*



| Valor      | Significado                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | El sistema operativo cliente Windows 2000.                                           |
| 0x00000008 | El sistema operativo cliente es de 32 Windows XP o de 32 Windows Server 2003. |
| 0x00010008 | El sistema operativo cliente es de 64 Windows XP o de 64 bits Windows Server 2003. |



 

\_**fClientIsRemote:** valor booleano que indica si el cliente se ejecuta en un equipo diferente al servidor. DEBE establecerse en 0x00000001.

\_**cbBlob1:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cPropSet, PropertySet1 y PropertySet2 combinados.

\_**cbBlob2:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cExPropSet y aPropertySet combinados.

\_**padding:** 12 bytes de relleno que pueden contener valores arbitrarios y DEBEN omitirse.

**MachineName:** el nombre de la máquina del cliente. La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode, incluido el terminador NULL.

**UserName:** cadena que representa el nombre de usuario de la persona que ejecuta la aplicación que invocó este protocolo. La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode cuando se concatena con MachineName.

**\_ paddingcPropSets:** este campo DEBE tener entre 0 y 7 bytes de longitud. El número de bytes DEBE ser el número necesario para que el desplazamiento de bytes del campo cPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8. El valor de los bytes puede ser cualquier valor arbitrario y DEBE ser omitido por el receptor.

**cPropSets:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo. Este valor DEBE establecerse en 0x0000002.

**PropertySet1:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ FSCIFRMWRK EXT (consulte la \_ sección 2.2.1.22).

**PropertySet2:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ CIFRMWRKCORE EXT (consulte la \_ sección 2.2.1.22).

\_**PaddingExtPropset:** este campo DEBE tener entre 0 y 7 bytes de longitud. El número de bytes DEBE ser el número necesario para que el desplazamiento de bytes del campo cExtPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8. El valor de los bytes puede ser cualquier valor arbitrario y DEBE ser omitido por el receptor.

**cExtPropSet:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo.

**aPropertySets:** matriz de estructuras CDbPropSet que especifican otras propiedades. El número de elementos de esta matriz DEBE ser igual a cExtPropSet.

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

El mensaje CPMConnectOut contiene una respuesta a un mensaje CPMConnectIn.

El formato del mensaje CPMConnectOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_serverVersion

\_reserved (variable)



 

**\_ serverVersion**:

Entero de 32 bits que indica si el servidor puede admitir desplazamientos de 64 *bits.* Consulte la sección 2.2.3.16 para obtener más información.



| Valor      | Significado                                 |
|------------|-----------------------------------------|
| 0x00000007 | El servidor solo puede enviar desplazamientos de 32 bits. |
| 0x00010007 | El servidor puede enviar desplazamientos de 32 o 64 bits.   |



 

**\_ reserved:** reservado. El servidor PUEDE enviar un número arbitrario de valores arbitrarios y el cliente DEBE omitir estos valores si están presentes.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

El mensaje CPMCreateQueryIn crea una nueva consulta. El formato del mensaje CPMCreateQueryIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Size

CColumnSetPresent

ColumnSet (opcional)

... (variable)

CRestrictionPresent.

Restricción (opcional)

... (variable)

CSortSetPresent

SortSet (opcional)

... (variable)

CCategorizationSetPresent

CategorizationSet (opcional)

... (variable)

RowSetProperties

...

...

...

...

PidMapper (variable)



 

**Tamaño:** entero de 32 bits sin signo que indica el número de bytes desde el principio de este campo hasta el final del mensaje.

**CColumnSetPresent:** campo de bytes que indica si el campo ColumnSet está presente. Este campo DEBE establecerse en 0x01 o 0x00. Si se establece en 0x01 el campo CColumnSet DEBE estar presente. Si se establece en 0x00, DEBE estar ausente.

**ColumnSet:** estructura CColumnSet que contiene los números de columna en los que se devolverán las propiedades de CPidMapper.

**CRestrictionPresent:** campo de bytes que indica si el campo Restricción está presente. Si se establece en cualquier valor distinto de cero, el campo Restricción DEBE estar presente. Si se establece en 0x00, la restricción DEBE estar ausente.

**Restricción:** estructura CRestriction que contiene el árbol de comandos de la consulta.

**CSortSetPresent:** campo de bytes que indica si el campo SortSet está presente. Si se establece en cualquier valor distinto de cero, el campo SortSet DEBE estar presente. Si se establece en 0x00, SortSet DEBE estar ausente.

**SortSet:** una estructura CSortSet que indica el criterio de ordenación de la consulta.

**CCategorizationSetPresent:** campo de bytes que indica si el campo CCategorizationSet está presente. Si se establece en cualquier valor distinto de cero, el campo CCategorizationSet DEBE estar presente. Si se establece en 0x00, CCategorizationSet DEBE estar ausente.

**CCategorizationSet:** estructura CCategorizationSet que contiene los grupos de la consulta.

**RowSetProperties:** estructura CRowsetProperties que proporciona información de configuración para la consulta.

**PidMapper:** estructura CPidMapper que contiene las propiedades que se devuelven en un conjunto de filas.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

El mensaje CPMCreateQueryOut contiene una respuesta a un mensaje CPMCreateQueryIn.

El formato del mensaje CPMCreateQueryOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential:** un valor booleano informativo que indica si se puede esperar que la consulta proporcione resultados más rápido. Cuando se establece en 0x00000001 para la consulta proporcionada en CPMCreateQueryIn, el servidor puede usar el índice de forma que los resultados de la consulta probablemente se entreguen más rápido. Cuando se establece en 0x00000000, habría una latencia mayor en la entrega de los resultados de la consulta. NO DEBE establecerse en ningún otro valor.

**\_ fWorkIdUnique:** valor booleano que indica si los identificadores de documento a los que apuntan los cursores son únicos en los resultados de la consulta. Si se establece en 0x00000001, los identificadores son únicos. Si se establece en 0x00000000, son únicos solo en todo el conjunto de filas.

**aCursors:** matriz de enteros de 32 bits sin signo que representan los identificadores de los cursores, con el número de elementos igual al número de categorías del campo CategorizationSet del mensaje CPMCreateQueryIn.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

El mensaje CPMGetQueryStatusIn solicita el estado de una consulta. El formato del mensaje CPMGetQueryStatusIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** entero de 32 bits sin signo que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

El mensaje CPMGetQueryStatusOut responde a un mensaje CPMGetQueryStatusIn con el estado de la consulta. El formato del mensaje CPMGetQueryStatusOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Estado



 

**\_ Estado:** máscara de bits de valores definidos en las tablas siguientes, que describe la consulta.

En la tabla siguiente se enumeran los valores STAT obtenidos mediante la realización de una operación AND bit a bit \_ \* en Status con \_ 0x00000007. El resultado DEBE ser uno de los siguientes:



| Constante                 | Significado                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ BUSY 0x00000000    | La consulta asincrónica todavía se está ejecutando.                                          |
| Error \_ de stat 0x00000001   | La consulta está en un estado de error.                                                   |
| STAT \_ DONE 0x00000002    | La consulta se ha completado.                                                            |
| Actualización \_ de STAT 0x00000003 | La consulta está completa, pero las actualizaciones están dando lugar a cálculos de consulta adicionales. |



 

En la tabla siguiente se enumeran los bits stat \_ \* adicionales que se pueden establecer de forma independiente.



| Constante                                    | Significado                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| STAT \_ NOISE \_ WORDS 0x00000010               | Las palabras ruidosas se reemplazaron por caracteres comodín en la consulta de contenido.                                                              |
| CONTENIDO \_ DE STAT NO ACTUALIZADO \_ \_ \_ 0x00000020     | Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados, pero sin indexar.                             |
| ACTUALIZACIÓN \_ DE \_ ESTADÍSTICAS INCOMPLETA 0X00000040        | Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados y indexados cuyo contenido no se incluyó. |
| CONSULTA DE CONTENIDO DE STAT \_ \_ INCOMPLETA \_ 0x00000080 | La consulta de contenido era demasiado compleja para completar o enumeración necesaria en lugar de usar el índice de contenido.                          |
| SE \_ HA SUPERADO EL LÍMITE DE TIEMPO DE \_ \_ 0X00000100      | Los resultados de la consulta pueden ser incorrectos porque el tiempo de ejecución de la consulta alcanzó el tiempo máximo permitido.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

El mensaje CPMGetQueryStatusExIn solicita el estado de una consulta e información adicional, como el número de documentos que se han indexado, el número de documentos que quedan por indexar, y así sucesivamente. El formato del mensaje CPMGetQueryStatusExIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_Bmk



 

**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.

**\_ bmk:** valor de 32 bits que indica el identificador de un marcador cuya posición se debe recuperar.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

El mensaje CPMGetQueryStatusExOut responde a un mensaje CPMGetQueryStatusExIn con el estado de la consulta y otra información de estado, como se describe en el diagrama siguiente. El formato del mensaje CPMGetQueryStatusExOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Estado

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ Estado:** una de las estadísticas \_ \* valores especificados en la sección 2.2.3.11.

**\_ cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos que se han indexado

**\_ cDocumentsToFilter:** entero de 32 bits sin signo que indica el número de documentos que quedan por indexar.

**\_ dwRatioFinishedDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de documentos que la consulta ha terminado de procesar.

**\_ dwRatioFinishedNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de documentos que la consulta ha terminado de procesar.

**\_ iRowBmk:** entero de 32 bits sin signo que indica la posición aproximada del marcador en el conjunto de filas en términos de filas.

**\_ cRowsTotal:** entero de 32 bits sin signo que especifica el número total de filas del conjunto de filas.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

El mensaje CPMSetBindingsIn solicita el enlace de columnas a un conjunto de filas. El servidor responderá al mensaje de solicitud CPMSetBindingsIn mediante la sección de encabezado del mensaje CPMBindingsIn con los resultados de la solicitud contenida en el campo \_ de estado. El formato del mensaje CPMSetBindingsIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (opcional)

\_cbRow (opcional)

\_cbBindingDesc (opcional)

\_dummy (opcional)

cColumns (opcional)

aColumns (variable, opcional)



 

**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la fila para la que se establecen los enlaces. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**\_ cbRow:** entero de 32 bits sin signo que indica el tamaño, en bytes, de una fila. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**\_ cbBindingDesc:** entero de 32 bits sin signo que indica la longitud, en bytes, de los campos que sigue al \_ campo ficticio. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**\_ dummy:** este campo no se usa y DEBE omitirse. Se puede establecer en cualquier valor arbitrario. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**cColumns:** entero de 32 bits sin signo que indica el número de elementos de la matriz aColumns. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**aColumns:** matriz de las estructuras CTableColumn que describen las columnas de una fila del conjunto de filas. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje. Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

El mensaje CPMGetRowsIn solicita filas de una consulta. El formato del mensaje CPMGetRowsIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

eType

\_chapt

SeekDescription

...

... (variable)



 

**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se recuperan las filas.

**\_ cRowsToTransfer:** entero de 32 bits sin signo que indica el número máximo de filas que el cliente desea recibir en respuesta a este mensaje.

**\_ cbRowWidth:** entero de 32 bits sin signo que indica la longitud de una fila, en bytes.

**\_ cbSeek:** entero de 32 bits sin signo que indica el tamaño del mensaje que comienza por eType.

**\_ cbReserved:** entero de 32 bits sin signo que indica el tamaño, en bytes, de un mensaje CPMGetRowsOut (sin los campos Rows y SeekDescriptions). Este valor de este campo se agrega al valor del campo cbSeek y, a continuación, se va a usar para calcular el desplazamiento del campo Rows en el mensaje \_ CPMGetRowsOut.

**\_ cbReadBuffer:** entero de 32 bits sin signo que DEBE establecerse en el valor máximo de cbRowWidth o 1000 veces el valor de \_ cRowsToTransfer, redondeado al múltiplo de \_ 512 bytes más cercano. El valor NO DEBE superar 0x00004000.

**\_ ulClientBase:** entero de 32 bits sin signo que indica el valor base que se usará para los cálculos de puntero en el búfer de fila. Si se usan desplazamientos de 64 bits, el campo reserved2 del encabezado del mensaje se usa como los 32 bits superiores y ulClientBase como los 32 bits inferiores de un valor de \_ 64 bits. Consulte la sección 2.2.3.16 para obtener más información.

**\_ fBwdFetch:** entero de 32 bits sin signo que indica el orden en el que se capturan las filas. Si se establece en 0x00000001, las filas se capturarán en orden inverso. Si se establece en 0x00000000, las filas se capturarán en orden de reenvío. NO DEBE establecerse en ningún otro valor.

**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación que se debe realizar.



| Valor                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription contiene una estructura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una estructura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una estructura CRowSeekAtRatio.    |
| ERowSeekByBookmark 0x00000004 | SeekDescription contiene una estructura CRowSeekByBookmark. |



 

**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.

**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el valor eType.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

El mensaje CPMGetRowsOut responde a un mensaje CPMGetRowsIn con las filas de una consulta. Los servidores DEBEN dar formato a los desplazamientos a los tipos de datos de longitud variable en el campo Filas de la manera siguiente:

-   El cliente indicó que era un sistema de 32 bits (0x00000008 o menos en el campo iClientVersion de CPMConnectIn): los desplazamientos son enteros de 32 bits.
-   El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 32 bits (serverVersion establecido en \_ \_ 0x00000007 en CPMConnectOut): los desplazamientos son enteros de 32 bits.
-   El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 64 bits (serverVersion establecido en \_ \_ 0x00010007 en CPMConnectOut): los desplazamientos son enteros de 64 bits

El formato del mensaje CPMGetRowsOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chapt

SeekDescription (opcional, variable)

...

...

paddingRows (opcional, variable)

Filas



 

**\_ cRowsReturned:** entero de 32 bits sin signo que indica el número de filas devueltas en Filas.

**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación rowseek que se debe realizar.



| Valor                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | Sin SeekDescription, ignore el campo SeekDescription.        |
| eRowSeekNext 0x00000001       | SeekDescription contiene una estructura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una estructura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una estructura CRowSeekAtRatio.    |
| ERowSeekByBookmark 0x00000004 | SeekDescription contiene una estructura CRowSeekByBookmark. |



 

**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.

**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el campo eType.

**paddingRows:** este campo DEBE tener una longitud suficiente (de 0 a cbReserved-1 bytes) para rellenar el campo Rows hasta el desplazamiento cbReserved desde el principio de un mensaje, donde cbReserved es el valor del mensaje \_ \_ \_ CPMGetRowsIn. Los bytes de relleno utilizados en este campo pueden ser cualquier valor arbitrario. El receptor DEBE omitir este campo.

**Filas:** los datos de fila tienen el formato indicado por la información de columna en el mensaje CPMSetBindingsIn más reciente. Las filas DEBEN almacenarse en orden de reenvío (por ejemplo, la fila 1 antes de la fila 2).

Las columnas de tamaño fijo DEBEN almacenarse en los desplazamientos especificados por el mensaje CPMSetBindingsIn más reciente.

Las columnas de tamaño variable (por ejemplo, cadenas) DEBEN almacenarse de la siguiente manera:

-   Los propios datos de la variable (por ejemplo, la cadena) se almacenan cerca del final del búfer en orden descendente (por ejemplo, la colección de todos los datos de variables para la fila 1 está al final, la fila 2 siguiente más cercana, etc.).
-   El área de tamaño fijo (al principio del búfer de fila) DEBE contener un CRowVariant para cada columna, almacenado en el desplazamiento especificado en el mensaje CPMSetBindingsIn más reciente. vType DEBE contener el tipo de datos (por ejemplo, VT \_ LPWSTR). Si, según lo determinado por las reglas al principio de la sección de esta sección, se usan desplazamientos de 32 bits, el campo Offset de CRowVariant DEBE contener un valor de 32 bits que sea el desplazamiento de los datos de variable desde el principio del mensaje CPMGetRowsOut, más el valor de ulClientBase especificado en el mensaje \_ CPMGetRowsIn más reciente. Si se usan desplazamientos de 64 bits, el campo Offset de CRowVariant DEBE contener un valor de 64 bits que sea el desplazamiento desde el principio del mensaje CPMGetRowsOut, agregado a un valor de 64 bits compuesto por el uso de ulClientBase como los 32 bits inferiores y \_ \_ ulReserved2 como los 32 bits altos.

Por ejemplo, si el mensaje CPMSetBindingsIn especificaba dos columnas :Size (VT \_ I4) y Title \_ (VT LPWSTR)-, y ulClientBase de CPMGetRowsIn era 0x10000, dos filas aparecerán como se indica a \_ continuación. La sección marcada en gris es la parte de longitud fija del búfer.

![Ejemplo de mensaje cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

El mensaje CPMRatioFinishedIn solicita el porcentaje de finalización de una consulta. El formato del mensaje CPMRatioFinishedIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_fQuick



 

**\_ hCursor: identificador** del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a solicitar información de finalización.

**\_ fQuick:** DEBE establecerse en 0x00000001. Sin usar y DEBE omitirse por el servidor.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

El mensaje CPMRatioFinishedOut responde a un mensaje CPMRatioFinishedIn con la proporción de finalización de una consulta. El formato del mensaje CPMRatioFinishedOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_Cuervos

\_fNewRows



 

**\_ ulNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de finalización en términos de filas.

**\_ ulDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de finalización en términos de filas. DEBE ser mayor que cero.

**\_ cRows:** entero de 32 bits sin signo que indica el número total de filas de la consulta.

**\_ fNewRows:** valor booleano que indica si hay nuevas filas disponibles. Un valor de 0x00000001 indica que hay nuevas filas disponibles en el conjunto de filas. Un valor de 0x00000000 indica que el conjunto de filas no contiene ninguna fila nueva. Este campo NO DEBE establecerse en ningún otro valor.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

El mensaje CPMFetchValueIn solicita un valor de propiedad demasiado grande para devolverlo en un conjunto de filas. Como se especifica en la sección 3.2.4.2.5, este mensaje se envía repetidamente para recuperar todos los bytes de la propiedad, actualizando cbSoFar para cada uno, hasta que el campo fMoreExists del mensaje \_ \_ CPMFetchValueOut se establece en **FALSE.**

El formato del mensaje CPMFetchValueIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (variable)

...

\_padding (variable)



 

**\_ wid:** entero de 32 bits sin signo que contiene información sobre el identificador de documento que identifica el documento para el que se debe capturar una propiedad.

**\_ cbSoFar:** entero de 32 bits sin signo que contiene el número de bytes transferidos previamente para esta propiedad. DEBE establecerse en 0x00000000 en el primer mensaje.

**\_ cbPropSpec:** entero de 32 bits sin signo que contiene el tamaño del campo PropSpec, en bytes.

**\_ cbChunk:** entero de 32 bits sin signo que contiene el número máximo de bytes que el remitente puede aceptar en un mensaje CPMFetchValueOut.

*Windows Comportamiento: este campo se establece en 0x00004000 para todas las versiones de Windows.*

**PropSpec:** estructura CFullPropSpec que especifica la propiedad que se recuperará.

**\_ padding:** este campo DEBE tener la longitud necesaria (de 0 a 3 bytes) para rellenar el mensaje hasta un múltiplo de 4 bytes de longitud. El valor de los bytes de relleno puede ser cualquier valor arbitrario. El receptor DEBE omitir este campo.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

El mensaje CPMFetchValueOut responde a un mensaje CPMFetchValueIn con un valor de propiedad de una consulta anterior. Como se especifica en la sección 3.1.5.2.8, este mensaje se envía después de cada mensaje CPMFetchValueIn hasta que se transfieren todos los bytes de la propiedad.

El formato del mensaje CPMFetchValueOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cbValue

\_fMoreExists

\_fValueExists

vType

vValue (variable)



 

**\_ cbValue:** entero de 32 bits sin signo que contiene el tamaño total, en bytes en vValue.

**\_ fMoreExists:** valor booleano que indica si hay mensajes CPMFetchValueOut adicionales disponibles. Si se establece en 0x00000001, hay mensajes CPMFetchValueOut adicionales. Si se establece en 0x00000000, no hay mensajes CPMFetchValueOut adicionales disponibles.

**\_ fValueExists:** valor booleano que indica si hay un valor para la propiedad . Si se establece en 0x00000001, existe un valor para la propiedad . Si se establece 0x00000000, no existe ningún valor para la propiedad .

**vType:** un valor de la enumeración VARENUM, vea la sección 2.2.1.1 para obtener más información y describir el tipo de la propiedad.

**vValue:** parte de una matriz de bytes que contiene una estructura SERIALIZEDPROPERTYVALUE como se especifica en la sección 2.2.1.32, donde el desplazamiento del principio de la parte es el valor \_ de cbSoFar en CPMFetchValueIn. La longitud de la parte, indicada por el campo cbValue, DEBE ser igual al valor de \_ \_ cbChunk en CPMFetchValueIn si \_ fMoreExists está establecido en 0x00000001 y DEBE ser menor o igual que el valor de cbChunk en caso \_ contrario.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

El mensaje CPMGetNotify solicita que se notifique al cliente de los cambios del conjunto de filas.

El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

El mensaje CPMSendNotifyOut notifica al cliente un cambio en los resultados de una consulta.

Este mensaje solo se envía cuando se produce un cambio. El formato del mensaje CPMSendNotifyOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify:** el cambio en la consulta. DEBE ser uno de los siguientes valores:



| Valor                                     | Significado                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | El número de filas del conjunto de filas de consulta ha cambiado. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | La consulta se ha completado.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | Se ha reecutado la consulta.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

El mensaje CPMGetApproximatePositionIn solicita la posición aproximada de un marcador en un capítulo. El formato del mensaje CPMGetApproximatePositionIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_Bmk



 

**\_ hCursor:** valor de 32 bits que representa el cursor de consulta obtenido de CPMCreateQueryOut para el conjunto de filas que contiene el marcador.

**\_ chapt:** valor de 32 bits que representa el identificador del capítulo que contiene el marcador.

**\_ bmk:** valor de 32 bits que representa el identificador del marcador para el que se va a recuperar la posición aproximada.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

El mensaje CPMGetApproximatePositionOut responde a un mensaje CPMGetApproximatePositionIn que describe la posición aproximada del marcador en el capítulo. El formato del mensaje CPMGetApproximatePositionOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_numerator

\_denominator



 

**\_ numerador:** entero de 32 bits sin signo que contiene el número de fila del marcador en el conjunto de filas. Si no hay filas, este campo DEBE establecerse en 0x00000000.

**\_ denominador:** entero de 32 bits sin signo que contiene el número de filas del conjunto de filas.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

El mensaje CPMCompareBmkIn solicita una comparación de dos marcadores en un capítulo.

El formato del mensaje CPMCompareBmkIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmkFirst

\_bmkSecond



 

\_**hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut para el conjunto de filas que contiene los marcadores.

\_**chapt:** valor de 32 bits que representa el identificador del capítulo que contiene los marcadores que se compararán.

\_**bmkFirst:** valor de 32 bits que representa el identificador del primer marcador que se va a comparar.

\_**bmkSecond:** valor de 32 bits que representa el identificador del segundo marcador que se va a comparar.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

El mensaje CPMCompareBmkOut responde a un mensaje CPMCompareBmkIn con la comparación de los dos marcadores del capítulo. El formato del mensaje CPMCompareBmkOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison:** uno de los valores siguientes, que indica las posiciones relativas de los dos marcadores del capítulo.



| Valor                               | Significado                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DbCOMPARE \_ LT 0x00000000            | El primer marcador se coloca delante del segundo.               |
| DBCOMPARE \_ EQ 0x00000001            | El primer marcador tiene la misma posición que el segundo.           |
| DBCOMPARE \_ GT 0x00000002            | El primer marcador se coloca después del segundo.                |
| DBCOMPARE \_ NE 0x00000003            | El primer marcador no tiene la misma posición que el segundo. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | El primer marcador no es comparable al segundo.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

El mensaje CPMRestartPositionIn mueve la posición de captura de un cursor al principio del capítulo. Como se especifica en la sección 3.1.5.2.12, el servidor responderá con el mismo mensaje, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado CISP.

El formato del mensaje CPMRestartPositionIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (opcional)

\_chapt (opcional)



 

**\_ hCursor:** valor de 32 bits que representa el identificador, obtenido de un mensaje CPMCreateQueryOut, que identifica la consulta para la que se debe reiniciar la posición. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

**\_ chapt:** valor de 32 bits que representa el identificador de un capítulo del que se recuperan filas. Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

El mensaje CPMFreeCursorIn solicita la liberación de un cursor. El formato del mensaje CPMFreeCursorIn que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** valor de 32 bits que representa el identificador del cursor del mensaje CPMCreateQueryOut que se liberará.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

El mensaje CPMFreeCursorOut responde a un mensaje CPMFreeCursorIn con los resultados de liberar un cursor. El formato del mensaje CPMFreeCursorOut que sigue al encabezado es:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining:** entero de 32 bits sin signo que indica el número de cursores que siguen en uso para la consulta.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

El mensaje CPMDisconnect finaliza la conexión con el servidor

El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.

### <a name="224-errors"></a>2.2.4 Errores

Todos los mensajes de Content Indexing Service Protocol DEBEN devolver 0x00000000 correcto; De lo contrario, devuelven un código de error distinto de cero de 32 bits que puede ser un valor HRESULT o NTSTATUS (consulte la sección 1.8). Si un búfer es demasiado pequeño para ajustarse a un resultado, se debe devolver un código de estado de STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) y la operación con errores debe reinterse con un búfer \_ mayor.

Todos los demás valores de error DEBEN tratarse igual.

(Tenga en cuenta que actualmente los espacios de numeración HRESULT y NTSTATUS no se superponen excepto con valores de significado idéntico, pero incluso si estuvieran en conflicto en el futuro, no provocaría ningún problema de protocolo siempre que el valor de STATUS \_ INSUFFICIENT \_ RESOURCES sigue siendo único, ya que todos los demás valores de error se tratan igual).

## <a name="3-protocol-details"></a>3 Detalles del protocolo

-   [3.1 Detalles del servidor](#31-server-details)
-   [3.2 Detalles del cliente](#32-client-details)

Las solicitudes de mensajes CISP para consultar de forma remota los catálogos del servicio de indexación no requieren ninguna secuencia determinada. Sin embargo, se recomienda que la capa superior cumpla una secuencia de mensajes significativa, como en el caso de los mensajes que se reciben fuera de esta secuencia o con datos no válidos, el servidor responderá con un error. Algunos mensajes también dependen de la capa superior que proporciona datos válidos que se recibieron en los mensajes anteriores de la secuencia.

En el diagrama siguiente se muestra una secuencia de mensajes típica para una consulta simple desde un cliente a un equipo remoto.

![secuencia de mensajes para una consulta simple](images/protocoldetails.jpg)

Los mensajes representados en el diagrama anterior representan un subconjunto de todos los mensajes CISP usados para consultar un catálogo de servicios de indexación remota.

### <a name="31-server-details"></a>3.1 Detalles del servidor

### <a name="311-abstract-data-model"></a>3.1.1 Modelo de datos abstracto

En la sección siguiente se especifican los datos y el estado que mantiene el servidor CISP. Los datos que se proporcionan aquí son para facilitar la explicación de cómo se comporta el protocolo. Esta sección no exige que las implementaciones cumplan este modelo siempre que su comportamiento externo sea coherente con el descrito en este documento.

Un servicio de indexación que implementa CISP DEBE mantener los siguientes elementos de datos abstractos:

-   Lista de clientes conectados al servidor
-   Información sobre cada cliente, que incluye:
-   -   Versión del cliente (como se indica en el mensaje CPMConnectIn especificado en la sección 2.2.3.6)
    -   Catálogo asociado al cliente (por un mensaje CPMConnectIn)
    -   Propiedades de cliente adicionales como se especifica en la sección 2.2.1.21.1.
    -   Consulta de búsqueda del cliente
    -   Lista de identificadores de cursor para la consulta y la posición en el conjunto de resultados para cada identificador.
    -   Conjunto actual de enlaces
    -   Estado actual de la consulta que incluye (para cada cursor):
    -   -   Número de filas en el resultado de la consulta
        -   Numerador y denominador de la finalización de consultas
        -   Último número de filas, notificado por el mensaje CPMRatioFinishedOut más reciente para este cursor
        -   Si el servidor supervisa la consulta en busca de cambios en los resultados de la consulta y si se supervisa, qué ha cambiado en los resultados de la consulta desde la última vez que CPMSendNotifyOut la informó al cliente por última vez.
        -   Lista de identificadores de capítulos que sirve esta consulta a un cliente.
        -   Lista de identificadores de marcador para cada cursor, que sirve esta consulta a un cliente.

-   Estado actual del servicio de indexación, que puede ser "no inicializado", "en ejecución" o "apagado". Tenga en cuenta que la mayoría de las veces el servidor está en estado "en ejecución". A continuación se muestra el diagrama de la máquina de estado para el servidor:

    ![diagrama de máquina de estado del servidor de servicio de indexación](images/abstractdatamodel.jpg)

-   Información por catálogo: número de documentos indexados, tamaño del índice, número de claves únicas, etc. (consulte la sección 2.2.3.1 para obtener una lista completa), estado (que corresponde a los valores de dwNewState en la sección 2.2.3.2).
-   Para cada idioma admitido, una base de datos de variaciones de palabras como se describe en la sección 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Temporizadores

No se requiere ningún temporizador de protocolo.

### <a name="313-initialization"></a>3.1.3 Inicialización

Tras la inicialización, el servidor DEBE establecer su estado en "no inicializado" y empezar a escuchar mensajes en la canalización con nombre especificada en la sección 1.9. Después de realizar cualquier otra inicialización interna, DEBE pasar al estado "en ejecución".

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Eventos desencadenados al más alto nivel

Ninguno.

### <a name="315-message-processing-and-sequencing-rules"></a>3.1.5 Reglas de procesamiento y secuenciación de mensajes

Cada vez que se produce un error durante el procesamiento de un mensaje enviado por un cliente, el servidor DEBE notificar un error al cliente como se indica a continuación:

-   Detener el procesamiento del mensaje enviado por el cliente
-   Responda con el encabezado del mensaje (solo) del mensaje enviado por el cliente, manteniendo \_ intacto el campo msg.
-   Establezca el \_ campo de estado en el valor del código de error.

Cuando llega un mensaje, el servidor DEBE comprobar el valor del campo msg para ver si es un tipo conocido (consulte la \_ sección 2.2.2). Si no se conoce el tipo, DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).

A continuación, el servidor DEBE validar el valor del campo \_ ulChecksum si el tipo de mensaje es uno de los siguientes:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Para validar el valor del campo ulChecksum, el servidor DEBE comprobar el valor que el cliente especificó en el campo iClientVersion en el \_ \_ mensaje CPMConnectIn.

Si el campo iClientVersion no está establecido en 0x00000008 y el campo ulChecksum no está establecido en 0x00000000, el servidor DEBE notificar un \_ error STATUS INVALID PARAMETER \_ \_ \_ (0xC000000D). El servidor NO DEBE validar el campo ulChecksum para los clientes y establecer el campo iClientVersion en un \_ \_ valor menor que 0x00000008.

Si el valor del campo iClientVersionfield es 0x00000008 o superior, el servidor DEBE validar que el campo ulChecksum se calculó como se especifica en la sección \_ \_ 3.2.4. Si el \_ valor ulChecksum no es válido, el servidor DEBE notificar un error STATUS \_ INVALID PARAMETER \_ (0xC000000D).

A continuación, el servidor comprueba en qué estado se encuentra. Si su estado es "no inicializado", el servidor DEBE notificar un error CI \_ E \_ NOT \_ INITIALIZED (0x8004180B). Si el estado es "apagar", el servidor DEBE notificar un error CI \_ E \_ SHUTDOWN (0x80041812).

Una vez que se ha determinado que un encabezado es válido y que el servidor está en estado "en ejecución", se DEBE realizar un procesamiento específico del mensaje adicional, tal como se especifica en las subsecciones siguientes.

### <a name="3151-remote-indexing-service-catalog-management"></a>3.1.5.1 Remote Indexing Service Catalog Management

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 Recepción de una solicitud CPMCiStateInOut

Cuando el servidor recibe una solicitud de mensaje CPMCIStateInOut del cliente, el servidor debe comprobar primero si el cliente está en una lista de clientes conectados. Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D). De lo contrario, DEBE responder al cliente con un mensaje CPMCIStateInOut, rellenando con información sobre el catálogo asociado del cliente, tal como se especifica en la sección 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 Recepción de una solicitud CPMSetCatStateIn

Cuando el servidor recibe una solicitud de mensaje CPMSetCatStateIn del cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).
-   Si dwNewState no es igual a CICAT ALL OPENED, cambie el estado del catálogo especificado en el campo CatName según lo especificado por el \_ \_ campo \_ \_ dwNewState. Consulte la sección 2.2.3.2 para obtener más detalles. Si el servidor no encuentra un catálogo con el nombre especificado en el campo CatName, el servidor DEBE devolver un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Responda al cliente con un mensaje CPMSetCatStateOut, donde dwOldState DEBE establecerse en \_ el estado anterior del catálogo. Si dwNewState es igual a CICAT ALL OPENED, el servidor DEBE comprobar el estado de todos los catálogos y, si todos ellos se inician, debe establecer dwOldState en 0x00000001 y, de lo \_ \_ \_ \_ contrario, \_ establecer dwOldState en 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 Recepción de una solicitud CPMUpdateDocumentsIn

Cuando el servidor recibe una solicitud de mensaje CPMUpdateDocumentsIn, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado). Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo al servidor, el servidor DEBE notificar un error DE ACCESO DENEGADO DE ESTADO \_ \_ (0xC0000022).
-   Comience el proceso de indexación de la ruta de acceso especificada por el cliente, realizando un examen completo o incremental, en función del valor del campo de marca en el mensaje \_ CPMUpdateDocumentsIn. Si la ruta de acceso no se indexó previamente, DEBE agregarse a la colección de ubicaciones indizadas y realizar un examen completo. Si se especifica un valor no válido del campo de marca, el servidor DEBE actuar como si la marca se hubiera establecido en UPD INIT y realizar \_ \_ un examen \_ completo. Esta operación DEBE realizarse en el catálogo asociado al cliente.
-   Responda al cliente con el encabezado de mensaje para CPMUpdateDocumentsIn y establezca el campo de estado \_ en los resultados de la solicitud.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 Recepción de una solicitud CPMForceMergeIn

Cuando el servidor recibe una solicitud de mensaje CPMForceMergeIn, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado). Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).
-   Inicie cualquier proceso de mantenimiento necesario para mejorar el rendimiento de las consultas en un catálogo, asociado al cliente.
-   Responda al cliente con un encabezado de mensaje para CPMForceMergeIn y establezca el campo de estado en los \_ resultados de la solicitud.

Tenga en cuenta que el proceso de mantenimiento es asincrónico y puede continuar después de que el cliente reciba el mensaje de respuesta. Este proceso no afecta directamente al protocolo de ninguna manera (aparte del tiempo de respuesta).

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 Consultas de Remote Indexing Service

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 Recepción de una solicitud CPMConnectIn

Cuando el servidor recibe una solicitud CPMConnectIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente está en la lista de clientes conectados. Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Comprueba si el catálogo especificado existe y no está en estado detenido. Si este no es el caso, el servidor DEBE notificar un error CI \_ E \_ NO CATALOG \_ (0x8004181D).
-   Agregue el cliente a la lista de clientes conectados.
-   Asocie el catálogo al cliente.
-   Almacene la información pasada en el mensaje CPMConnectIn (como el nombre del catálogo, la versión del cliente, etc.) en el estado de cliente.
-   Responda al cliente con un mensaje CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 Recepción de una solicitud CPMCreateQueryIn

Cuando el servidor recibe una solicitud de mensaje CPMCreateQueryIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente está en la lista de clientes conectados. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el cliente ya tiene una consulta asociada. Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el catálogo asociado al cliente está en estado que permite procesar la consulta (CICAT \_ READONLY o CICAT \_ WRITABLE). Si este no es el caso, el servidor DEBE notificar un error QUERY \_ S \_ NO QUERY \_ (0x8004160C).
-   Analice el conjunto de restricciones, los criterios de ordenación y las agrupaciones especificados en la consulta. Si el servidor encuentra un error, DEBE notificar un error adecuado. Si se produce un error en este paso por cualquier otro motivo, el servidor DEBE notificar el error encontrado. Para obtener información sobre los errores de consulta del servicio de indexación, \[ vea MSDN-QUERYERR \] .
-   Guarde la consulta de búsqueda en el estado del cliente.
-   Realice los preparativos necesarios para atender filas a un cliente y asocie la consulta con los identificadores de cursor adecuados (en función de la información que se pase en el mensaje CPMCreateQueryIn).
-   Agregue esos identificadores a la lista de identificadores de cursor del cliente e inicialice listas de identificadores de capítulos y marcadores.
-   Inicializar una lista de identificadores de capítulo para cada cursor de esta consulta en DB \_ NULL \_ HCHAPTER
-   Inicialice la lista de identificadores de marcador para cada cursor de esta consulta en un conjunto de DBBMK \_ FIRST y DBBMK \_ LAST.
-   Marque la consulta como no supervisada para los cambios.
-   Inicialice el número de filas en el número calculado actualmente de filas (que puede ser 0 si la consulta no comenzó a ejecutarse o algún número si la consulta está en un proceso de ejecución) e inicialice el numerador y el denominador de finalización de la consulta.
-   Responda al cliente con un mensaje CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 Recepción de una solicitud CPMGetQueryStatusIn

Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador del cursor está en una lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Prepare un mensaje CPMGetQueryStatusOut. El servidor DEBE recuperar el estado de consulta actual y establecerlo en el \_ campo QStatus (vea 2.2.3.11 para ver los valores posibles). Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
-   Responda al cliente con el mensaje CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 Recepción de una solicitud CPMGetQueryStatusExIn

Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusExIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador de cursor pasado está en una lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Prepare un mensaje CPMGetQueryStatusExOut. El servidor DEBE recuperar el estado de consulta actual y el progreso de la consulta y establecer QStatus (vea 2.2.3.11 para ver los valores posibles), \_ dwRatioFinishedDenominator y \_ dwRatioFinishedNumerator, respectivamente. A continuación, DEBE establecer el número de filas de los resultados de la consulta \_ en cRowsTotal. Si se produce un error en este paso por cualquier motivo, el servidor DEBE informar de que se ha encontrado un error.
-   Recupere información sobre el catálogo del cliente y rellene \_ cFilteredDocuments y \_ cDocumentsToFilter. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.
-   Recupere la posición del marcador indicado por el identificador en el campo bmk y rellene el campo iRowBmk restante en el \_ \_ mensaje CPMGetQueryStatusExOut. Si se produce un error en este paso por cualquier motivo, el servidor DEBE informar de que se ha encontrado un error.
-   Responda al cliente con el mensaje CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 Recepción de una solicitud CPMRatioFinishedIn

Cuando el servidor recibe una solicitud de mensaje CPMRatioFinishedIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Prepare un mensaje CPMRatioFinishedOut. El servidor DEBE recuperar el estado de consulta del cliente y rellenar los campos \_ ulNumerator, \_ ulDenominator \_ y cRows. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.
-   Si cRows es igual al último número notificado de filas para esta consulta, establezca \_ \_ fNewRows en 0x00000000; de lo contrario, estafórelo en 0x00000001.
-   Actualice el último número notificado de filas de esta consulta al valor \_ de cRows.
-   Responda al cliente con el mensaje CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 Recepción de una solicitud CPMSetBindingsIn

Cuando el servidor recibe una solicitud de mensaje CPMSetBindingsIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Compruebe que la información de enlaces es válida (es decir, la columna especifica al menos el valor, la longitud o el estado que se va a devolver; no se superpone en los enlaces para el valor, la longitud o el estado; y el valor, la longitud y el estado caben en el tamaño de fila especificado) y, si no se informa de un \_ error BADBINDINFO (0x80040E08) de base de \_ datos.
-   Guarde la información de enlace asociada a las columnas especificadas en el campo aColumns. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.
-   Responda al cliente con un encabezado de mensaje (solo) con msg establecido en CPMSetBindingsIn y el estado establecido en los resultados \_ \_ del enlace especificado.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 Recepción de una solicitud CPMGetRowsIn

Cuando el servidor recibe una solicitud de mensaje CPMGetRowsIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Compruebe si el cliente tiene un conjunto actual de enlaces. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Prepare un mensaje CPMGetRowsOut. El servidor DEBE colocar el cursor en los resultados de la consulta como se indica en la descripción de la búsqueda. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.
-   Capture tantas filas como quepa en un búfer, cuyo tamaño se indica mediante cbReadBuffer, pero no más de lo indicado por \_ \_ cRowsToTransfer. Al capturar filas, el servidor DEBE comparar el tipo de valor de propiedad de cada columna seleccionada con el tipo especificado en el conjunto actual de enlaces del cliente (sección 3.1.1). Si el tipo del enlace no es VT VARIANT, el servidor DEBE intentar convertir el valor de propiedad de la columna \_ en ese tipo. De lo contrario, si la marca DBPROP USEEXTENDEDDBTYPES está establecida en el conjunto de propiedades \_ DBPROPSET QUERYEXT del cliente, o si el valor de propiedad de la columna no es un tipo VT VECTOR, el valor de propiedad DEBE devolverse en su \_ \_ tipo normal. Si ninguno de estos casos es el caso (es decir, el servidor tiene un tipo VT VECTOR y el cliente no admite VT VECTOR), el servidor DEBE intentar convertirlo a un tipo VT ARRAY como se muestra a continuación: los elementos de la matriz VT \_ \_ \_ \_ I8, VT \_ UI8, VT FILETIME y \_ VT \_ CLSID no se pueden convertir y, en su lugar, producir un error. Los elementos de la matriz VT LPSTR y VT LPWSTR DEBEN convertirse en \_ VT BSTR; los elementos de matriz de todos los demás tipos \_ DEBEN permanecer sin \_ cambios. Por último, si las columnas de fila contienen identificadores de capítulo o identificadores de marcador, el servidor DEBE actualizar las listas correspondientes. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.
-   Almacene el número real de filas capturadas en \_ cRowsReturned.
-   Copie la descripción de la búsqueda y el campo de capítulo de CPMGetRowsIn en un mensaje CPMGetRowsOut que se va a enviar.
-   Almacene las filas capturadas en el campo Filas (vea la nota sobre el byte de estado siguiente y la sección 2.2.3.16 en la estructura del campo Filas).
-   Responda al cliente con el mensaje CPMGetRowsOut.

Nota sobre el campo de bytes de estado:

Si StatusUsed está establecido en 0x01 en la CTableColumn del mensaje CPMSetBindingIn de la columna, el servidor DEBE establecer el byte de estado (que se encuentra en StatusOffset desde el principio de la fila) para esta columna en uno de los valores siguientes:



| Valor | Significado        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Si el valor de propiedad no está presente para esta fila, el servidor DEBE establecer el byte de estado en StatusNull. Si el valor es demasiado grande para transferirse en el mensaje CPMGetRowsOut, el servidor DEBE establecer el byte de estado en StatusDeferred. De lo contrario, el servidor DEBE establecer el byte de estado en StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 Recepción de una solicitud CPMFetchValueIn

Cuando el servidor recibe una solicitud de mensaje CPMFetchValueIn de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Prepare un mensaje CPMFetchValueOut. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
-   Busque el documento indicado por el campo wid y compruebe si el identificador de propiedad de este documento (más adelante denominado "valor de propiedad") indicado por la estructura PropSpec está disponible para este \_ cliente. Si este valor no está disponible, el servidor DEBE establecer fValueExists en 0x00000000 y, de lo \_ contrario, \_ establecer fValueExists en 0x00000001. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
-   Si \_ fValueExists es igual a 0x00000001 el servidor DEBE hacer lo siguiente:
-   -   Serialice el valor de propiedad en una estructura SERIALIZEDPROPERTYVALUE y copie, a partir del desplazamiento cbSoFar, como máximo cbChunk bytes (pero no más allá del final de la propiedad serializada) en el \_ \_ campo vValue. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
    -   Establezca \_ cbValue en el número de bytes copiados en el paso anterior.
    -   Establezca vType en el tipo de propiedad del valor de propiedad.
    -   Si la longitud de la propiedad serializada es mayor que cbSoFar agregada a \_ \_ cbValue, establezca \_ fMoreExists en 0x00000001; de lo contrario, estafrála en 0x00000000.

-   Respuesta al cliente con el mensaje CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 Recibir una solicitud CPMGetNotify

Cuando el servidor recibe un mensaje CPMGetNotify de un cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Si no se ha realizado ningún cambio en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut para este cliente, o si la consulta no está supervisada actualmente para los cambios en el conjunto de resultados, el servidor DEBE responder con el mensaje CPMGetNotify y empezar a supervisar la consulta en busca de cambios en el conjunto de resultados. Si más adelante se produce un cambio en el conjunto de resultados de la consulta, el servidor DEBE enviar exactamente un mensaje CPMSendNotifyOut al cliente y DEBE especificar el cambio en el \_ campo watchNotify.
-   Si hubo cambios en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut, el servidor DEBE responder con CPMSendNotifyOut y DEBE especificar el cambio en el \_ campo watchNotify. Tenga en cuenta que, en el caso de muchos cambios en los resultados de la consulta, DBWATCHNOTIFY ROWSCHANGED tiene prioridad (es decir, si la consulta se ha realizado, se vuelve a ejecutar y, a continuación, el número de filas ha cambiado y la consulta se ha realizado de nuevo, el evento notificado sería \_ DBWATCHNOTIFY \_ ROWSCHANGED).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 Recepción de una solicitud CPMGetApproximatePositionIn

Cuando el servidor recibe una solicitud de mensaje CPMGetApproximatePositionIn del cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador del cursor, el identificador de capítulo y el identificador de marcador pasados están en las listas correspondientes. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Busque una fila asociada al identificador de marcador en los resultados de la consulta y aproximado de la posición de la fila en el conjunto de filas, a la que hace referencia el identificador de capítulo, y determine el numerador y el denominador de la posición. Tenga en cuenta que cuando el identificador de capítulo es DB \_ NULL \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
-   Responda al cliente con un mensaje CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 Recibir una solicitud CPMCompareBmkIn

Cuando el servidor recibe una solicitud de mensaje CPMCompareBmkIn del cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador del cursor, el identificador de capítulo y los identificadores de marcador pasados están en las listas correspondientes. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Prepare un mensaje CPMCompareBmkOut.
-   Si los identificadores de marcador son iguales, \_ dwComparison DEBE estar establecido en DBCOMPARE \_ EQ.
-   De lo contrario, si uno de los identificadores de marcador es DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEBE establecerse en DBCOMPARE \_ NE.
-   De lo contrario, el servidor DEBE hacer lo siguiente:
-   -   Buscar filas a las que hace referencia cada identificador de marcador en los resultados de la consulta
    -   Si alguna de las filas no está en el capítulo indicado por el identificador de capítulo en CPMCompareBmkIn, dwComparison DEBE establecerse en \_ DBCOMPARE \_ NOTCOMPARABLE.
    -   De lo contrario, cuando ambas filas están en el mismo capítulo, el servidor DEBE aproximarse a una posición de esas filas en el conjunto de filas al que hace referencia el identificador de este capítulo. A continuación, DEBE comparar los valores de posición y establecer dwComparison en DBCOMPARE LT si la posición de la primera fila es menor que la posición de la segunda fila; de lo contrario, dwComparison DEBE establecerse en \_ \_ \_ DBCOMPARE \_ GT.

-   Responda al cliente con el mensaje CPMCompareBmkOut rellenado.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 Recibir una solicitud CPMRestartPositionIn

Cuando el servidor recibe la solicitud de mensaje CPMRestartPositionIn del cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador del cursor y el identificador de capítulo pasados están en las listas correspondientes. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Mueva el cursor al principio del capítulo, identificado por el identificador del capítulo. Tenga en cuenta que cuando el identificador de capítulo es DB \_ NULL \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta. Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.
-   Responda al cliente con un mensaje CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 Recibir una solicitud CPMFreeCursorIn

Cuando el servidor recibe una solicitud de mensaje CPMFreeCursorIn del cliente, el servidor DEBE hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente. Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).
-   Libere el cursor y los recursos asociados (consulte la sección 3.1.1 para obtener una lista completa) para este identificador de cursor.
-   Quite el cursor de la lista de cursores para ese cliente.
-   Responda con un mensaje CPMFreeCursorOut, estableciendo el campo \_ cCursorsRemaining con el número de cursores restantes. en la lista de este cliente.
-   Si no hay más cursores para este cliente, el servidor DEBE liberar la consulta y los recursos asociados (consulte la sección 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 Recepción de una solicitud CPMDisconnect

Cuando el servidor recibe una solicitud de mensaje CPMDisconnect del cliente, el servidor DEBE quitar el cliente de la lista de clientes conectados y liberar todos los recursos asociados al cliente.

### <a name="316-timer-events"></a>3.1.6 Eventos de temporizador

Ninguno.

### <a name="317-other-local-events"></a>3.1.7 Otros eventos locales

Cuando se detiene el servidor, debe pasar primero al estado "apagar". A continuación, DEBE dejar de escuchar la canalización, realizar cualquier otra tarea de apagado específica de la implementación y, a continuación, realizar la transición al estado "detenido".

### <a name="32-client-details"></a>3.2 Detalles del cliente

### <a name="321-abstract-data-model"></a>3.2.1 Modelo de datos abstractos

En la sección siguiente se especifican los datos y el estado que mantiene el cliente del Protocolo de servicio de indexación de contenido. Los datos proporcionados son para facilitar la explicación de cómo se comporta el protocolo. Esta sección no exige que las implementaciones cumplan este modelo siempre que su comportamiento externo sea coherente con el descrito en este documento.

Un cliente tiene el siguiente estado abstracto:

-   **Último mensaje enviado:** una copia del último mensaje enviado al servidor.
-   **Valor de propiedad actual:** valor parcial de una propiedad "diferida", que está en proceso de recuperación.
-   **Bytes actuales recibidos:** el número de bytes recibidos para el valor de propiedad actual hasta ahora.
-   **Estado de conexión de canalización con nombre:** una conexión al servidor

### <a name="322-timers"></a>3.2.2 Temporizadores

No se requiere ningún temporizador de protocolo.

### <a name="323-initialization"></a>3.2.3 Inicialización

No se realizarán acciones hasta que se reciba una solicitud de capa superior.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 eventos Higher-Layer desencadenados

Cuando se recibe una solicitud de una capa superior, el cliente DEBE crear una conexión de canalización con nombre al servidor con los detalles especificados en la sección 2.1. Si no puede hacerlo, se debe dar error a la solicitud de capa superior. Es decir, en caso de error de conexión, es responsabilidad del nivel superior reintentar si lo desea.

Un encabezado DEBE incluirse previamente con campos establecidos como se especifica en la sección 2.2.2.

Para los mensajes que se especifican como que requieren una suma de comprobación distinta de cero, el \_ valor ulChecksum DEBE calcularse de la siguiente manera:

1.  El contenido del mensaje después del campo ulReserved2 en el encabezado del mensaje DEBE interpretarse como una secuencia de enteros de \_ 32 bits. El cliente DEBE calcular la suma de los valores numéricos especificados por estos enteros.
2.  Calcule el XOR bit a bit de este valor con 0x59533959.
3.  Resta el valor especificado por \_ msg del valor que resulta del XOR bit a bit.

### <a name="3241-remote-indexing-service-catalog-management"></a>3.2.4.1 Remote Indexing Service Catalog Management

Cada mensaje se desencadena mediante una solicitud de la capa superior. No hay ninguna secuencia de mensajes aplicada por el cliente para las solicitudes de mensajes CISP para administrar catálogos de forma remota, pero (a excepción de un mensaje CPMSetCatStateIn), el servidor solo responderá correctamente si el cliente se conectó previamente por medio de un mensaje CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 Envío de una solicitud CPMCiStateInOut

Normalmente, la capa superior pide al cliente de protocolo que envíe un mensaje CPMCiStateInOut cuando requiera información sobre los servicios de indexación en el servidor.

Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:

-   Envíe un mensaje CPMCiStateInOut como se especifica en la sección 2.2.3.1 al servidor.
-   Espere a recibir el mensaje CPMCiStateInOut del servidor, descartando de forma silenciosa todos los demás mensajes.
-   Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la estructura de información de vuelta \_ a la capa superior.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 Envío de una solicitud CPMSetCatStateIn

Normalmente, la capa superior pide al cliente de protocolo que envíe un mensaje CPMSetCatStateIn cuando requiera información sobre un catálogo o todo el catálogo. Para este mensaje, la capa superior debe proporcionar al cliente de protocolo un valor para dwNewState y, si es necesario, el \_ nombre del catálogo.

Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:

-   Envíe un mensaje CPMSetCatStateIn como se especifica en 2.2.3.2 al servidor.
-   Espere a recibir un mensaje CPMSetCatStateOut del servidor, descartando silenciosamente todos los demás mensajes.
-   Informe del valor del campo de estado de la respuesta y, si se ha realizado \_ correctamente, dwOldState de vuelta \_ a la capa superior.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 Envío de una solicitud CPMUpdateDocumentsIn

La capa superior normalmente solicita enviar este mensaje cuando necesita actualizar documentos en la ruta de acceso existente o agregar una nueva ruta de acceso de archivo al índice. Por lo tanto, la capa superior es proporcionar la ruta de acceso y el tipo de un examen, que se especifica como en la sección 2.2.3.4, donde una actualización incremental o completa está pensada para las rutas de acceso existentes, y la inicialización nueva está pensada para nuevas rutas de acceso.

Para atender la solicitud de capa superior, el cliente DEBE hacer lo siguiente:

-   Envíe un mensaje CPMUpdateDocumentsIn como se especifica en la sección 2.2.3.4 al servidor.
-   Espere a recibir el mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.
-   Informe del valor del campo \_ de estado de la respuesta a la capa superior.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 Envío de una solicitud CPMForceMergeIn

Normalmente, la capa superior solicita enviar este mensaje cuando es necesario mejorar el rendimiento de las consultas o forma parte del mantenimiento programado del servicio de indexación.

Para atender la capa superior, el cliente DEBE hacer lo siguiente:

-   Envíe el mensaje CPMForceMergeIn como se especifica en la sección 2.2.3.5 al servidor.
-   Espere a recibir un mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.
-   Informe del valor del campo \_ de estado de la respuesta a la capa superior.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2 Mensajes de consulta del catálogo del servicio de indexación remota

A excepción de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, hay una relación uno a uno entre los mensajes CISP y las solicitudes de nivel superior. Para las dos excepciones mencionadas anteriormente, puede haber varios mensajes generados por el cliente para satisfacer los requisitos de tamaño o para recuperar una propiedad completa. La capa superior suele realizar un seguimiento de toda la información específica de la consulta (por ejemplo, los identificadores de cursor abiertos, los valores legales para los identificadores de marcadores y capítulos, los valores wid para los valores de propiedad diferidos, etc.) y también realiza un seguimiento de si el cliente está en un estado conectado, pero el cliente no lo aplica de ninguna manera.

Con fines ilustrativos, la parte del cliente del diagrama de la sección 3 ilustra esta secuencia para una consulta sencilla de Indexing Service.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 Envío de una solicitud CPMConnectIn

Este mensaje suele ser la primera solicitud de la capa superior (como si el cliente no está conectado, el servidor producirá un error en la mayoría de los mensajes con la excepción de CPMSetCatStateIn). El nivel superior proporciona al cliente de protocolo la información necesaria para conectarse.

Para atender la capa superior, el cliente DEBE hacer lo siguiente:

-   Rellene el mensaje con la información proporcionada por el cliente de capa superior (consulte la sección 2.2.3.6) en \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 y aPropertySet.
-   Establezca \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet y cExtPropSet como se especifica en 2.2.3.6.
-   Establezca la suma de comprobación en \_ el campo ulChecksum.
-   Envíe el mensaje CPMConnectIn al servidor.
-   Espere a recibir un mensaje CPMConnectOut del servidor, descartando silenciosamente todos los demás mensajes.
-   Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, serverVersion de \_ vuelta a la capa \_ superior.

Con fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones tras una conexión correcta, pero el cliente CISP no las aplica:

-   Uso de mensajes de administración remota del catálogo de servicios de indexación para tareas administrativas
-   Use una solicitud CPMCreateQueryIn para crear una consulta de búsqueda con el fin de recuperar los resultados del catálogo.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 Envío de una solicitud CPMCreateQueryIn

La capa superior normalmente proporcionará información para la creación de consultas una vez conectado el cliente de protocolo. La capa superior proporciona al cliente un conjunto de restricciones, un conjunto de columnas, reglas de criterio de ordenación y un conjunto de categorización (se puede omitir cada una de ellas), propiedades de conjunto de filas y estructura del asignador de identificadores de propiedad.

Cuando esta solicitud se recibe de una capa superior, el cliente DEBE hacer lo siguiente:

-   Prepare un CPMCreateQueryOut como se muestra a continuación.
-   -   Si hay un conjunto de columnas, establezca CColumnsSetPreset en 0x01 y rellene el campo ColumnsSet.
    -   Si existen restricciones, establezca CRestrictionPresent en 0x01 y rellene el campo Restricción.
    -   Si hay un conjunto de ordenación, rellene el campo SortSet.
    -   Si hay un conjunto de categorización, establezca CSortSetPresent en 0x01 y rellene el campo CategorizationSet.
    -   Establezca el resto de campos como se especifica en 2.2.3.8.

-   Calcule \_ el campo ulCheckSum en el encabezado.
-   Envíe el mensaje CPMCreateQueryIn al servidor.
-   Espere a recibir el mensaje CPMCreateQueryOut (consulte los detalles de la sección 3.2.5.1.1), descartando de forma silenciosa todos los demás mensajes.
-   Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la matriz de identificadores de cursor y los valores booleanos informativos (como se especifica en \_ 2.2.3.9) de vuelta a la capa superior.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 Envío de una solicitud CPMSetBindingsIn

Normalmente, la capa superior establecerá enlaces para cada columna que se devolverá en las filas cuando ya tenga un identificador de cursor válido (después de recibir correctamente CPMCreateQueryOut, vea la sección 3.2.5.1.1). Se espera que el valor superior proporcione una matriz de estructuras CTableColumn, como se especifica en la sección 2.2.4.31, para el campo aColumns y un identificador de cursor válido.

Cuando se recibe esta solicitud de la capa superior, el cliente DEBE hacer lo siguiente:

-   Calcule el número de estructuras CTableColumn en la matriz aColumns y establezca el campo cColumns en este valor.
-   Calcule el tamaño total en bytes de los campos cColumns y aColumns y establezca el \_ campo cbBindingDesc en este valor.
-   Establezca los campos especificados en el mensaje CPMSetBindingsIn en los valores proporcionados por la capa de aplicación superior. Establezca el \_ campo ulChecksum en el valor calculado como se especifica en la sección 3.2.5.
-   Envíe el mensaje CPMSetBindignsIn completado al servidor.
-   Espere a recibir un mensaje CPMSetBindingsIn del servidor, descartando otros mensajes.
-   Indique el estado del \_ campo de estado de la respuesta a la capa superior.

Con fines informativos, se espera que las capas superiores soliciten normalmente a un cliente que envíe un mensaje CPMGetRowsIn, pero el Protocolo de servicio de indexación de contenido no lo exige.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 Envío de una solicitud CPMGetRowsIn

Cuando la capa superior está a punto de recibir información de filas, proporcionará al cliente de protocolo un identificador de cursor y capítulo válido y proporcionará la descripción de la búsqueda adecuada. Normalmente, se espera que una capa superior lo haga cuando tenga un cursor o un identificador de capítulo válidos, y los enlaces se hubieran establecido con el mensaje CPMSetBindingsIn. Para acceder al conjunto de filas de un capítulo, la capa superior es usar el identificador de capítulo recibido del servidor en un mensaje CPMGetRowsOut anterior.

Cuando se recibe esta solicitud de la capa superior, el cliente DEBE hacer lo siguiente:

-   Determine qué valor entero sin signo se va a especificar para el \_ campo cbReadBuffer. Para determinar este valor, el cliente DEBE tomar el valor máximo de lo siguiente:
-   -   Mil veces el valor del campo \_ RowsToTransfer de c.
    -   Valor de \_ cbRowWidth, redondeado al múltiplo de 512 bytes más cercano.
    -   Tome el valor más alto de estos dos valores, hasta el límite de 16 000.
    -   En los casos en los que una sola fila es mayor que 16 000, el servidor no puede devolver resultados a esta consulta.

Especifique una base de cliente para los datos de fila de tamaño variable en el espacio de direcciones del cliente \_ en el campo ulClientBase.

*Windows Comportamiento: para un cliente de 32 bits que habla con un servidor de 32 bits o un cliente de 64 bits que habla con un servidor de 64 bits, este valor se establece en una dirección de memoria del búfer receptor en el proceso de aplicación. Esto permite que los punteros recibidos en el campo Filas de CPMGetRowsOut sean punteros de memoria correctos en un proceso de aplicación cliente. De lo contrario, se establece en 0x00000000.*

-   Calcule el tamaño de la descripción de la búsqueda y estapóla en el \_ campo cbSeek.
-   Establezca el valor de cbReserved (que actuaría como desplazamiento para el inicio de filas) en el valor \_ de cbSeek más 0x14.
-   Envíe un mensaje CPMConnectIn como se especifica en 2.2.3.15 al servidor.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 Envío de una solicitud CPMFetchValueIn

Si el cliente recibe una respuesta CPMGetRowsOut del servidor con el campo Status de la columna establecido en StatusDeferred (0x01), significa que el valor de propiedad no se incluyó en el campo Rows del mensaje CPMGetRowsOut. En este caso, la capa superior normalmente pide al cliente de protocolo que recupere el valor mediante el mensaje CPMFetchValueIn y proporciona el valor PropSpec y wid para una propiedad diferida, que el cliente de protocolo DEBE usar en el primer mensaje \_ CPMFetchValueIn.

Si este es el primer mensaje CPMFetchValueIn que el cliente ha enviado para solicitar la propiedad especificada, el cliente DEBE hacer lo siguiente:

-   Establezca todos los campos de un mensaje como se especifica en la sección 2.2.3.19.
-   Establezca \_ cbSoFar en 0x00000000.
-   Establezca Bytes actuales recibidos en 0.
-   Envíe el mensaje CPMFetchValueIn al servidor.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 Envío de una solicitud CPMFreeCursorIn

Una vez que el nivel superior ya no usa la consulta de búsqueda, puede liberar los recursos en el servidor solicitando al cliente que envíe un mensaje CPMFreeCursorIn.

Cuando se recibe esta solicitud, el cliente DEBE enviar un mensaje CPMFreeCursorIn como se especifica en 2.2.3.28 al servidor, que contiene el identificador especificado por la capa superior.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 Envío de un mensaje CPMDisconnect

Si la capa superior no tiene más consultas para el servicio de indexación, para liberar más recursos de servidor, la aplicación puede solicitar que el cliente envíe un mensaje CPMDisconnect al servidor. Cuando se recibe esta consulta, el cliente DEBE enviar simplemente el mensaje como se solicitó. No hay ninguna respuesta a este mensaje desde el servidor.

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 Reglas de procesamiento y secuenciación de mensajes

Cuando el cliente recibe una respuesta de mensaje del servidor, el cliente DEBE usar el último mensaje enviado para determinar si el mensaje recibido del servidor es el esperado por el cliente. Todos los mensajes \_ con el campo msg distinto del de Last Send Message DEBEN omitirse.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 Recibir una respuesta CPMCreateQueryOut

Cuando el cliente recibe una respuesta de mensaje CPMCreateQueryOut del servidor, el cliente DEBE devolver el estado y (si el estado es correcto) controlar los valores del cursor de vuelta a una \_ capa superior. Las acciones adicionales están hasta la capa superior.

Como la capa superior es consciente de la estructura de consulta, siempre esperará que se devuelva el número correcto de identificadores de cursor en el mensaje CPMCreateOueryOut. Los identificadores de cursor se devuelven en el orden siguiente: el primer identificador es para el conjunto de filas sin cadena, el segundo es para el primer conjunto de filas con capítulos (que es la agrupación de resultados en función de la primera categoría especificada en el campo CategorizationSet del mensaje CPMCreateQueryIn).

Con fines informativos, se espera que las capas superiores puedan realizar las siguientes acciones, pero el cliente CISP no las aplica:

-   Use CPMSetBindingsIn para establecer enlaces para columnas individuales y realizar las acciones posteriores en la ruta de acceso de consulta.
-   Use CPMGetQueryStatusIn para comprobar el progreso de ejecución de una consulta.
-   Use CPMRatioFinishedIn para solicitar el porcentaje de finalización de la consulta.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 Recibir una respuesta CPMGetRowsOut

Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:

-   Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no.
-   Si el \_ valor de estado es STATUS BUFFER TOO SMALL (0xC0000023), el cliente \_ DEBE comprobar el estado Último mensaje \_ \_ enviado. Si no contiene un mensaje CPMGetRowsIn, el mensaje recibido DEBE omitirse en modo silencioso. De lo contrario, el cliente DEBE enviar al servidor un nuevo mensaje CPMGetRowsIn con todos los campos idénticos al almacenado, excepto que cbReadBuffer DEBE aumentarse en 512 (pero no mayor que \_ 0x4000). Si el estado es STATUS BUFFER TOO SMALL (0xC0000023) y El último mensaje enviado ya tiene \_ \_ cbReadBuffer igual a 0x4000 el cliente DEBE notificar el error hasta el \_ \_ nivel \_ superior.
-   Si el \_ valor de estado es cualquier otro valor de error, el cliente DEBE indicar el error hasta la capa superior.
-   Si el valor de estado indica que se ha producido correctamente, los resultados SE DEBEN indicar hasta la capa superior que solicita la información, y las acciones adicionales están hasta \_ la capa superior.

Con fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones, pero el cliente del Protocolo de servicio de indexación de contenido no las aplica:

-   Si los valores de las filas representan los identificadores de documento, los identificadores de capítulo o marcador de la capa superior normalmente los almacenarán para su uso en operaciones posteriores que implican identificadores de documento, capítulos o identificadores de marcador válidos.
-   La capa superior normalmente almacenará o mostrará o usará los datos de los valores de fila.
-   Para los valores que se marcaron como capas más altas diferidas, se capturará el valor mediante mensajes CPMFetchValueIn.
-   La descripción de la búsqueda también se devuelve a una capa superior y la capa superior puede reutilizarla o examinarla.

Con fines informativos, si la capa superior solicitó identificadores a capítulos y marcadores que se recibieron en las filas, puede hacer lo siguiente:

-   Use CPMGetQueryStatusExIn para comprobar el progreso de ejecución de una consulta, así como información de estado adicional, como el número de documentos filtrados, los documentos que quedan por filtrar, la proporción de documentos procesados por la consulta, el número total de filas de la consulta y la posición del marcador en el conjunto de filas.
-   Use CPMGetNotify para solicitar que el servidor notifique al cliente los cambios del conjunto de filas.
-   Use CPMGetApproximatePositionIn para solicitar la posición aproximada de un marcador en un capítulo.
-   Use CPMCompareBmkIn para solicitar una comparación de dos marcadores en un capítulo.
-   Use CPMRestartPositionIn en el servidor para cambiar la ubicación del cursor al inicio del conjunto de filas.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 Recepción de una respuesta CPMFetchValueOut

Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:

-   Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no. En caso de error, notifique a la capa superior. De lo contrario, continúe a continuación.
-   Active fValueExist y, si se establece en 0x00000000 informe a la capa \_ superior de que no se encontró el valor.
-   De lo contrario, \_ anexe los bytes cbValue de vValue al valor de propiedad actual.
-   Si fMoreExists se establece en 0x00000001, incremente los bytes actuales recibidos por cbValue y envíe un mensaje \_ \_ \_ \_ CPMFetchValueIn al servidor, estableciendo cbSoFar en el valor de \_ Bytes actuales recibidos, cbPropSpec en cero y \_ \_ cbChunk en el tamaño de búfer deseado por la capa superior.
-   Si fMoreExists se establece en 0x00000000, indique el valor de propiedad de Valor de \_ propiedad actual a la capa superior.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 Recibir una respuesta CPMFreeCursorOut

Cuando el cliente recibe una respuesta de mensaje CPMFreeCursorOut correcta del servidor, el cliente DEBE devolver el valor \_ cCursorsRemaining a la capa superior.

La siguiente información se proporciona solo con fines informativos y no se aplica por el cliente CISP. Se espera que la capa superior realice un seguimiento de los identificadores de cursor y no use los que ya se han liberado. Una vez que el número de cCursorsRemaining es igual a 0x00000000, la capa superior puede usar la conexión para especificar otra consulta (mediante un \_ mensaje CPMCreateQueryIn).

### <a name="326-timer-events"></a>3.2.6 Eventos de temporizador

Ninguno.

### <a name="327-other-local-events"></a>3.2.7 Otros eventos locales

Ninguno.

## <a name="4-protocol-examples"></a>4 Ejemplos de protocolo

-   [4.1 Ejemplo 1](#41-example-1)
-   [4.2 Ejemplo 2](#42-example-2)

### <a name="41-example-1"></a>4.1 Ejemplo 1

En el ejemplo siguiente, se considera un escenario en el que el usuario JOHN del equipo A quiere obtener los tamaños de los archivos que contienen la palabra "Microsoft" del conjunto de documentos almacenados en el servidor X en el catálogo SYSTEM. Supongamos que la máquina A ejecuta un sistema operativo Windows XP de 32 bits y la máquina X ejecuta un sistema operativo de 32 bits Windows Server 2003.

1.  El usuario inicia una aplicación de búsqueda y escribe la consulta de búsqueda. A su vez, la aplicación pasa la consulta de búsqueda al cliente de protocolo.
2.  El cliente de protocolo establece una conexión con el servidor de indexación X. El cliente de protocolo usa la \\ canalización con nombre CI TFTPDS para \\ \_ conectarse al servidor X a través de SMB.
3.  A continuación, el cliente de protocolo prepara un mensaje CPMConnectIn con los valores siguientes:

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectIn.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada como se especifica en la sección 3.2.4.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ iClientVersion** se establece en 0x00000008, lo que indica que el servidor va a validar el campo de suma de comprobación.
    -   **\_ fClientIsRemote** se establece en 0x00000001, lo que indica que el servidor es un servidor remoto.
    -   **\_ cbBlob1 se** establece en el tamaño, en bytes, de los campos cPropSet, PropertySet1 y PropertySet2 combinados.
    -   **\_ cbBlob2** se establece en 0x00000004 (lo que significa que no hay conjuntos de propiedades adicionales).
    -   **MachineName** se establece en A.
    -   **UserName** se establece en JOHN.
    -   **cPropSets** se establece en 0x00000002.
    -   **El campo PropertySet1** es de tipo CDbPropSet. La estructura CDbPropSet que contiene el campo PropertySet1 se rellena de la siguiente manera:
        -   **El campo GuidPropSet** se establece en A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).
        -   **El campo cProperties** se establece en 0x00000004.
        -   **El campo aProps** es una matriz de estructuras CDbProp.

            Para el **elemento aProps \[ 0: \]**

            -   **PropId** se establece en 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS se** establece en 0x00000000.
            -   Para el **elemento ColId:**
                -   **eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID)
                -   **GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el **elemento vValue:**
                -   **vType** se establece en 0x001F (VT \_ LPWSTR).
                -   **vValue** se establece en "SYSTEM", el nombre del catálogo deseado.

            Para el **elemento aProps \[ 1: \]**

            -   **PropId** se establece en 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS se** establece en 0x000000000.
            -   Para el **elemento ColId:**
                -   **eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el **elemento vValue:**
                -   **vType** se establece en 0x0003 (VT \_ I4).
                -   **vValue** se establece en 0x00000000 (CiNormal), lo que significa que es una consulta normal.

            Para el **elemento aProps \[ 2: \]**

            -   **PropId** se establece en 0x00000004 (MARCAS DE ÁMBITO \_ DE CI DE \_ \_ DBPROP).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS se** establece en 0x00000000.
            -   Para el **elemento ColId:**
                -   **eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el **elemento vValue:**
                -   **vType**: 0x1003 (VT \_ VECTOR VT \| \_ I4)
                -   **vValue:** 0x00000001 /0x00000001 (un elemento con el valor 1), lo que significa subcarpetas de búsqueda

            Para el **elemento aProps \[ 3: \]**

            -   **PropId**: 0x00000003 (ÁMBITOS DE INCLUIR \_ DE CI DE \_ \_ DBPROP)
            -   **DBPROPOPTIONS:** 0x0000000
            -   **DBPROPSTATUS:** 0x00000000
            -   Para el **elemento ColId:**
                -   **eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.
                -   **ulID** se establece en 0x00000000
            -   Para el **elemento vValue:**
                -   **vType** se establece en 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).
                -   **vValue** se establece en 0x00000001 / 0x00000002 / " " (un elemento con una cadena terminada en NULL de 2 caracteres), lo que significa el \\ ámbito raíz.

    -   El **campo PropertySet2** es de tipo CDbPropSet.

        La estructura CDbPropSet que contiene el campo PropertySet1 se rellena de la siguiente manera:

        -   **GuidPropSet** se establece en AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).
        -   **El campo cProperties** se establece en 0x00000001.
        -   El **campo aProps** es una matriz de estructuras CDbProp.

            Para el **elemento aProps \[ 0: \]**

            -   **PropId** se establece en 0x00000002 (DBPROP \_ MACHINE).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS se** establece en 0x00000000.
            -   Para el **elemento ColId:**
                -   **eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID),
                -   **GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.
                -   **ulID** se establece en 0x00000000.
            -   Para **el elemento vValue:**
                -   **vType**: 0x0008 (VT \_ BSTR)
                -   **vValue:** 0x04 / "X" (4 bytes / cadena Unicode terminada en NULL), lo que significa "X" -name de un servidor.

    -   **El campo cExtPropSet** se establece en 0x00000000.
    -   **la matriz aPropertySets** no existe.
    -   Se rellenan varios campos de relleno según sea necesario. El mensaje se envía al servidor.

4.  El servidor comprueba que **\_ ulChecksum** es correcto, comprueba que el usuario está autorizado para realizar esta solicitud y responde con un mensaje CPMConnectOut.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectOut.
    -   **\_ status** se establece en 0x0000000 que indica SUCCESS.
    -   **\_ ulChecksum** se establece en 0.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ El campo serverVersion** se establece en 0x00000007 (32 bits Windows XP o 32 bits Windows Server 2003).
    -   **\_ Los** campos reservados se rellenan con datos arbitrarios.

5.  El cliente prepara un mensaje CPMCreateQueryIn.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryIn.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada según la versión 3.2.5.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **El** campo Tamaño se establece en el tamaño del resto del mensaje.
    -   **El campo CColumnSetPresent** se establece en 0x01.
    -   **El campo ColumnSet** es de tipo CColumnSet. La estructura CColumnSet que contiene este campo se establece de la siguiente manera:
        -   **\_ count** field se establece en 0x00000001 indica que se devuelve una columna.
        -   **La** matriz indexes 0x00000000 indica la primera entrada de \_ aPropSpec.
    -   **El campo CRestrictionPresent** se establece en 0x01 que indica que **el campo Restricción** está presente.
    -   **El** campo Restricción es de tipo CRestriction y se establece en:
        -   **\_ ulType** se establece en 0x00000004 (RTContent).
        -   **\_ weight** se establece en 0x00000000.
    -   El resto del campo contiene una estructura CContentRestriction:
        -   **\_ La** propiedad se establece en GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (para PRSPEC PROPID) / 0x13 que representa el cuerpo \_ del documento.
        -   **\_ Cc** se establece en 0x00000009.
        -   **\_ pwcsphrase** se establece en la cadena "Microsoft".
        -   **\_ lcid** se establece en 0x409 (para inglés).
        -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).
    -   **CSortPresent** se establece en 0x00.
    -   **CCategorizationSetPresent** se establece en 0x00.
    -   **RowSetProperties** se establece de la siguiente manera:
        -   **\_ uBooleanOptions** se establece en 0x00000001 (secuencial).
        -   **\_ ulMaxOpenRows** se establece en 0x00000000.
        -   **\_ ulMemoryUsage** se establece en 0x00000000.
        -   \_**cMaxResults** se establece en 0x00000100 (devuelve como máximo 256 filas).
        -   **\_ cCmdTimeOut se** establece en 0x00000000 (tiempo de espera nunca).
    -   **PidMapper** se establece en:
        -   **\_ count** se establece en 0x00000001.
        -   **\_ aPropSpec se** establece en GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ Windows.

6.  El servidor lo procesa y responde con un mensaje CPMCreateQueryOut.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryOut.
    -   **\_ status** se establece en SUCCESS.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ fTrueSeqeuntial** se establece en 0x00000000, lo que indica que la consulta puede usar un índice.
    -   **\_ fWorkIdUnique** se establece en 0x00000001.
    -   La **matriz aCursors** contiene solo un elemento, que representa un identificador de cursor para esta consulta. El valor depende del estado del servidor. Supongamos que el valor devuelto es 0xAAAAAAAA.

7.  El cliente emite un mensaje de solicitud CPMSetBindingsIn para definir el formato de una fila.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000D0, lo que indica que se trata de un mensaje CPMSetBindingsIn.
    -   **\_ status** se establece en SUCCESS.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ hCursor** se establece en 0xAAAAAAAA.
    -   **\_ cbRow** se establece en 0x10 (lo suficientemente grande como para caber columnas).
    -   **\_ cbBindingDesc** se establece en el tamaño de los campos **\_ cColumns** y **\_ aColumns** combinados.
    -   **\_ cColumns** se establece en 0x00000001.
    -   **\_ La matriz aColumns** se establece para contener una estructura CTableColumn que contiene:
    -   -   **\_ PropSpec** se establece en GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ Windows.
        -   **\_ vType** se establece en 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed** se establece en 0x01 (columna transferida en fila).
        -   **\_ ValueOffset** se establece en 0x0002 (al principio de la fila).
        -   **\_ ValueSize** se establece en 0x08 (tamaño de una \_ UI8 de VT).
        -   **\_ StatusUsed** se establece en 0x01.
        -   **\_ StatusOffset** se establece en 0x0A.
        -   **\_ LengthUsed** se establece en 0x00.

8.  El servidor lo procesa y responde con un mensaje CPMSetBindingsIn.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000D0.
    -   **\_ status** se establece en SUCCESS.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

9.  El cliente emite un mensaje de solicitud CPMGetRowsIn. Supongamos que el cliente está preparado para aceptar 100 filas en este momento y las quiere en orden ascendente.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsIn.
    -   **\_ status** se establece en 0x00000000
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada según la sección 0.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ hCursor** se establece en 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** se establece en 0x00000064.
    -   **\_ cRowWidth** se establece en 0x00000010 (desde enlaces).
    -   **\_ cbSeek** se establece en 0x14 que es el tamaño de los campos eType, chapt y \_ CRowSeekNext combinados.
    -   **\_ cbReserved** se establece en 0x18 (0x14 más \_ cbSeek).
    -   **\_ cbReadBuffer** se establece en 0x800 (0x64 0x10 redondea al siguiente \* múltiplo de 0x200).
    -   **\_ ulClientBase** se establece en 0x00000000.
    -   **\_ fBwdfetch** se establece en 0x00000000 indica que las filas se van a capturar en orden de avance.
    -   **eType** se establece en 0x0000001 indica que el cliente quiere las filas siguientes.
    -   **\_ chapt** se establece en 0 (no en un resultado con capítulos).
    -   **SeekDescription** se establece en CRowSeekNext. La estructura CRowSeekNext contiene los valores siguientes:
        -   **CiTblChapt** se establece en 0x00000000.
        -   **\_ hRegion** se establece en 0x00000000.
        -   **\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.

10. El servidor lo procesa y responde con un mensaje CPMGetRowsOut. Supongamos que el servidor encontró 100 documentos que contienen la palabra "Microsoft".

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsOut.
    -   **\_ status** se establece en SUCCESS.
    -   **\_ ulChecksum** se establece en 0x00000000.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ CRowsReturned** se establece en 0x00000064.
    -   **eType** se establece en 0x00000001.
    -   **\_ chapt** se establece en 0x00000000 (no en un resultado con capítulos).
    -   **SeekDescription** contiene una estructura CRowSeekNext, rellenada de la siguiente manera:
        -   **CiTblChapt** se establece en 0x00000000.
        -   **\_ hRegion** se establece en 0x00000000.
        -   **\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.
    -   **Las** filas contienen el tamaño de los 100 documentos que contienen la palabra "Microsoft". Dado que se trata de datos de tamaño fijo, simplemente se estructura como una lista de enteros de 100 y 8 bytes sin signo.

11. El cliente envía un mensaje CPMDisconnect para finalizar la conexión.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ msg** se establece en 0x000000C9, lo que indica que se trata de un mensaje CPMDisconnect.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** se establece en 0x00000000.

12. El servidor procesa el mensaje y quita todo el estado de cliente.

### <a name="42-example-2"></a>4.2 Ejemplo 2

En el ejemplo anterior, la consulta era bastante sencilla. Ahora vamos a considerar una consulta ligeramente más compleja. Supongamos que el usuario quiere recuperar el tamaño de los documentos que contienen las palabras siguientes: "Microsoft" y "Office". Esto se especifica cambiando el campo Restricción contenido en el mensaje CPMCreateQueryIn enviado en el paso 5 como se indica a continuación:

El **campo** Restricción es de tipo CRestriction y se establece en:

-   -   **\_ ulType** se establece en 0x00000004 (RTAnd).
    -   **\_ weight** se establece en 0x00000000.

El resto del campo contiene una estructura CNodeRestriction:

-   -   **\_ cNode** se establece en 0x00000002, lo que indica que hay dos nodos en la matriz paNode.
    -   El **\_ campo paNode** es una matriz de dos estructuras CRestriction.

        **\_ paNode \[ \] 0** contiene:

        -   -   **\_ ulType** se establece en 0x00000004 (RTContent).
            -   **\_ weight** se establece en 0x00000000.
            -   El resto del campo contiene una estructura CContentRestriction:
                -   **\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.
                -   **\_ Cc** se establece en 0x00000009.
                -   **\_ pwcsphrase** se establece en la cadena "Microsoft".
                -   **\_ lcid** se establece en 0x409 (para inglés).
                -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).

        **\_ paNode \[ \] 1** contiene:

        -   -   **\_ ulType** se establece en 0x00000004 (RTContent).
            -   **\_ weight** se establece en 0x00000000.
            -   El resto del campo contiene una estructura CContentRestriction:
                -   **\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.
                -   **\_ Cc** se establece en 0x00000006.
                -   **\_ pwcsphrase** se establece en la cadena "Office".
                -   **\_ lcid** se establece en 0x409 (para inglés).
                -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).

## <a name="5-security"></a>5 Seguridad

### <a name="51-security-considerations-for-implementers"></a>5.1 Consideraciones de seguridad para los implementadores

Las implementaciones de indexación que indexa el contenido seguro deben considerar la posibilidad de usar el contexto de usuario proporcionado por SMB MS-SMB para recortar los resultados de la búsqueda y devolver solo los accesibles para \[ el autor de la \] llamada.

### <a name="52-index-of-security-parameters"></a>5.2 Índice de parámetros de seguridad



| Parámetro de seguridad  | Sección |
|---------------------|---------|
| Nivel de suplantación | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Índice del comportamiento específico de la versión



| Comportamiento específico de la versión                                                                         | Sección   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista. | 1.3.2     | X            | X          | X                   |
| Las aplicaciones normalmente interactúan con un contenedor OLE DB interfaz                                  | 1.4       | X            | X          | X                   |
| Valores NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| El cliente establece el campo \_ de estado en cada encabezado de mensaje.                                        | 2.2.2     | X            | X          | X                   |
| El valor de cPendingScans suele ser cero                                                               | 2.2.3.1   | X            | X          | X                   |
| Valor de iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_cbChunk value                                                                                   | 2.2.3.19  | X            | X          | X                   |
| Direcciones de memoria de 32 y 64 bits                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





