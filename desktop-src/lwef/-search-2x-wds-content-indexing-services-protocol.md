---
title: Protocolo de servicios de indexación de contenido
description: Este documento es una especificación del protocolo del servicio de indización de contenido.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789316"
---
# <a name="content-indexing-services-protocol"></a>Protocolo de servicios de indexación de contenido

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Especificación del Protocolo, versión 0,12

-   [1 Introducción](#1-introduction)
    -   [1.1 Glosario](#11-glossary)
    -   [1.2 Referencias](#12-references)
    -   [Información general del protocolo 1,3 (Sinopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Relación con otros protocolos](#14-relationship-to-other-protocols)
    -   [1,5 requisitos previos y condiciones previas](#15-prerequisites-and-preconditions)
    -   [1.6 Declaración de aplicabilidad](#16-applicability-statement)
    -   [1.7 Control de versiones y negociación de funcionalidad](#17-versioning-and-capability-negotiation)
    -   [1.8 Campos extensibles por el proveedor](#18-vendor-extensible-fields)
    -   [1.9 Asignaciones de estándares](#19-standards-assignments)
-   [2 Mensajes](#2-messages)
    -   [2.1 Transporte](#21-transport)
    -   [2.2 Sintaxis de mensajes](#22-message-syntax)
-   [3 Detalles del protocolo](#3-protocol-details)
    -   [Detalles del servidor 3,1](#31-server-details)
    -   [Detalles del cliente 3,2](#32-client-details)
-   [4 Ejemplos de protocolo](#4-protocol-examples)
    -   [4,1 ejemplo 1](#41-example-1)
    -   [ejemplo 2 de 4,2](#42-example-2)
-   [5 Seguridad](#5-security)
    -   [5.1 Consideraciones de seguridad para los implementadores](#51-security-considerations-for-implementers)
    -   [5.2 Índice de parámetros de seguridad](#52-index-of-security-parameters)
-   [6 índice de comportamiento específico de la versión](#6-index-of-version-specific-behavior)

Este documento es una especificación del protocolo del servicio de indización de contenido.

La documentación del programa de protocolo de servidor de grupo de trabajo (WSPP) está pensada para su uso junto con la documentación de estándares públicos, material de programación para redes y conceptos de sistemas distribuidos de Windows Workgroup, y da por supuesto que el lector está familiarizado con el material mencionado anteriormente o tiene acceso inmediato a él.

Una especificación del protocolo WSPP no requiere el uso de las herramientas de programación de Microsoft o los entornos de programación para que un licenciatario desarrolle una implementación. Los licenciatarios que tienen acceso a las herramientas y los entornos de programación de Microsoft pueden aprovecharlos de forma gratuita.

## <a name="1-introduction"></a>1 Introducción

-   [1.1 Glosario](#11-glossary)
-   [1.2 Referencias](#12-references)
-   [Información general del protocolo 1,3 (Sinopsis)](#13-protocol-overview-synopsis)
-   [1.4 Relación con otros protocolos](#14-relationship-to-other-protocols)
-   [1,5 requisitos previos y condiciones previas](#15-prerequisites-and-preconditions)
-   [1.6 Declaración de aplicabilidad](#16-applicability-statement)
-   [1.7 Control de versiones y negociación de funcionalidad](#17-versioning-and-capability-negotiation)
-   [1.8 Campos extensibles por el proveedor](#18-vendor-extensible-fields)
-   [1.9 Asignaciones de estándares](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glosario

> [!Note]  
> Los siguientes términos se definen en la sección Glosario de \[ MS-sys \] :
>
> -   GUID
> -   Little endian
> -   Canalización con nombre
> -   Ruta

 

**Binding**: una solicitud para incluir una **columna** determinada en un **conjunto de filas** devuelto. El **enlace** especifica una propiedad que se va a incluir en los resultados de la búsqueda.

**Marcador**: un marcador que identifica de forma única una fila dentro de un conjunto de filas.

**Catálogo**: la unidad de la organización de nivel superior del servicio de Index Server. Representa un conjunto de documentos indizados en los que se pueden ejecutar consultas mediante el protocolo del servicio de indización de contenido.

**Categoría**: una agrupación jerárquica de filas. Por ejemplo, el resultado de una consulta que contiene columnas de autor y título se puede clasificar en función del autor. Cada grupo de filas que contiene el mismo valor para autor constituiría una categoría.

**Chapter** : un intervalo de **filas** dentro de un conjunto de **filas** .

**Columna**: el contenedor para un único tipo de información de una **fila** . Las columnas se asignan a los nombres de propiedad y especifican las propiedades que se usan para los elementos de **árbol** de **comandos** de la consulta de búsqueda.

**Árbol de comandos**: combinación de **restricciones** , **categorías** y **criterios de ordenación** especificados para la consulta de búsqueda.

**Cursor**: una entidad que se usa como mecanismo para trabajar con una **fila** o un pequeño bloque de **filas** a la vez en un conjunto de datos devueltos en un conjunto de resultados. Un **cursor** se coloca en una única **fila** dentro del conjunto de resultados. Una vez que el **cursor** se coloca en una fila, se pueden realizar operaciones en esa **fila** o en un bloque de **filas** a partir de esa posición.

**Handle**: un token que se puede usar para identificar y tener acceso a **cursores** , **capítulos** y **marcadores** .

**Index**: estructura persistente que contiene el contenido de texto extraído de archivos por un **servicio de indización** . Esto incluye la lista de palabras, que se almacenan junto con el nombre de archivo contenedor, la ubicación de la palabra y la **configuración regional** .

**Indexación**: proceso de extracción de texto y propiedades de archivos y almacenamiento de los valores extraídos en los **índices** (para texto) y **en la caché de propiedades** (para propiedades).

**Servicio de indexación**: servicio que crea **catálogos** indexados para el contenido y las propiedades de los sistemas de archivos. Las aplicaciones pueden buscar información en los catálogos de los archivos del sistema de archivos indizado.

**Locale**: un identificador, como se especifica en el apéndice a de \[ MS-GPSI \] , que especifica las preferencias relacionadas con el idioma. Estas preferencias indican cómo se va a dar formato a las fechas y horas, los elementos se ordenarán alfabéticamente, las cadenas se compararán, etc.

**Consulta en lenguaje natural**: consulta construida con la sintaxis de consulta de lenguaje humano en lugar de.

**Palabra irrelevante**: palabra omitida por el servicio de indización cuando está presente en las **restricciones** especificadas para la consulta de búsqueda porque tiene un pequeño valor discriminado. Entre los ejemplos en inglés se incluyen "a", "and" y "The".

**Caché** de propiedades: memoria caché de propiedades de archivo extraídas por un **servicio de indización** .

**Indexación de propiedades**: proceso de creación de un **Índice** de propiedades de **tipo de valor** de un documento, incluidos el autor, el asunto, el tipo, el recuento de palabras, el recuento de páginas impresas y cualquier otra propiedad.

**Restricción**: un conjunto de condiciones que un archivo debe cumplir para que se incluyan en los resultados de búsqueda devueltos por el **servicio de indización** en respuesta a una consulta de búsqueda. Una **restricción** reduce el foco de una consulta de búsqueda, limitando los archivos que el **servicio de indexación** incluirá en los resultados de la búsqueda a solo aquellos que cumplan las condiciones.

**Row**: la colección de **columnas** , que contiene los valores de propiedad que describen un solo archivo del conjunto de archivos que coinciden con las **restricciones** especificadas en la consulta de búsqueda enviada al **servicio de indización** .

Conjunto de **filas**: conjunto de **filas** devueltas en los resultados de la búsqueda.

Criterio de **ordenación**: conjunto de reglas de una consulta de búsqueda que definen el orden de las filas en el resultado de la búsqueda. Cada regla se compone de una propiedad (nombre, tamaño, etc.) y una dirección para la ordenación (ascendente o descendente). Varias reglas se aplican secuencialmente

**Propiedad de tipo de texto**: una propiedad que describe el contenido de un documento y solo tiene texto sin formato asociado a su nombre.

**Propiedad de tipo de valor**: una propiedad que describe un solo atributo de un documento completo. Una propiedad de tipo de valor tiene un identificador de tipo de datos y un valor de ese tipo de datos asociado a su nombre.

**Raíz virtual**: ruta de acceso alternativa a una carpeta. Una carpeta física puede tener cero o más raíces virtuales. Las rutas de acceso que comienzan por una raíz virtual se denominan rutas de acceso virtuales. Por ejemplo,/Server/vanityroot podría ser una raíz virtual de C: \\ IIS \\ Web \\ Folder1. A continuación, el archivo C: \\ IIS \\ web \\ Folder1 \\default.htm tendría una ruta de acceso virtual de/Server/vanityroot/default.htm.

**Mayo,** debe, no debe, no debe: estos términos (en mayúsculas) se usan tal y como se describe en \[ RFC2119 \] . Todas las instrucciones de comportamiento opcional utilizan MAY, SHOULD o SHOULD NOT.

### <a name="12-references"></a>1.2 Referencias

### <a name="121-normative-references"></a>1.2.1 Referencias de normativa

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point aritmético", IEEE 754-1985, 1985 de octubre, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "protocolos remotos del modelo de objetos de componentes distribuidos", el 2006 de junio.

\[MS-GPSI \] Microsoft Corporation, "Directiva de grupo de instalación de software Extension", junio 2006.

\[MS-SMB \] Microsoft Corporation, "Protocolo de bloque de mensajes del servidor de Microsoft (SMB) y extensiones", 2006 de mayo.

\[MS-SYS \] Microsoft Corporation, "información general del sistema V4", 2006 de julio.

\[SALTon \] salon, G., "procesamiento de texto automático: el análisis y la recuperación de la información por equipo", 1988 y ISBN 0-201-2227-8.

\[Unicode \] (Unicode Consortium), "The Unicode Standard, Version 2,0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Referencias informativas

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valores, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>Información general del protocolo 1,3 (Sinopsis)

Un **servicio de indización** de contenido ayuda a organizar de manera eficaz las características extraídas de una colección de documentos. El protocolo del servicio de indización de contenido (CISP) permite a un cliente comunicarse con un servidor que hospeda un servicio de indización para emitir consultas y permitir que un administrador administre el servidor de indexación.

Al procesar archivos, un servicio de indización analiza un conjunto de documentos y reorganiza su contenido de tal forma que **las propiedades** de esos documentos se pueden devolver eficazmente en respuesta a las consultas. Una colección de documentos que se pueden consultar se compone de un **Catálogo** . Un catálogo puede contener un **Índice** (para una referencia rápida a texto) y una **caché de propiedades** (para una recuperación rápida de los valores de propiedad).

Conceptualmente, un catálogo consta de una "tabla" lógica de propiedades con el texto o el valor y la configuración regional correspondiente almacenada en **las columnas** de la tabla. Cada "fila" de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada "columna" de la tabla corresponde a una propiedad.

Las tareas específicas realizadas por CISP se agrupan en dos áreas funcionales:

-   Administración remota de catálogos de servicios de Index Server,
-   Consulta remota de catálogos de servicios de Index Server.

### <a name="131-remote-administration-tasks"></a>1.3.1 tareas de administración remota

CISP permite las siguientes tareas de administración de catálogos de servicios de Index Server desde un cliente:

-   Consultar el estado actual de un catálogo de servicios de Index Server en el servidor.
-   Actualice el estado de un catálogo de servicios de Index Server.
-   Inicia el proceso de indización de un conjunto determinado de archivos.
-   Inicie la optimización de un índice con el fin de mejorar el rendimiento de las consultas.

Todas las tareas de administración remota siguen un modelo de solicitud/respuesta simple. No se mantiene ningún estado en el cliente para ninguna llamada de administración y las llamadas administrativas se pueden realizar en cualquier orden.

### <a name="132-remote-querying"></a>1.3.2 consultas remotas

CISP permite a los clientes realizar consultas de búsqueda en un servidor remoto que hospeda un servicio de indexación.

El envío de una consulta de búsqueda es un proceso de varios pasos Iniciado por el cliente. Los pasos son los siguientes:

1.  El cliente solicita una conexión a un servidor que hospeda un servicio de indización.
2.  El cliente envía los parámetros de la consulta de búsqueda, que incluyen:
    -   Las **restricciones** para especificar qué documentos se van a incluir o excluir de los resultados de la búsqueda.
    -   El orden en el que se van a devolver los resultados de la búsqueda.
    -   Columnas que se van a devolver en el conjunto de resultados.
    -   Número máximo de **filas** que se deben devolver para la consulta.
    -   Tiempo máximo de ejecución de la consulta.

        Una vez que el servidor ha confirmado la solicitud del cliente para iniciar la consulta, el cliente puede solicitar información de estado sobre la consulta, pero no es un paso necesario.

3.  Después, el cliente especifica las propiedades que el servidor debe incluir en los resultados de la búsqueda.
4.  El cliente solicita un conjunto de resultados del servidor y el servidor responde enviando al cliente los valores de propiedad de los archivos incluidos en los resultados de la consulta de búsqueda del cliente. Si el valor de una propiedad es demasiado grande para caber en un búfer de respuesta único, el servidor no enviará la propiedad pero, en su lugar, establecerá el estado de la propiedad en diferido. Después, el cliente solicita el valor de propiedad por separado usando una serie de solicitudes para fragmentos sucesivos del valor y, a continuación, reanuda la solicitud de otros valores.
5.  Una vez que el cliente finaliza con la consulta de búsqueda y ya no requiere resultados adicionales, el cliente se pone en contacto con el servidor para liberar la consulta.
6.  Una vez que el servidor haya lanzado la consulta, el cliente puede enviar una solicitud para desconectarse del servidor. A continuación, se cierra la conexión. Como alternativa, el cliente puede emitir otra consulta y repetir la secuencia del paso 2.

Comportamiento de Windows: este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relación con otros protocolos

CISP se basa en el protocolo SMB \[ MS-SMB \] para el transporte de mensajes. Ningún otro protocolo depende directamente del protocolo del servicio de indización de contenido.

*Comportamiento de Windows: las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB \[ MSDN-OleDb \] (por ejemplo, un cliente de protocolo) y no directamente con el protocolo.*

### <a name="15-prerequisites-and-preconditions"></a>1,5 requisitos previos y condiciones previas

Se supone que el cliente ha obtenido el nombre del servidor y un nombre de catálogo antes de que se invoque este protocolo. Cómo hace un cliente esto está fuera del ámbito de esta especificación.

También se supone que el cliente y el servidor tienen una asociación de seguridad que se puede usar con las canalizaciones con nombre \[ MS-SMB \] .

### <a name="16-applicability-statement"></a>1.6 Declaración de aplicabilidad

CISP está diseñado para consultar y administrar catálogos en un servidor remoto desde un cliente. CISP está en desuso en Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Control de versiones y negociación de funcionalidad

Este protocolo no tiene ningún mecanismo de control de versiones o de negociación de capacidad.

### <a name="18-vendor-extensible-fields"></a>1.8 Campos extensibles por el proveedor

Este protocolo usa Valores HRESULT que son extensibles. Los proveedores pueden elegir sus propios valores para este campo, siempre que el bit C (0x20000000) esté establecido como se especifica en la sección 4.1.1 de \[ MS-sys \] , lo que indica que es un código de cliente.

Este protocolo también usa los valores de NTSTATUS tomados del espacio de número de NTSTATUS definido en \[ MS-sys \] . Los proveedores deben reutilizar esos valores con el significado indicado. Al elegir cualquier otro valor se corre el riesgo de una colisión en el futuro.

*Comportamiento de Windows: Windows solo usa los valores especificados en la sección 4.1.3 de \[ MS-sys \] .*

### <a name="181-property-ids"></a>Identificadores de propiedad de 1.8.1

Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad. Cada propiedad debe tener un identificador único global. Este identificador se compone de un **GUID** que representa una colección de propiedades denominada un conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto. Si se utiliza la forma de entero de ID, se considera que los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE no son válidos.

Los proveedores pueden garantizar que sus propiedades se definen de forma exclusiva colocándolas en un conjunto de propiedades definido por su propio GUID.

### <a name="19-standards-assignments"></a>1.9 Asignaciones de estándares

Este protocolo no tiene asignaciones de estándares, solo las asignaciones privadas realizadas por Microsoft mediante procedimientos de asignación especificados en otros protocolos.

Microsoft ha asignado a este protocolo una canalización con nombre, tal y como se especifica en \[ MS-SMB \] . La asignación es:



| Parámetro | Value             | Referencia  |
|-----------|-------------------|------------|
| Nombre de canalización | \\canalización de \\ CI \_ SKADS | \[SMB DE MS\] |



 

## <a name="2-messages"></a>2 Mensajes

-   [2.1 Transporte](#21-transport)
-   [2.2 Sintaxis de mensajes](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transporte

Todos los mensajes se deben transportar mediante una canalización con nombre, como se especifica en \[ MS-SMB \] . Se usa el siguiente nombre de canalización:

-   \\canalización de \\ CI \_ SKADS

Este protocolo usa el protocolo de canalización con nombre SMB subyacente para recuperar la identidad del autor de la llamada que realizó la conexión como se especifica en la sección 2.2.8 de \[ MS-SMB \] ; el cliente debe establecer la identificación de seguridad \_ como ImpersonationLevel en la solicitud para abrir la canalización con nombre.

### <a name="22-message-syntax"></a>2.2 Sintaxis de mensajes

Varias estructuras y mensajes en las secciones siguientes hacen referencia a los identificadores de capítulo o marcador. Un identificador es una estructura opaca larga de 32 bits que identifica de forma única un capítulo o marcador. Normalmente, las aplicaciones cliente reciben valores de identificador a través de llamadas a métodos. sin embargo, hay varios valores bien conocidos que no es necesario obtener de un servidor, cuyo significado se especifica en la tabla siguiente:



| Value                         | Significado                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ null \_ HCHAPTER 0x00000000 | Identificador de capítulo del conjunto de filas no chaptered, que contiene todos los resultados de la consulta.    |
| DBBMK \_ primero 0x00000001       | Identificador de marcador de un marcador que identifica la primera fila del conjunto de filas. |
| DBBMK \_ Last 0x00000002        | Identificador de marcador de un marcador que identifica la última fila del conjunto de filas.  |



 

### <a name="221-structures"></a>2.2.1 estructuras

En esta sección se detallan las estructuras de datos que CISP define y usa.

Todos los enteros con y sin signo de 2, 4 y 8 bytes de las siguientes estructuras deben transferirse en orden de bytes Little-Endian.

En la tabla siguiente se resumen las estructuras de datos definidas en esta sección.



| Estructura                    | Descripción                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contiene el valor en el que se realiza una operación de coincidencia para una propiedad especificada en una estructura CPropertyRestriction. |
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
| CRangeRestriction            | Contiene una restricción de un intervalo de valores.                                                                           |
| CScopeRestriction            | Contiene una restricción de los archivos que se van a buscar.                                                                    |
| CSort                        | Identifica una columna que se va a ordenar.                                                                                           |
| CSynRestriction              | Contiene una palabra o sus sinónimos para una frase de consulta.                                                                    |
| CVectorRestriction           | Contiene una operación ponderada o en un nodo de árbol de comandos.                                                               |
| CWordRestriction             | Contiene una palabra para una frase de consulta.                                                                                    |
| CRestriction                 | Contiene un nodo de un árbol de comandos de consulta.                                                                               |
| CColumnSet                   | Indica el número de columnas que se van a devolver.                                                                             |
| CCategorizationSet           | Contiene información acerca de la agrupación de un conjunto de resultados de la consulta.                                                     |
| CCategorizationSpec          | Contiene una definición de categorías en las que se clasificarán los resultados de la consulta.                                      |
| CDbColId                     | Contiene una columna.                                                                                                     |
| CDbProp                      | Contiene una propiedad.                                                                                                   |
| CDbPropSet                   | Contiene un conjunto de propiedades.                                                                                          |
| CPidMapper                   | Contiene una matriz de identificadores de propiedad que especifican las propiedades que se van a devolver en un conjunto de filas.                                     |
| CRowSeekAt                   | Contiene el desplazamiento en el que se recuperan filas en un mensaje CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifica los marcadores de los que se van a recuperar filas de un mensaje CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contiene el número de filas que se van a omitir en un mensaje CPMGetRowsIn.                                                         |
| CRowsetProperties            | Contiene la información de configuración de una consulta.                                                                    |
| CSortSet                     | Contiene el criterio de ordenación de una consulta.                                                                                   |
| CTableColumn                 | Contiene una columna para el mensaje CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contiene un valor serializado.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

La estructura CBaseStorageVariant contiene el valor en el que se realiza una operación de coincidencia para una propiedad especificada en la estructura CPropertyRestriction.



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



 

**vType**: un indicador de tipo que indica el tipo de vValue. DEBE ser uno de los valores de VARENUM especificados en la tabla siguiente.



| Value                 | Significado                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ vacío (0x0000)    | vValue no está presente.                                                                                                               |
| VT \_ null (0x0001)     | vValue no está presente.                                                                                                               |
| VT \_ I1 (0x0010)       | Entero de 1 byte con signo.                                                                                                             |
| VT \_ UI1 (0x0011)      | Entero de 1 byte sin signo.                                                                                                           |
| VT \_ i2 (0x0002)       | Entero de 2 bytes con signo.                                                                                                             |
| VT \_ UI2 (0x0012)      | Entero de 2 bytes sin signo.                                                                                                           |
| VT \_ bool (0x000B)     | Valor booleano; entero de 2 bytes que contiene 0x0000 (FALSE) o 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Entero de 4 bytes con signo.                                                                                                             |
| VT \_ UI4 (0x0013)      | Entero de 4 bytes sin signo.                                                                                                           |
| VT \_ R4 (0x0004)       | Número de punto flotante de IEEE 32 bits, tal y como se define en \[ IEEE754 \] .                                                                     |
| VT \_ int (0x0016)      | Entero de 4 bytes con signo.                                                                                                             |
| VT \_ uint (0x0017)     | Entero de 4 bytes sin signo.                                                                                                           |
| \_Error VT (0x000a)    | Entero sin signo de 4 bytes que contiene un valor HRESULT, tal como se especifica en \[ MS-sys \] .                                                         |
| VT \_ i8 (0x0014)       | Entero de 8 bytes con signo.                                                                                                            |
| VT \_ UI8 (0x0015)      | Entero de 8 bytes sin signo.                                                                                                          |
| VT \_ R8 (0x0005)       | Número de punto flotante de IEEE 64 bits tal y como se define en \[ IEEE754 \] .                                                                      |
| VT \_ CY (0x0006)       | Entero del complemento de dos bytes de 8 bytes (escalado por 10.000).                                                                               |
| Fecha de VT \_ (0x0007)     | Número de punto flotante de 64 bits que representa el número de días transcurridos desde 00:00:00 el 31 de diciembre de 1899 (hora universal coordinada).     |
| VT \_ FILETIME (0x0040) | Entero de 64 bits que representa el número de intervalos de 100-nanosegundos 00:00:00 desde el 1 de enero de 1601 (hora universal coordinada). |
| VT \_ decimal (0x000E)  | Una estructura DECIMAL como se especifica en la sección 2.2.1.1.1.1.                                                                             |
| VT \_ CLSID (0x0048)    | Un valor binario de 16 bytes que contiene un GUID.                                                                                            |
| BLOB de VT \_ (0x0041)     | Un número entero sin signo de 4 bytes de bytes en el BLOB, seguido de muchos bytes de datos.                                           |
| VT \_ BSTR (0x0008)     | Un número entero sin signo de 4 bytes de bytes en la cadena, seguido de una cadena, tal y como se especifica a continuación en vValue.                       |
| VT \_ LPSTR (0x001E)    | Una cadena ANSI terminada en NULL.                                                                                                       |
| VT \_ LPWStr (0x001F)   | Una cadena Unicode de Unicode terminada en NULL \[ \] .                                                                                        |
| VT \_ (variante de 0x000C)  | CBaseStorageVariant. DEBE combinarse con un modificador de tipo de \_ matriz VT o un \_ Vector VT.                                               |



 

En la tabla siguiente se especifican los modificadores de tipo para vType. Los modificadores de tipo pueden ser binarios ORed con vType, para cambiar el significado de vValue para indicar que es uno de los dos tipos de matriz posibles.



| Value               | Significado                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ (vector) (0x1000) | Si el indicador de tipo se combina con VT \_ Vector mediante un operador OR, vValue es una matriz contada de valores del tipo indicado. Vea la sección 2.2.1.1.1.2 para obtener más información. <br/> Este modificador de tipo no debe combinarse con los tipos siguientes: VT \_ int, VT \_ uint, VT \_ decimal, \_ BLOB de VT, objeto de BLOB de VT \_ \_ .<br/>                                    |
| \_Matriz VT (0x2000)  | Si el indicador de tipo se combina con \_ una matriz de VT mediante un operador OR, el valor es un SafeArray (como se especifica en la sección 2.2.1.1.1.3) que contiene valores del tipo indicado. <br/> Este modificador de tipo no debe combinarse con los siguientes tipos: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPSTR, VT \_ LPWStr. <br/> |



 

**vData1**: cuando VTYPE es VT \_ decimal, el valor de este campo se especifica como el campo Scale en la sección 2.2.1.1.1.1. Para el resto de vTypes, el valor debe establecerse en 0x00.

**vData2**: cuando VTYPE es VT \_ decimal, el valor de este campo se especifica como el campo Sign en la sección 2.2.1.1.1.1. Para el resto de vTypes, el valor debe establecerse en 0x00.

**vValue**: el valor de la operación de coincidencia. La sintaxis debe ser la indicada en el campo vType.

En la tabla siguiente se resumen los tamaños del campo vValue, según el campo vType para tipos de datos de longitud fija. El tamaño está en bytes.



| vType                                                   | Tamaño |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ bool                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, error de VT \_   | 4    |
| VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ Date, VT \_ FILETIME | 8    |
| VT \_ decimal, VT \_ CLSID                                  | 16   |



 

Si vType se establece en VT \_ BLOB, VT \_ BSTR o VT \_ LPSTR, se especifica la estructura de vValue en el diagrama siguiente:



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



 

**cbSize**: entero de 32 bits sin signo, que indica el tamaño del campo blobData en bytes. Si vType se establece en VT \_ BSTR o VT \_ LPSTR, cbSize debe establecerse en 0x00000000 cuando la cadena representada sea una cadena vacía.

**blobData**: debe tener una longitud de cbSize en bytes.

En el caso de vType establecido en VT \_ BLOB, este campo es datos de blobs binarios opacos.

En el caso de vType establecido en VT \_ BSTR, este campo es un juego de caracteres en un juego de caracteres OEM seleccionado. El cliente y el servidor deben estar configurados para tener conjuntos de caracteres interoperables (fuera de banda del Protocolo). No es necesario terminar en NULL.

Para vType establecido en VT \_ LPSTR, este campo es una cadena de caracteres terminada en null en un juego de caracteres OEM seleccionado. El cliente y el servidor deben estar configurados para tener conjuntos de caracteres interoperables (fuera de banda del Protocolo).

Si vType se establece en VT \_ LPWStr, se especifica la estructura de vValue en el diagrama siguiente:



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

String (variable, opcional)



 

**ccLen**: entero de 32 bits sin signo, que indica el tamaño del campo de cadena en caracteres Unicode. DEBE establecerse en 0x00000000 para una cadena vacía.

**cadena**: cadena Unicode terminada en NULL.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 estructuras CBaseStorageVariant

Se usan las siguientes estructuras en la estructura CBaseStorageVariant.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL se usa para representar un valor numérico exacto con una precisión fija y una escala fija.

Cuando vType se establece en VT \_ decimal (0x0000E), los campos vData1 y vData2 de CBaseStorageVariant se deben interpretar de la siguiente manera:

**vData1**: número de dígitos a la derecha del separador decimal. DEBE estar en el intervalo comprendido entre 0 y 28.

**vData2**: el signo del valor numérico. Establézcalo en 0x00 si es positivo, 0x80 si es negativo.

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



 

**Hi32**: los 32 bits más altos del entero de 96 bits.

**Lo32**: los 32 bits más bajos del entero de 96 bits.

**Mid32**: el medio 32 bits del entero de 96 bits.

### <a name="221112-vt_vector"></a>Vector 2.2.1.1.1.2 VT \_

El \_ Vector VT se usa para pasar Matrices unidimensionales.



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



 

**vVectorElements**: entero de 32 bits sin signo, que indica el número de elementos del campo vVectorData.

**vVectorData**: una matriz de elementos que tienen un tipo indicado por vType con el bit de 0x1000 desactivado. El tamaño de un elemento de longitud fija individual se puede obtener a partir de la tabla de tipos de datos de longitud fija, como se especifica en la sección 2.2.1.1. La longitud de este campo, en bytes, se puede calcular multiplicando vVectorElements por el tamaño de cada elemento individual.

En el caso de los tipos de datos de longitud variable vVectorData contiene una secuencia de tipos simples de serialización consecutiva donde el tipo se indica mediante vType con el bit de 0x1000 desactivado. Esto incluye un caso especial indicado por vType VT \_ array \| VT \_ Variant (es decir, 0x100C).

Los elementos del campo vVectorData se deben separar entre 0 y 3 bytes de relleno, de modo que cada elemento comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si los bytes de relleno están presentes, el valor que contienen es arbitrario. El receptor debe omitir el contenido de los bytes de relleno.

En el caso de una vType establecida en VT \_ array \| VT \_ Variant, el tipo de los elementos de esta secuencia es CBaseStorageVariant.

### <a name="221113-safearray"></a>SAFEARRAY 2.2.1.1.1.3

SAFEARRAY se utiliza para pasar matrices multidimensionales. La estructura contiene información sobre el tamaño de la matriz, así como los datos de la matriz.



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



 

**cDims**: entero de 16 bits sin signo, que indica el número de dimensiones de la matriz multidimensional.

**fFeatures**: un campo de bits de 16 bits. Los valores representan características, definidas por aplicaciones de nivel superior y deben omitirse.

**cbElements**: entero de 32 bits sin signo que especifica el tamaño de cada elemento de la matriz.

**Rgsabound**: una matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4, por dimensión en SafeArray. En primer lugar, esta matriz tiene la dimensión situada más a la izquierda y la dimensión situada más a la derecha.

**vData**: un vector de elementos de serialización de un tipo determinado, indicado por el VType de CBaseStorageVariant que contiene, con el bit 0x2000 desactivado.

vData se calcula de forma similar a VT \_ Vector, como se especifica en la sección 2.2.1.1.1.2, con la diferencia de que el número de elementos no se almacena delante del vector. En su lugar, el número de elementos se calcula multiplicando el valor de cElements por todos los límites de matriz seguros que se proporcionan en el campo Rgsabound. Los elementos se almacenan en un vector en orden de dimensiones, iterando a partir de la dimensión situada más a la derecha.

El siguiente diagrama representa visualmente una matriz bidimensional de ejemplo. La primera dimensión tiene cElements igual a 4 (representada horizontalmente) y lLbound igual a 0, y la segunda dimensión tiene cElements igual a 2 (representada verticalmente) y lLbound igual a 0.



|            |            |            |            |
|------------|------------|------------|------------|
| 0x00000001 | 0x00000002 | 0x00000003 | 0x00000005 |
| 0x00000007 | 0x00000011 | 0x00000013 | 0x00000017 |



 

Con el diagrama anterior, vData contendrá la siguiente secuencia: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (recorrer en iteración la dimensión situada más a la derecha y, a continuación, incrementar la dimensión siguiente). El Rgsabound anterior (que registra cElements y LBound) sería: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

La estructura SAFEARRAYBOUND representa los límites de una dimensión de un SAFEARRAY o de un SAFEARRAY2. Su formato es:



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



 

**cElements**: entero de 32 bits sin signo, que especifica el número de elementos de la dimensión.

**lLbound**: entero de 32 bits sin signo, que especifica el límite inferior de la dimensión.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 se usa para pasar matrices multidimensionales en SERIALIZEDPROPERTYVALUE. La estructura contiene información sobre los límites y los datos.



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



 

**cDims**: entero de 32 bits sin signo, que indica el número de dimensiones de SAFEARRAY2.

**Rgsabound**: una matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4 por dimensión en SAFEARRAY2. En primer lugar, esta matriz tiene la dimensión situada más a la izquierda y la dimensión situada más a la derecha.

**vData**: un vector de elementos de serialización de un tipo determinado, indicado por el valor de DWTYPE del SERIALIZEDPROPERTYVALUE contenedor, con el bit 0x2000 desactivado. El formato de vData es el mismo que el especificado para el campo vData de SAFEARRAY en la sección 2.2.1.1.1.3.

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



 

**\_ guidPropSet**: el GUID del conjunto de propiedades al que pertenece la propiedad.

**ulKind**: entero de 32 bits sin signo. Uno de los siguientes valores, que indica el contenido de PrSpec.



| Value                                            | Significado                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWStr<br/> 0x00000000<br/> | El campo PrSpec especifica el número de caracteres no NULOs en el campo Nombre de propiedad. |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | El campo PrSpec especifica el identificador de propiedad (PROPID).                                     |



 

**PrSpec**: entero de 32 bits sin signo con un significado indicado por el campo ulKind.

**Nombre de propiedad**: si ulKind está establecido en PRSPEC \_ PROPID, este campo no debe estar presente. Si ulKind se establece en PRSPEC \_ LPWStr, este campo debe contener una matriz sin distinción entre mayúsculas y minúsculas de PRSPEC caracteres Unicode que no sean NULL y que contenga el nombre de la propiedad.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

La estructura CContentRestriction contiene una cadena que debe coincidir con una propiedad de la memoria caché de propiedades.



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



 

**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.2. Este campo indica la propiedad en la que se va a realizar una operación de coincidencia.

**Padding1**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**CC**: un entero de 32 bits sin signo, que especifica el número de caracteres en el \_ campo pwcsPhrase.

**\_ pwcsPhrase**: una cadena Unicode terminada en null que representa la palabra o frase que debe coincidir con la propiedad. Este campo no debe estar vacío. El campo CC contiene la longitud de la cadena.

**Padding2**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**LCID**: un entero de 32 bits sin signo, que indica la configuración regional de \_ pwcsPhrase, como se especifica en el \[ apéndice a de MS-GPSI \] .

**\_ ulGenerateMethod**: un entero de 32 bits sin signo, que especifica el método que se va a usar al generar formas de palabras alternativas



| Value                                                       | Significado                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GENERAR \_ método \_ exactamente<br/> 0x00000000<br/>    | Coincidencia exacta.                                                                                                                                                                                                                                                                                      |
| GENERAR \_ \_ Prefijo de método<br/> 0x00000001 <br/>  | Coincidencia de prefijo.                                                                                                                                                                                                                                                                                     |
| \_derivación de método de generación \_ <br/> 0x00000002<br/> | Coincide con las inflexiones de una palabra. Una inflexión de una palabra es una variante de la palabra raíz en la misma parte de la voz que se ha modificado según las reglas lingüísticas de un idioma determinado. Por ejemplo, las inflexiones del verbo "nadar" en inglés son "nadar", "nadar", "natación" y "Swam". |



 

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

CB

buf (variable)



 

**PROPID**: entero de 32 bits sin signo que representa el identificador de propiedad como se describe en la sección 1.8.1. Los valores conocidos son:



| Value      | Significado                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Representa un identificador de propiedad no válido y no se debe utilizar. |
| 0xFFFFFFFE | Representa un identificador de propiedad no válido y no se debe utilizar. |
| 0x00000000 | Representa cualquier identificador de propiedad.                             |



 

**CB**: entero de 32 bits sin signo que contiene la longitud de buf, en bytes.

**BUF**: secuencia de bytes que representa el valor de la propiedad.

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

\_relop

\_ID

\_prval (variable)

restrictionPresent

nextRestriction (variable)



 

**\_ relop**: entero de 32 bits que especifica la relación que se va a realizar en la propiedad. DEBE ser uno de los siguientes valores:



| Value                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Una comparación de menor que.                                                                                           |
| PRLE 0x00000001       | Comparación menor o igual que.                                                                               |
| PRGT 0x00000002       | Una comparación mayor que.                                                                                        |
| PRGE 0x00000003       | Comparación mayor o igual que.                                                                            |
| PREQ 0x00000004       | Una comparación de igualdad.                                                                                           |
| PRNE 0x00000005       | Comparación no igual.                                                                                           |
| PRRE 0x00000006       | Una comparación de expresiones regulares.                                                                                  |
| PRAllBits 0x00000007  | Una operación and bit a bit que devuelve el operando derecho.                                                                     |
| PRSomeBits 0x00000008 | Una operación bit a bit y que devuelve un valor distinto de cero.                                                                       |
| PRAll 0x00000100      | La operación se realiza en una columna de un conjunto de filas y solo es true si la operación es true para todas las filas. |
| PRAny 0x00000200      | La operación se realiza en una columna de un conjunto de filas y es true si la operación es true para cualquier fila.       |



 

**\_ PID**: un entero de 32 bits sin signo que representa el identificador de propiedad (consulte PROPID en la sección 2.2.1.4).

**\_ prval**: un CBaseStorageVariant que contiene el valor que se va a relacionar con la propiedad.

**restrictionPresent**: un valor de tipo byte que indica si el campo nextRestriction está presente. DEBE establecerse en 0x00 o 0x01. Si se establece en 0x01, restrictionPresent indica que el campo nextRestriction está presente. Si se establece en 0x00, restrictionPresent indica que el campo nextRestriction no está presente.

**nextRestriction**: una estructura CRestriction, como se especifica en la sección 2.2.1.16, que especifica una restricción adicional.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

La estructura CNatLanguageRestriction contiene una coincidencia de **consulta de lenguaje natural** para una propiedad.



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

\_relleno \_ CC (variable)

CC

\_pwcsPhrase (variable)

...

\_LCID de relleno \_ (variable)

Lcid



 

**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.3. Este campo indica la propiedad en la que se va a realizar la operación de coincidencia.

**\_ relleno \_ CC**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**CC**: entero de 32 bits sin signo. Número de caracteres del \_ campo pwcsPhrase.

**\_ pwcsPhrase**: una cadena Unicode terminada en null que representa la palabra o frase que debe coincidir con la propiedad. NO debe estar vacío. El campo CC contiene la longitud de la cadena.

**\_ \_ LCID de relleno**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**LCID**: entero de 32 bits sin signo que indica la configuración regional de \_ pwcsPhrase, tal y como se especifica en el \[ apéndice a de MS-GPSI \] .

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

La estructura CNodeRestriction contiene una matriz de nodos de **árbol de comandos** que especifican las restricciones de la consulta.



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

\_panode (variable)



 

**\_ cNode**: entero de 32 bits sin signo que especifica el número de estructuras CRestriction contenidas en el \_ campo panode.

**\_ panode**: una matriz de estructuras CRestriction. Las estructuras de la matriz se deben separar entre 0 y 3 bytes de relleno, de modo que cada estructura comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si los bytes de relleno están presentes, el valor que contienen es arbitrario. El receptor debe omitir el contenido de los bytes de relleno.

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

\_OCC

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ OCC**: entero de 32 bits sin signo que especifica el desplazamiento de la palabra en una cadena de consulta, en unidades de palabras. Una palabra, como se usa en esta especificación, es una unidad de idioma en cualquier configuración regional que lleve el significado.

**\_ cPrevNoiseWords**: entero de 32 bits sin signo que contiene el número de **palabras irrelevantes** que se producen entre esta palabra y la palabra anterior en la frase.

**\_ cNextNoiseWords**: entero de 32 bits sin signo que contiene el número de palabras irrelevantes que se producen entre esta palabra y la siguiente palabra de la frase.

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

\_relop

\_Propiedad (variable)

\_prval (variable)



 

**\_ relop**: entero de 32 bits sin signo que especifica la relación que se va a realizar en la propiedad. DEBE ser uno de los valores siguientes.



| Value                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Una comparación de menor que.                                                                                           |
| PRLE 0x00000001       | Comparación menor o igual que.                                                                               |
| PRGT 0x00000002       | Una comparación mayor que.                                                                                        |
| PRGE 0x00000003       | Comparación mayor o igual que.                                                                            |
| PREQ 0x00000004       | Una comparación de igualdad.                                                                                           |
| PRNE 0x00000005       | Comparación no igual.                                                                                           |
| PRRE 0x00000006       | Una comparación de expresiones regulares.                                                                                  |
| PRAllBits 0x00000007  | Una operación and bit a bit que devuelve el operando derecho.                                                                     |
| PRSomeBits 0x00000008 | Una operación bit a bit y que devuelve un valor distinto de cero.                                                                       |
| PRAll 0x00000100      | La operación se realiza en una columna de un conjunto de filas y solo es true si la operación es true para todas las filas. |
| PRAny 0x00000200      | La operación se realiza en una columna de un conjunto de filas y es true si la operación es true para cualquier fila.       |



 

**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.2, que indica la propiedad en la que se va a realizar una operación de coincidencia.

**\_ prval**: una estructura CBaseStorageVariant, como se especifica en la sección 2.2.1.1, que contiene el valor que se va a relacionar con la propiedad.

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



 

**\_ keyStart**: una estructura CKey, como se especifica en la sección 2.2.1.4, que contiene el principio del intervalo.

**\_ keyEnd**: estructura CKey que contiene el final del intervalo.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

La estructura CScopeRestriction contiene una restricción en los archivos que se van a buscar.



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

\_longitud

\_fRecursive

\_fVirtual



 

**CcLowerPath**: entero de 32 bits sin signo que contiene el número de caracteres Unicode en el \_ campo lowerPath.

**\_ lowerPath**: cadena Unicode terminada en null que representa la **ruta** de acceso en la que se debe restringir la consulta. El campo CcLowerPath contiene la longitud de la cadena.

**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**\_ length**: entero de 32 bits sin signo que contiene la longitud de \_ lowerPath, en caracteres Unicode. DEBE ser el mismo valor que CcLowerPath.

**\_ fRecursive**: entero de 32 bits sin signo. DEBE establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, el servidor examina de forma recursiva todos los subdirectorios de la ruta de acceso. Si se establece en 0x00000000, el servidor no examinará ningún subdirectorio.

**\_ fVirtual**: entero de 32 bits sin signo. DEBE establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, \_ lowerPath es una ruta de acceso virtual (el localizador uniforme de recursos (URL) asociado a un directorio físico en el sistema de archivos) para un sitio Web. Si se establece en 0x00000000, \_ lowerPath es una ruta de acceso del sistema de archivos.

### <a name="22112-csort"></a>2.2.1.12 CSort

La estructura CSort identifica una columna que se va a ordenar.



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

dwOrd

locale



 

**pidColumn**: entero de 32 bits sin signo. Número de la columna por la que se va a ordenar.

**DWORD**: entero de 32 bits sin signo. DEBE ser uno de los siguientes valores, especificando cómo ordenar en función de la columna.



| Value                        | Significado                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| CONSULTA \_ SORTASCEND 0x00000000 | Las filas se van a ordenar en orden ascendente en función de los valores de la columna especificada.  |
| QUERY \_ Descending 0x00000001    | Las filas se van a ordenar en orden descendente en función de los valores de la columna especificada. |



 

**locale**: un entero de 32 bits sin signo que indica la configuración regional, tal como se especifica en \[ \] el apéndice a de MS-GPSI, de la columna.

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



 

**Restriction**: una estructura COccRestriction que especifica la ubicación de la palabra.

**cKey**: entero de 32 bits sin signo que especifica el número de elementos de la \_ matriz de keyArray.

**\_ keyArray**: una matriz de estructuras CKey que especifica una palabra y sus sinónimos.

**\_ isRange**: si se establece en 0x01, las claves son prefijos que deben coincidir. Si se establece en 0x00, las claves son valores exactos que deben coincidir. \_isRange no debe establecerse en ningún otro valor.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

La estructura CVectorRestriction contiene una operación ponderada o en un nodo de árbol de comandos.



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

\_Pres (variable)

...

\_padding (variable)

\_ulRankMethod



 

**\_ Pres**: un árbol de comandos CNodeRestriction en el que se va a realizar una operación de clasificación.

**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**\_ ulRankMethod**: entero de 32 bits sin signo que especifica un algoritmo de clasificación. DEBE establecerse en uno de los valores siguientes.



| Value                            | Significado                                       |
|----------------------------------|-----------------------------------------------|
| Rango del VECTOR \_ \_ min 0x00000000     | Use el algoritmo mínimo \[ Salton \] .             |
| Rango de VECTOR \_ \_ máximo 0x00000001     | Use la sal máxima del algoritmo \[ \] .             |
| VECTOR de \_ clasificación \_ interior 0x00000002   | Usar el algoritmo de producto interior \[ salon \] .       |
| Índices de rango de VECTOR \_ \_ 0x00000003    | Usar el algoritmo de coeficiente de los dados \[ . salon \] .    |
| VECTOR \_ Rank \_ JACCARD 0x00000004 | Use el algoritmo de coeficiente Jaccard \[ Salton \] . |



 

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

\_Key (variable)

\_isRange



 

**Restriction**: una estructura COccRestriction que especifica la ubicación de la palabra.

**\_ key**: una estructura CKey que especifica una palabra.

**\_ isRange**: si se establece en 0x01, la clave es un prefijo que debe coincidir. Si se establece en 0x00, la clave es un valor exacto que debe coincidir. \_isRange no debe establecerse en ningún otro valor.

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



 

**\_ ulType**: entero de 32 bits sin signo que indica el tipo de restricción que se usa para el nodo de árbol de comandos. DEBE establecerse en uno de los valores siguientes.



| Value                    | Significado                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | El nodo representa una palabra irrelevante en una consulta de vector.                                         |
| RTAnd 0x00000001         | El nodo contiene un CNodeRestriction en el que se realiza una operación AND lógica que se va a realizar. |
| RTOr 0x00000002          | El nodo contiene un CNodeRestriction en el que se va a realizar una operación OR lógica.  |
| RTNot 0x00000003         | El nodo contiene un CRestriction en el que se va a realizar una operación NOT.             |
| RTContent 0x00000004     | El nodo contiene una CContentRestriction.                                                    |
| RTProperty 0x00000005    | El nodo contiene una CPropertyRestriction.                                                   |
| RTProximity 0x00000006   | El nodo contiene un CNodeRestriction sobre el que se va a realizar una clasificación de proximidad.     |
| RTVector 0x00000007      | El nodo contiene una CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | El nodo contiene una CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | El nodo contiene una CScopeRestriction.                                                      |
| PRAny 0xFFFFFFFA         | El nodo contiene una CInternalPropertyRestriction.                                           |
| RTRange 0xFFFFFFFC       | El nodo contiene una CRangeRestriction.                                                      |
| RTPhrase 0xFFFFFFFD      | El nodo contiene un CNodeRestriction sobre el que se va a realizar una coincidencia de frase.          |
| RTSynonym 0xFFFFFFFE     | El nodo contiene una CSynRestriction.                                                        |
| RTWord 0xFFFFFFFF        | El nodo contiene una CWordRestriction.                                                       |



 

**Weight**: entero de 32 bits sin signo que representa el peso del nodo. Weight indica la importancia del nodo en relación con otros nodos del árbol de comandos de consulta. Los valores de peso mayores son más importantes.

**Restriction**: el tipo de restricción para el nodo de árbol de comandos. La sintaxis debe ser la indicada por el \_ campo ulType.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

La estructura CColumnSet especifica los números de columna que se van a devolver. Esta estructura siempre se usa en referencia a una estructura CPidMapper específica (sección 2.2.1.23).



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

count

índices (variable)



 

**Count**: entero de 32 bits sin signo que especifica el número de elementos de la matriz de índices.

**Indexes**: matriz de enteros de 4 bytes sin signo que representan índices de base cero en la matriz aPropSpec de la estructura CPidMapper correspondiente.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

La estructura CCategorizationSet contiene información sobre la agrupación de un conjunto de resultados de la consulta.



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

count

categorías (variable)



 

**Count**: entero de 32 bits sin signo que contiene el número de elementos de la matriz de categorías.

**Categories**: matriz de estructuras CCategorizationSpec que especifican la agrupación de la consulta.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

La estructura CCategorizationSpec contiene una agrupación para un conjunto de resultados de la consulta.



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



 

**\_ csColumns**: una estructura CColumnSet que indica las columnas por las que se va a agrupar la consulta.

**\_ ulCategType**: entero de 32 bits sin signo. DEBE establecerse en 0x00000000.

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



 

**eKind**: debe establecerse en uno de los valores siguientes que indique el contenido de GUID y vValue.



| Value                            | Significado                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| DBKIND \_ \_ nombre GUID 0x00000000    | vString contiene un nombre de propiedad.                                                                               |
| GUID de DBKIND \_ \_ PROPID 0x00000001  | ulId contiene un entero de 4 bytes que indica el identificador de la propiedad.                                                      |
| DBKIND \_ PGUID \_ nombre 0x00000003   | vString contiene un nombre de propiedad. Este valor se debe tratar igual que el nombre del GUID de DBKIND \_ \_ .                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId contiene un entero de 4 bytes que indica el identificador de la propiedad. Este valor debe ser el mismo que el \_ GUID de DBKIND \_ . |



 

**GUID**: el GUID de la propiedad.

**ulId**: si EKIND es DBKIND \_ GUID \_ PROPID o DBKIND \_ PGUID \_ PROPID, este campo contiene un entero sin signo que especifica el identificador de la propiedad. Si eKind es DBKIND \_ \_ nombre GUID o DBKIND \_ PGUID \_ nombre, este campo contiene un entero sin signo que especifica el número de caracteres Unicode contenidos en el campo vString.

**vString**: cadena Unicode terminada en null que representa el nombre de la propiedad. Se debe omitir a menos que el campo eKind se establezca en DBKIND \_ GUID \_ Name o DBKIND \_ PGUID \_ Name.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

La estructura CDbProp contiene una propiedad.



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

colid (variable)

vValue (variable)



 

**DBPROPID**: entero de 32 bits sin signo, que indica el identificador de la propiedad.

**DBPROPOPTIONS** : debe establecerse en 0x00000000.

**DBPROPSTATUS**: debe establecerse en 0x00000000.

**colid**: una estructura CDbColId, como se especifica en la sección 2.2.1.20, que indica la columna a la que se aplica la propiedad.

**vValue**: un CBaseStorageVariant que contiene el valor de propiedad.

### <a name="221211-properties"></a>propiedades de 2.2.1.21.1

En esta sección se detallan las propiedades que usa CISP. Estas propiedades se agrupan en tres conjuntos de propiedades: ident 2.2.1.21.1 ified en el campo guidPropertySet de la estructura CDbPropSet (sección 2.2.1.22).

En la tabla siguiente se enumeran las propiedades que forman parte \_ del \_ conjunto de propiedades ext de DBPROPSET FSCIFRMWRK.



| Value                                  | Significado                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre del catálogo de CI de DBPROP \_ \_ \_ 0x00000002   | Especifica el nombre del catálogo o los catálogos que se van a consultar. El valor debe ser un VT \_ LPWStr o un VT \_ Vector \| VT \_ LPWStr                                   |
| DBPROP \_ CI \_ incluye \_ ámbitos 0x00000003 | Especifica una o más rutas de acceso que se van a incluir en la consulta. El valor debe ser un VT \_ LPWStr o un \_ Vector \| VT \_ LPWStr LPWStr.                                 |
| DBPROP \_ marcas de ámbito de CI \_ \_ 0x00000004    | Especifica cómo se tratarán las rutas de acceso especificadas por la \_ propiedad ámbitos de inclusión de DBPROP CI \_ \_ . El valor debe ser VT \_ I4 o VT \_ Vector \| VT \_ I4. |
| DBPROP \_ tipo de consulta de CI \_ \_ 0x00000007     | Especifica el tipo de consulta. CDbColId debe establecerse en DB \_ NULLID.                                                                               |



 

En la tabla siguiente se enumeran las marcas de la propiedad de marcas de ámbito de CI de DBPROP \_ \_ \_ :



| Value                     | Significado                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BÚSQUEDA \_ profunda de consulta 0x01          | Si se establece, indica que los archivos del directorio de ámbito y todos los subdirectorios se incluyen en los resultados. Si está desactivada, solo los archivos del directorio de ámbito se incluyen en los resultados. NO se debe combinar con Deep de consulta \_ . |
| \_Ruta de acceso virtual de consulta \_ 0x02 | Si se establece, indica que el ámbito es una ruta de acceso virtual. Si está desactivada, indica que el ámbito es un directorio físico.                                                                                                         |



 

En la tabla siguiente se enumeran los tipos de consulta para la \_ \_ propiedad tipo de consulta DBPROP CI \_ :



| Value                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Una consulta normal.                                                                                                   |
| CiVirtualRoots 0x00000001 | La consulta solicita una lista de las raíces virtuales del catálogo. Este valor requiere privilegios administrativos. |
| CiProperties 0x00000003   | La consulta solicita una lista de todas las propiedades admitidas por el servicio de indización.                            |
| CiAdminOp 0x00000004      | La consulta es una operación administrativa. Este valor requiere privilegios administrativos.                           |



 

En la tabla siguiente se enumeran las propiedades que forman parte del \_ conjunto de propiedades DBPROPSET QUERYEXT.



| Value                                      | Significado                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Especifica cómo el servicio de indización controla las consultas lentas. El valor debe ser un VT \_ bool. Si es TRUE, se permite que el servidor no pueda realizar estas consultas.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indica si el servicio de indización va a realizar el recorte de los resultados. Si es TRUE, el servidor debe considerar la posibilidad de realizar un recorte de los resultados de forma que se optimice el tiempo de respuesta para el cliente. El valor debe ser un VT \_ bool.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indica si el cliente admite los \_ tipos de datos de vector VT. Si es TRUE, el cliente admite el \_ Vector VT; si es false, el servidor debe convertir los \_ tipos de datos de vector VT en \_ tipos de datos de matriz VT.  El valor debe ser un VT \_ bool. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indica las coincidencias de filas que se van a devolver. Si es TRUE, el servidor devuelve el primer conjunto de filas coincidentes. Si es FALSE, se deben devolver las filas coincidentes más adecuadas. El valor debe ser un VT \_ bool.                                             |



 

En la tabla siguiente se enumeran las propiedades que forman parte \_ del \_ conjunto de propiedades ext de DBPROPSET CIFRMWRKCORE.



| Valor/DBPROPID                 | Significado                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| \_Máquina DBPROP 0x00000002       | Especifica los nombres de los equipos en los que se va a procesar una consulta. El valor debe ser VT \_ BSTR o VT \_ matriz \| VT \_ . |
| \_CLSID de cliente DBPROP \_ 0x00000003 | Especifica una constante de conexión para el servicio de indización. El valor debe ser un CLSID de VT \_ que contenga 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

La estructura CDbPropSet contiene un conjunto de propiedades. Tenga en cuenta que el primer campo tiene un tamaño fijo, pero es posible que no esté alineado en un desplazamiento que sea un múltiplo de 4 bytes desde el inicio del mensaje que contiene esta estructura. Sin embargo, el campo cProperties se alinea como tal y, por lo tanto, el formato se muestra a continuación:



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



 

**guidPropertySet**: un GUID que identifica el conjunto de propiedades. DEBE establecerse en el formato binario correspondiente a uno de los siguientes valores (se muestra en formato de representación de cadena), identificando el conjunto de propiedades de las propiedades contenidas en el campo aProps.



| Valor/GUID                                                                              | Nombre                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ ext<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Conjunto de propiedades del marco de índice de contenido del sistema de archivos |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Conjunto de propiedades de extensión de consulta                     |
| DBPROPSET \_ CIFRMWRKCORE \_ ext<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Conjunto de propiedades Core de content index Framework        |



 

**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes. La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura. Si este campo está presente (es decir, la longitud es distinto de cero), el valor que contiene es arbitrario. El receptor debe omitir el contenido de este campo.

**cProperties**: entero de 32 bits sin signo que contiene el número de elementos de la matriz de aProps.

**aProps**: una matriz de estructuras CDbProp, como se especifica en la sección 0, que contiene propiedades. Las estructuras de la matriz se deben separar entre 0 y 3 bytes de relleno, de modo que cada estructura comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz. Si los bytes de relleno están presentes, el valor que contienen es arbitrario. El receptor debe omitir el contenido de los bytes de relleno.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

La estructura CPidMapper contiene una matriz de identificadores de propiedad que especifican las propiedades que se van a devolver en un conjunto de filas.



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

count

aPropSpec

... variable



 

**Count**: entero de 32 bits sin signo que contiene el número de elementos de la matriz aPropSpec.

**aPropSpec**: matriz de estructuras CFullPropSpec que indica las propiedades que se van a devolver. Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

La estructura CRowSeekAt contiene el desplazamiento en el que se recuperan las filas de un mensaje CPMGetRowsIn.



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



 

**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.

**\_ cskip**: entero de 32 bits sin signo que contiene el número de filas que se van a omitir en el conjunto de filas.

**\_ bmkOffset**: un valor de 32 bits que representa el identificador del **marcador** que indica la posición inicial desde la que se omitirá el número de filas especificado en \_ cskip antes de comenzar la recuperación.

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



 

**CiTblChapt**: entero de 32 bits sin signo que indica el capítulo del conjunto de filas del que se van a recuperar filas.

**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.

**\_ ulNumerator**: entero de 32 bits sin signo que representa el numerador de la proporción de filas del capítulo en la que se va a comenzar la recuperación.

**\_ ulDenominator**: entero de 32 bits sin signo que representa el denominador de la proporción de filas del capítulo en la que se va a comenzar la recuperación. DEBE ser mayor que cero.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

La estructura CRowSeekByBookmark identifica los marcadores desde los que se van a empezar a recuperar filas para un mensaje CPMGetRowsIn.



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



 

**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.

**\_ cBookmarks**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz de aBookmarks.

**\_ maxRet**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz de ascRet.

**\_ cValidRet**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz ascRet que son válidos. Los elementos válidos se han definido en la matriz, mientras que los elementos no válidos no están definidos.

**\_ aBookmarks**: una matriz de identificadores de marcador (cada uno representado por 4 bytes), tal y como se obtiene de un mensaje CPMGetRowsOut.

**\_ ascRet**: una matriz de Valores HRESULT. Cuando CRowSeekByBookMark se envía como parte de la solicitud CPMGetRowsIn, el número de entradas de la matriz debe ser igual a \_ cBookMarks. Cuando lo envía el cliente, los valores deben establecerse en cero y el servidor debe omitir el contenido de la matriz. Cuando lo envía el servidor (como parte del mensaje CPMGetRowsOut), los valores de la matriz indican el estado del resultado para cada recuperación de fila.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

La estructura CRowSeekNext contiene el número de filas que se van a omitir en un mensaje CPMGetRowsIn.



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



 

**CiTblChapt**: entero de 32 bits sin signo que especifica el capítulo del conjunto de filas del que se van a recuperar filas.

**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.

**\_ cskip**: entero de 32 bits sin signo que representa el número de filas que se van a omitir en el conjunto de filas.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

La estructura CRowsetProperties contiene información de configuración de una consulta.



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



 

**\_ uBooleanOptions**: los 3 bits menos significativos de este campo deben contener uno de los tres valores siguientes:



| Value                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | El cursor solo se puede transferir hacia delante.                              |
| eLocatable 0x00000003  | El cursor se puede mover a cualquier posición.                            |
| eScrollable 0x00000007 | El cursor se puede mover a cualquier posición y captura en cualquier dirección. |



 

Los bits restantes pueden estar claros o establecerse en cualquier combinación de los siguientes valores lógicamente o juntos:



| Value                     | Significado                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | El cliente no esperará a que se complete la ejecución.                                                          |
| eFirstRows 0x00000080     | Devuelve las primeras filas encontradas, no las mejores coincidencias.                                                    |
| eHoldRows 0x00000200      | El servidor no debe descartar las filas hasta que el cliente haya terminado de realizar una consulta.                                     |
| eChaptered 0x00000800     | El conjunto de filas admite capítulos.                                                                               |
| eUseCI 0x00001000         | Solo responde a la consulta del índice, no del sistema de archivos.                                                  |
| eDeferTrimming 0x00002000 | El servicio de Index Server es la posibilidad de optimizar el tiempo de respuesta al cliente al realizar la eliminación de los resultados. |



 

**\_ ulMaxOpenRows**: entero de 32 bits sin signo. Debe establecerse en 0x00000000. No se utiliza y se debe omitir.

**\_ ulMemoryUsage**: entero de 32 bits sin signo. Debe establecerse en 0x00000000. No se utiliza y se debe omitir.

**\_ cMaxResults**: entero de 32 bits sin signo que especifica el número máximo de filas que se van a devolver para la consulta.

**\_ cCmdTimeout**: un entero de 32 bits sin signo, que especifica el número de segundos durante los que se agotará el tiempo de espera de una consulta y se terminará automáticamente, contando desde el momento en que se inicia la ejecución de la consulta en el servidor. Un valor de 0x00000000 significa que no se agotará el tiempo de espera de la consulta.

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



 

**vType**: un indicador de tipo que indica el tipo de vValue. DEBE ser uno de los valores de VARENUM especificados en la sección 2.2.1.1.

**reserved1**: no se usa. El valor se puede establecer en cualquier valor arbitrario y debe omitirse en la recepción.

**reserved2**: no se usa. El valor se puede establecer en cualquier valor arbitrario y debe omitirse en la recepción.

**Offset**: desplazamiento de datos de longitud variable (por ejemplo, una cadena).  DEBE ser un valor de 32 bits (longitud de 4 bytes) si se usan desplazamientos de 32 bits (según las reglas de la sección 2.2.3.16) o un valor de 64 bytes (8 bytes de longitud) si se usan desplazamientos de 64 bits.

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



 

**Count**: entero de 32 bits sin signo que especifica el número de elementos de sortArray.

**sortArray**: una matriz de estructuras CSort que describe el orden en el que se ordenan los resultados de la consulta. Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.

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

... variable

vType

ValueUsed

\_padding1 (opcional)

ValueOffset (opcional)

Valuen (opcional)

StatusUsed

\_padding2 (opcional)

StatusOffset (opcional)

LengthUsed

\_padding3 (opcional)

LengthOffset (opcional)



 

**PropSpec**: una estructura CFullPropSpec tal como se especifica en la sección 2.2.1.3.

**vType**: especifica el tipo de valor de datos contenido en la columna. Vea el campo vType de la sección 2.2.1.1 para obtener la lista de valores de este campo.

**ValueUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00. Si se establece en 0x01, la columna se transfiere dentro de la fila de tamaño fijo. Si se establece en 0x00, el valor de la columna se transfiere en la sección de longitud variable al final del búfer.

**\_ padding1**: un campo de un byte que se debe insertar antes de ValueOffset si, sin él, ValueOffset no comenzará en un desplazamiento uniforme desde el principio del mensaje. El valor de este byte es arbitrario y se debe omitir. Si ValueUsed se establece en 0x00, este campo no debe estar presente.

**ValueOffset**: entero de 2 bytes sin signo que especifica el desplazamiento del valor de la columna en la fila. Si ValueUsed se establece en 0x00, este campo no debe estar presente.

Sizeof **: entero** de 2 bytes sin signo que especifica el tamaño del valor de la columna en bytes. Si ValueUsed se establece en 0x00, este campo no debe estar presente.

**StatusUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00. Si se establece en 0x01, el estado de la columna se transfiere dentro de la fila. Si 0x00, el estado de la columna no se transfiere dentro de la fila.

**\_ padding2**: un campo de un byte que se debe insertar antes de StatusOffset si, sin él, el campo StatusOffset no comenzará en un desplazamiento uniforme desde el principio del mensaje. El valor de este byte es arbitrario y se debe omitir. Si StatusUsed se establece en 0x00, este campo no debe estar presente.

**StatusOffset**: entero de 2 bytes sin signo que especifica el desplazamiento del estado de la columna en la fila. Si StatusUsed se establece en 0x00, este campo no debe estar presente.

**LengthUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00. Si se establece en 0x01, la longitud de la columna se transfiere dentro de la fila. Si 0x00, no se debe transferir la longitud de la columna dentro de la fila.

**\_ padding3**: un campo de un byte que se debe insertar antes de LengthOffset si, sin él, LengthOffset no comenzará en un desplazamiento uniforme desde el principio de un mensaje. El valor de este byte es arbitrario y se debe omitir. Si LengthUsed se establece en 0x00, este campo no debe estar presente.

**LengthOffset**: entero de 2 bytes sin signo que especifica el desplazamiento de la longitud de la columna en la fila. Si LengthUsed se establece en 0x00, este campo no debe estar presente.

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

RGB (variable)



 

**dwType**: uno de los tipos Variant, definido en la sección 2.2.1.1, que se puede combinar con modificadores de tipo variante. En todos los tipos de variante, excepto los \_ que se combinan con la matriz de VT, SERIALIZEDPROPERTYVALUE tiene el mismo diseño que CBaseStorageVariant, como se especifica en la sección 2.2.1.1. Si el tipo Variant se combina con el \_ modificador de tipo de matriz VT, se usa SAFEARRAY2, especificado en la sección 2.2.1.2.1.1, en lugar de SAFEARRAY en el campo vValue de CBaseStorageVariant.

**RGB**: valor serializado. Vea los detalles de la serialización de vValue en 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 encabezados de mensaje

Todos los mensajes del protocolo del servicio de indización de contenido tienen un encabezado de 16 bytes.

A continuación se muestra un diagrama que muestra el formato del encabezado de mensaje del protocolo del servicio de indización de contenido.



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

\_mensaje

\_estatus

\_ulChecksum

\_ulReserved2



 

\_**MSG**: un entero de 32 bits que identifica el tipo de mensaje que sigue al encabezado. En la tabla siguiente se enumeran los mensajes de protocolo del servicio de indización de contenido y los valores enteros especificados para cada mensaje. Como se muestra en la tabla, algunos valores identifican dos mensajes en la tabla. En esas instancias, el mensaje que sigue al encabezado puede identificarse por la dirección del flujo de mensajes. Si la dirección es cliente a servidor, se indica el mensaje con "in" anexado al nombre del mensaje. Si la dirección es servidor a cliente, se indica el mensaje con la marca "out" anexada al nombre del mensaje.



| Value      | Significado                                                     |
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



 

\_**status**: HRESULT \[ MS-sys \] , que indica el estado de la operación solicitada.

\* *

*Comportamiento de Windows: el cliente siempre establece el \_ campo de estado en 0x00000000.*

**\_ ulChecksum**: el \_ ulChecksum debe calcularse como se especifica en la sección 3.2.4 para los siguientes mensajes:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Para todos los demás mensajes, \_ ULCHECKSUM debe establecerse en 0x00000000. Un cliente debe omitir el \_ campo ulChecksum.

**\_ ulReserved2**: debe establecerse en 0 y el receptor lo omitirá.

### <a name="223-messages"></a>2.2.3 mensajes

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

El mensaje CPMCiStateInOut contiene información sobre el estado del servicio de indización. El formato del mensaje CPMCiStateInOut que sigue al encabezado es:



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



 

**cbStruct**: entero de 32 bits sin signo. Tamaño en bytes de este mensaje (sin incluir el encabezado común). DEBE establecerse en 0x0000003C.

**cWordList**: entero de 32 bits sin signo que indica el recuento de los índices iniciales creados para documentos indexados recientemente.

**cPersistentIndex**: entero de 32 bits sin signo que indica el recuento de índices persistentes.

**cQueries**: entero de 32 bits sin signo que indica un número de consultas que se ejecutan activamente.

**cDocuments**: entero de 32 bits sin signo que indica el número total de documentos que están en espera de ser indexados.

**cFreshTest**: entero de 32 bits sin signo que indica el número de documentos únicos con información en índices que no están totalmente optimizados para el rendimiento.

**dwMergeProgress**: entero de 32 bits sin signo que especifica el porcentaje de finalización de la optimización completa actual de los índices, si la optimización está en curso actualmente. DEBE ser menor o igual que 100.

**inmobiliaria**: el estado de la indización de contenido dado por una o varias de las constantes de estado de CI \_ \_ \* , definidas en la tabla siguiente.



| Value                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Combinación de instantáneas de estado de CI \_ \_ 0x00000001           | El servicio de indización está en proceso de optimizar algunos de los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ \_ Fusión mediante combinación maestra de estado de CI           | El servicio de indización está en proceso de optimización completa de todos los índices.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Examen de contenido de estado de CI \_ \_ \_ \_ requerido 0x00000004 | Algunos documentos del índice han cambiado y el servicio de indexación debe determinar cuáles se han agregado, cambiado o eliminado.                                                                                                                                                                                                                                                                                                                                                              |
| Recocido de estado de CI \_ \_ \_ Merge 0x00000008        | El servicio de indización está en proceso de optimizar los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas. Este proceso es más completo que el identificado por el valor de la \_ combinación de instantáneas de estado de CI \_ \_ , pero no es tan completo como lo especifica el valor de combinación del maestro de estado de CI \_ \_ \_ . Estas optimizaciones son específicas de la implementación, ya que dependen de la forma en que se almacenan internamente los datos. las optimizaciones no afectan al Protocolo de ningún modo que no sea el tiempo de respuesta. |
| Análisis de estado de CI \_ \_ 0x00000010                | El servicio de indización está examinando un directorio o un conjunto de directorios para ver si se ha agregado, eliminado o actualizado algún archivo desde la última vez que se indizó el directorio.                                                                                                                                                                                                                                                                                                                 |
| Recuperación de estado de CI \_ \_ 0x00000020              | El servicio se está iniciando desde el último estado guardado y está en proceso de recuperación.                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_Memoria insuficiente de estado de CI \_ \_ 0x00000080             | La mayor parte de la memoria virtual del servidor está en uso.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_ \_ Alta e/s de estado de CI \_ 0x00000100                | El nivel de actividad de entrada/salida (e/s) en el servidor es relativamente alto.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Combinación del maestro de estado de CI en \_ \_ \_ \_ pausa 0x00000200   | El proceso de optimización completa de todos los índices en curso se ha puesto en pausa. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                                  |
| Estado de CI \_ \_ \_ solo lectura 0x00000400              | La parte del servicio de indexación que recoge nuevos documentos para el índice se ha puesto en pausa. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                               |
| Energía de la batería de estado de CI \_ \_ \_ 0x00000800          | La parte del servicio de indexación que recoge nuevos documentos para el índice se ha pausado para conservar la duración de la batería, pero sigue respondiendo a las consultas. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                 |
| \_ \_ 0x00001000 activo de usuario de estado de CI \_            | La parte del servicio de indización que recoge nuevos documentos para el índice se ha puesto en pausa debido a la alta actividad por parte del usuario (teclado o del mouse) pero sigue respondiendo a las consultas. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                         |
| Estado de CI \_ \_ iniciando 0x00002000                | El servicio está iniciándose. Se pueden ejecutar consultas, pero aún no se ha habilitado el examen y la notificación. Esto se proporciona solo con fines informativos y no afecta a CISP.                                                                                                                                                                                                                                                                                                                   |
| Estado de CI \_ \_ leyendo \_ USN 0x00004000           | El servicio no ha leído el registro mantenido por el sistema de archivos para realizar un seguimiento de los cambios en los archivos o directorios de un volumen, por lo que es posible que el índice no esté actualizado.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments**: entero de 32 bits sin signo que indica el número de documentos indizados desde que se inició la indización de contenido.

**cTotalDocuments**: entero de 32 bits sin signo que indica el número total de documentos en el sistema.

**cPendingScans**: entero de 32 bits sin signo que indica el número de operaciones pendientes de indización de alto nivel. El significado de este valor es específico del proveedor, pero se espera que los números mayores indiquen que se mantiene más indexación.

*Comportamiento de Windows*: este valor suele ser cero, excepto inmediatamente después de que se haya iniciado la indexación o después de que se desborde una cola de notificaciones.

**dwIndexSize**: entero de 32 bits sin signo que indica el tamaño, en megabytes, del índice (excluida la memoria caché de propiedades).

**cUniqueKeys**: entero de 32 bits sin signo que indica el número aproximado de claves únicas en el catálogo.

**cSecQDocuments**: entero de 32 bits sin signo que indica el número de documentos que el servicio de indización volverá a intentar indizar debido a un error durante el intento de indexación inicial.

**dwPropCacheSize**: entero de 32 bits sin signo que indica el tamaño, en megabytes, de la memoria caché de propiedades.

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



 

el valor de **\_ este: debe** establecerse en 0x00000001.

**\_ dwNewState**: debe establecerse en uno de los siguientes valores, que indica el nuevo estado del catálogo.



| Value                         | Significado                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ detuvo 0x00000001     | El catálogo se ha detenido. Este estado significa que no se va a indizar ningún archivo nuevo y no se procesará ninguna consulta de búsqueda.                                                     |
| CICAT \_ ReadOnly 0x00000002    | El catálogo es de solo lectura. No se va a indizar ningún archivo nuevo.                                                                                                               |
| CICAT \_ grabable 0x00000004    | El catálogo es grabable. Los nuevos archivos se pueden indexar y las consultas de búsqueda se procesarán.                                                                              |
| CICAT \_ no \_ query 0x00000008   | El catálogo no está disponible para realizar consultas.                                                                                                                              |
| CICAT \_ Get \_ State 0x00000010  | No se puede cambiar el estado del catálogo, solo se recupera.                                                                                                          |
| CICAT \_ todo \_ abierto 0x00000020 | Una comprobación para ver si se han iniciado todos los catálogos. En ese caso, el \_ campo dwOldState enviado en la respuesta CPMSetCatStateOut a este mensaje se indicará como distinto de cero. |



 

**\_ CatName**: el nombre del catálogo cuyo estado se va a modificar. El nombre debe ser una cadena Unicode terminada en NULL. Este campo se debe omitir si \_ dwNewState está establecido en CiCAT \_ todos \_ abiertos.

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



 

**\_ dwOldState**: uno de los siguientes valores, que indica el estado anterior del catálogo.



| Value                       | Significado                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ detuvo 0x00000001   | El catálogo se ha detenido.                    |
| CICAT \_ ReadOnly 0x00000002  | El catálogo es de solo lectura.                  |
| CICAT \_ grabable 0x00000004  | El catálogo es grabable.                   |
| CICAT \_ no \_ query 0x00000008 | El catálogo no está disponible para realizar consultas. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

El mensaje CPMUpdateDocumentsIn dirige el servidor para indizar la ruta de acceso especificada.

El servidor responderá con el encabezado del mensaje del mensaje CPMUpdateDocumentsOut, con los resultados de la solicitud contenidos en el \_ campo Estado del encabezado del mensaje.

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

\_marca (opcional)

\_fRootPath (opcional)

RootPath (variable, opcional)



 

**\_ marca**: el tipo de actualización que se va a realizar. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje. Este campo debe establecerse en uno de los siguientes valores:



| Value                  | Significado                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | Se realiza una actualización incremental. |
| UPD \_ completo 0x00000001   | Se debe realizar una actualización completa.         |
| UPD \_ init 0x00000002   | Se debe realizar una nueva inicialización.  |



 

**\_ fRootPath**: un valor booleano que indica si el campo RootPath especifica una ruta de acceso en la que se va a realizar la actualización. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje. Este campo debe establecerse en 0x00000001 o 0x00000000. Si se establece en 0x00000001, se incluye en RootPath una ruta de acceso en la que se va a realizar la actualización. Si se establece en 0x00000000, la actualización se realizará en todas las rutas de acceso indizadas.

**RootPath**: nombre de la ruta de acceso que se va a actualizar. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje. El nombre debe ser una cadena Unicode terminada en NULL. Este campo se debe omitir si \_ fRootPath está establecido en 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

El mensaje CPMForceMergeIn solicita a un servidor que realice el mantenimiento necesario para mejorar el rendimiento de las consultas. El servidor responderá con el encabezado del mensaje del mensaje CPMForceMergeIn, con los resultados de la solicitud contenidos en el \_ campo Estado.

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

\_bajo (opcional)



 

**\_ enescribir: este** campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje. Cuando este campo está presente, debe establecerse en 0x00000001.

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

\_acolcha

...

...

MachineName

... variable

UserName

... variable

\_paddingcPropSets (opcional, variable)

cPropSets

PropertySet1 (variable)

PropertySet2 (variable)

\_paddingExtPropset (opcional, variable)

cExtPropSet

aPropertySets (variable)



 

**\_ iClientVersion**: entero de 32 bits que indica si el servidor debe validar el valor de suma de comprobación especificado en el \_ campo ulChecksum de los encabezados de mensaje para los mensajes enviados por el cliente. Si el \_ campo iClientVersion está establecido en 0x00000008 o superior, el servidor debe validar el \_ valor del campo ulChecksum para los siguientes mensajes:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Para obtener más información sobre cómo el servidor valida el valor especificado por el cliente en el campo ulChecksum para los mensajes enumerados anteriormente, consulte la sección 3.2.5.

Si el valor es mayor que 0x00000008, se supone que el cliente es capaz de controlar desplazamientos de 64 bits en los mensajes CPMGetRowsOut. Vea la sección 2.2.3.16 para obtener más información.

*Comportamiento de Windows: en los clientes de Windows, iClientVersion se establece de la manera siguiente*:



| Value      | Significado                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | El sistema operativo de cliente es Windows 2000.                                           |
| 0x00000008 | El sistema operativo de cliente es de 32 de Windows XP o de 32 bits de Windows Server 2003. |
| 0x00010008 | El sistema operativo de cliente es de 64 de Windows XP o de 64 bits de Windows Server 2003. |



 

\_**fClientIsRemote**: un valor booleano que indica si el cliente se está ejecutando en un equipo diferente que el servidor. DEBE establecerse en 0x00000001.

\_**cbBlob1**: entero de 32 bits sin signo que indica el tamaño en bytes de los campos CPropSet, PropertySet1 y PropertySet2, combinados.

\_**cbBlob2**: entero de 32 bits sin signo que indica el tamaño en bytes de los campos CExPropSet y aPropertySet, combinados.

\_**padding**: 12 bytes de relleno que pueden contener valores arbitrarios y deben omitirse.

**MachineName**: el nombre de equipo del cliente. La cadena de nombre debe ser una matriz terminada en NULL de menos de 512 caracteres Unicode, incluido el terminador NULL.

**Username**: una cadena que representa el nombre de usuario de la persona que ejecuta la aplicación que invocó este protocolo. La cadena de nombre debe ser una matriz terminada en NULL de menos de 512 caracteres Unicode cuando se concatena con MachineName.

**\_ paddingcPropSets**: este campo debe tener una longitud de 0 a 7 bytes. El número de bytes debe ser el número necesario para que el desplazamiento de bytes del campo cPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8. El valor de los bytes puede ser cualquier valor arbitrario y el receptor debe pasarlo por alto.

**cPropSets**: entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que siguen a este campo. Este valor debe establecerse en 0x0000002.

**PropertySet1**: una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ FSCIFRMWRK \_ EXT (consulte la sección 2.2.1.22).

**PropertySet2**: una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ CIFRMWRKCORE \_ EXT (consulte la sección 2.2.1.22).

\_**PaddingExtPropset**: este campo debe tener una longitud de 0 a 7 bytes. El número de bytes debe ser el número necesario para que el desplazamiento de bytes del campo cExtPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8. El valor de los bytes puede ser cualquier valor arbitrario y el receptor debe pasarlo por alto.

**cExtPropSet**: entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que siguen a este campo.

**aPropertySets**: una matriz de estructuras CDbPropSet que especifica otras propiedades. El número de elementos de esta matriz debe ser igual a cExtPropSet.

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

\_reservado (variable)



 

**\_ serverVersion**:

Entero de 32 bits, que indica si el servidor puede admitir desplazamientos de 64 bits *.* Vea la sección 2.2.3.16 para obtener más información.



| Value      | Significado                                 |
|------------|-----------------------------------------|
| 0x00000007 | El servidor solo puede enviar desplazamientos de 32 bits. |
| 0x00010007 | El servidor puede enviar desplazamientos de 32 o 64 bits.   |



 

**\_ reservado**: reservado. El servidor puede enviar un número arbitrario de valores arbitrarios y el cliente debe omitir estos valores si están presentes.

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

Tamaño

CColumnSetPresent

ColumnSet (opcional)

... variable

CRestrictionPresent.

Restricción (opcional)

... variable

CSortSetPresent

SortSet (opcional)

... variable

CCategorizationSetPresent

CategorizationSet (opcional)

... variable

RowSetProperties

...

...

...

...

PidMapper (variable)



 

**Tamaño**: entero de 32 bits sin signo que indica el número de bytes desde el principio de este campo hasta el final del mensaje.

**CColumnSetPresent**: un campo de byte que indica si el campo ColumnSet está presente. Este campo debe establecerse en 0x01 o 0x00. Si se establece en 0x01, el campo CColumnSet debe estar presente. Si se establece en 0x00, debe estar ausente.

**ColumnSet**: estructura CColumnSet que contiene los números de columna en los que se van a devolver las propiedades de CPidMapper.

**CRestrictionPresent**: un campo de byte que indica si el campo de restricción está presente. Si se establece en un valor distinto de cero, el campo de restricción debe estar presente. Si se establece en 0x00, la restricción debe estar ausente.

**Restriction**: una estructura CRestriction que contiene el árbol de comandos de la consulta.

**CSortSetPresent**: un campo de byte que indica si el campo SortSet está presente. Si se establece en un valor distinto de cero, el campo SortSet debe estar presente. Si se establece en 0x00, SortSet debe estar ausente.

**SortSet**: una estructura CSortSet que indica el criterio de ordenación de la consulta.

**CCategorizationSetPresent**: un campo de byte que indica si el campo CCategorizationSet está presente. Si se establece en un valor distinto de cero, el campo CCategorizationSet debe estar presente. Si se establece en 0x00, CCategorizationSet debe estar ausente.

**CCategorizationSet**: una estructura CCategorizationSet que contiene los grupos de la consulta.

**RowSetProperties**: una estructura CRowsetProperties que proporciona información de configuración para la consulta.

**PidMapper**: estructura CPidMapper que contiene las propiedades que se van a devolver en un conjunto de filas.

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



 

**\_ fTrueSequential**: un valor booleano informativo que indica si se puede esperar que la consulta proporcione resultados más rápido. Cuando se establece en 0x00000001 para la consulta proporcionada en CPMCreateQueryIn, el servidor puede usar el índice de tal forma que los resultados de la consulta se entreguen más rápido. Cuando se establece en 0x00000000, habrá una latencia mayor en la entrega de los resultados de la consulta. No debe establecerse en ningún otro valor.

**\_ fWorkIdUnique**: un valor booleano que indica si los identificadores de documento a los que apuntan los cursores son únicos en todos los resultados de la consulta. Si se establece en 0x00000001, los identificadores son únicos. Si se establece en 0x00000000, solo son únicos en todo el conjunto de filas.

**aCursors**: matriz de enteros de 32 bits sin signo que representa los identificadores de los cursores, con el número de elementos igual al número de categorías en el campo CategorizationSet del mensaje CPMCreateQueryIn.

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



 

**\_ hCursor**: entero de 32 bits sin signo que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.

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

\_Status



 

**\_ Status**: máscara de máscara de valores definidos en las tablas siguientes, que describe la consulta.

En la tabla siguiente se enumeran \_ \* los valores estadísticos obtenidos realizando una operación and bit a bit \_ con el estado con 0x00000007. El resultado debe ser uno de los siguientes:



| Constante                 | Significado                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ busy ocupado    | La consulta asincrónica todavía se está ejecutando.                                          |
| ERROR de STAT \_ 0x00000001   | La consulta está en un estado de error.                                                   |
| STAT \_ Done 0x00000002    | La consulta se ha completado.                                                            |
| \_Actualizar la actualización de 0x00000003 | La consulta se ha completado, pero las actualizaciones tienen como resultado un cálculo de consulta adicional. |



 

En la tabla siguiente se enumeran los \_ \* bits de estadísticas adicionales que se pueden establecer de forma independiente.



| Constante                                    | Significado                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| \_Palabras irrelevantes de estadísticas \_ 0x00000010               | Las palabras irrelevantes se reemplazaron por caracteres comodín en la consulta de contenido.                                                              |
| \_Contenido estadístico \_ no \_ \_ actualizado     | Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados, pero no indexados.                             |
| ESTADÍSTICAS de \_ actualización \_ incompleta 0x00000040        | Los resultados de la consulta podrían ser incorrectos porque la consulta contenía archivos modificados y reindexados cuyo contenido no se incluía. |
| Consulta de contenido de STAT \_ \_ \_ incompleta 0x00000080 | La consulta de contenido era demasiado compleja para completarse o era necesaria para la enumeración en lugar de usar el índice de contenido.                          |
| Límite de tiempo de STAT \_ \_ \_ superado 0x00000100      | Los resultados de la consulta pueden ser incorrectos porque el tiempo de ejecución de la consulta alcanzó el tiempo máximo permitido.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

El mensaje CPMGetQueryStatusExIn solicita el estado de una consulta e información adicional, como el número de documentos que se han indizado, el número de documentos que quedan por indizar, etc. El formato del mensaje CPMGetQueryStatusExIn que sigue al encabezado es:



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

\_bmk



 

**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.

**\_ BMK**: un valor de 32 bits que indica el identificador de un marcador cuya posición se debe recuperar.

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

\_Status

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ Estado**: una de las estadísticas \_ \* los valores especificados en la sección 2.2.3.11.

**\_ cFilteredDocuments**: entero de 32 bits sin signo que indica el número de documentos que se han indexado.

**\_ cDocumentsToFilter**: entero de 32 bits sin signo que indica el número de documentos que todavía quedan indexados.

**\_ dwRatioFinishedDenominator**: entero de 32 bits sin signo que indica el denominador de la relación de los documentos que ha finalizado el procesamiento de la consulta.

**\_ dwRatioFinishedNumerator**: entero de 32 bits sin signo que indica el numerador de la relación de los documentos que ha finalizado el procesamiento de la consulta.

**\_ iRowBmk**: entero de 32 bits sin signo que indica la posición aproximada del marcador en el conjunto de filas en términos de filas.

**\_ cRowsTotal**: entero de 32 bits sin signo que especifica el número total de filas del conjunto de filas.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

El mensaje CPMSetBindingsIn solicita el enlace de las columnas a un conjunto de filas. El servidor responderá al mensaje de solicitud CPMSetBindingsIn mediante la sección de encabezado del mensaje CPMBindingsIn con los resultados de la solicitud incluida en el \_ campo Estado. El formato del mensaje CPMSetBindingsIn que sigue al encabezado es:



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

\_ficticio (opcional)

cColumns (opcional)

aColumns (variable, opcional)



 

**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la fila para la que se van a establecer enlaces. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**\_ cbRow**: entero de 32 bits sin signo que indica el tamaño, en bytes, de una fila. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**\_ cbBindingDesc**: entero de 32 bits sin signo que indica la longitud, en bytes, de los campos que siguen al \_ campo ficticio. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**\_ ficticio**: este campo no se utiliza y se debe omitir. Se puede establecer en cualquier valor arbitrario. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**cColumns**: entero de 32 bits sin signo que indica el número de elementos de la matriz aColumns. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**aColumns**: una matriz de las estructuras CTableColumn que describen las columnas de una fila del conjunto de filas. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje. Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje. Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.

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

... variable



 

**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se van a recuperar filas.

**\_ cRowsToTransfer**: entero de 32 bits sin signo que indica el número máximo de filas que el cliente desea recibir en respuesta a este mensaje.

**\_ cbRowWidth**: entero de 32 bits sin signo que indica la longitud de una fila, en bytes.

**\_ cbSeek**: entero de 32 bits sin signo que indica el tamaño del mensaje que empieza por ETYPE.

**\_ cbReserved**: entero de 32 bits sin signo que indica el tamaño, en bytes, de un mensaje CPMGetRowsOut (sin los campos Rows y SeekDescriptions). Este valor de este campo se agrega al valor del \_ campo cbSeek y, a continuación, se utiliza para calcular el desplazamiento del campo de filas en el mensaje CPMGetRowsOut.

**\_ cbReadBuffer**: entero de 32 bits sin signo que se debe establecer en el valor máximo del valor de \_ cbRowWidth o 1000 veces el valor de \_ cRowsToTransfer, redondeado al múltiplo más cercano de 512 bytes. El valor no debe ser mayor que 0x00004000.

**\_ ulClientBase**: entero de 32 bits sin signo que indica el valor base que se va a usar para los cálculos de puntero en el búfer de filas. Si se usan desplazamientos de 64 bits, el campo reserved2 del encabezado del mensaje se usa como los 32 bits superiores y \_ ulClientBase como los 32 bits inferiores de un valor de bit de 64. Vea la sección 2.2.3.16 para obtener más información.

**\_ fBwdFetch**: entero de 32 bits sin signo que indica el orden en el que se van a capturar las filas. Si se establece en 0x00000001, las filas se van a capturar en orden inverso. Si se establece en 0x00000000, las filas se van a capturar en orden hacia delante. NO debe establecerse en ningún otro valor.

**ETYPE**: entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación que se va a realizar.



| Value                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription contiene una estructura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una estructura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una estructura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contiene una estructura CRowSeekByBookmark. |



 

**\_ chapt**: un valor de 32 bits que representa el identificador del capítulo del conjunto de filas.

**SeekDescription**: este campo debe contener una estructura del tipo indicado por el valor ETYPE.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

El mensaje CPMGetRowsOut responde a un mensaje CPMGetRowsIn con las filas de una consulta. Los servidores deben dar formato a los desplazamientos de los tipos de datos de longitud variable en el campo filas como se indica a continuación:

-   El cliente indicó que era un sistema de 32 bits (0x00000008 o menos en el campo iClientVersion de CPMConnectIn): los desplazamientos son enteros de 32 bits.
-   El cliente indicó que era un sistema de 64 bits ( \_ iClientVersion > 0x00000008 en CPMConnectIn) y el servidor indicó que era un sistema de 32 bits ( \_ serverVersion establecido en 0X00000007 en CPMConnectOut): los desplazamientos son enteros de 32 bits
-   El cliente indicó que era un sistema de 64 bits ( \_ iClientVersion > 0x00000008 en CPMConnectIn) y el servidor indicó que era un sistema de 64 bits ( \_ serverVersion establecido en 0X00010007 en CPMConnectOut): los desplazamientos son enteros de 64 bits

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



 

**\_ cRowsReturned**: entero de 32 bits sin signo que indica el número de filas devueltas en filas.

**ETYPE**: entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación de rowseek que se va a realizar.



| Value                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | No SeekDescription, ignore el campo SeekDescription.        |
| eRowSeekNext 0x00000001       | SeekDescription contiene una estructura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contiene una estructura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contiene una estructura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contiene una estructura CRowSeekByBookmark. |



 

**\_ chapt**: un valor de 32 bits que representa el identificador del capítulo del conjunto de filas.

**SeekDescription**: este campo debe contener una estructura del tipo indicado por el campo ETYPE.

**paddingRows**: este campo debe tener una longitud suficiente (de 0 a \_ cbReserved-1 bytes) para rellenar el campo de filas en el \_ desplazamiento de cbReserved desde el principio de un mensaje, donde \_ cbReserved es el valor del mensaje CPMGetRowsIn. Los bytes de relleno usados en este campo pueden ser cualquier valor arbitrario. El receptor debe omitir este campo.

**Rows**: los datos de fila, tienen el formato que indica la información de columna en el mensaje CPMSetBindingsIn más reciente. Las filas deben almacenarse en orden directo (por ejemplo, la fila 1 antes de la fila 2).

Las columnas de tamaño fijo deben almacenarse en los desplazamientos especificados por el mensaje CPMSetBindingsIn más reciente.

Las columnas de tamaño variable (por ejemplo, cadenas) deben almacenarse de la siguiente manera:

-   Los datos de la variable (por ejemplo, la cadena) se almacenan cerca del final del búfer en orden descendente (por ejemplo, la colección de todos los datos variables de la fila 1 está al final, la fila 2 siguiente más cercana, etc.).
-   El área de tamaño fijo (al principio del búfer de filas) debe contener una CRowVariant para cada columna, almacenada en el desplazamiento especificado en el mensaje de CPMSetBindingsIn más reciente. vType debe contener el tipo de datos (por ejemplo: VT \_ LPWStr). Si, según lo determinado por las reglas al principio de la sección, se usan desplazamientos de 32 bits, el campo de desplazamiento de CRowVariant debe contener un valor de 32 bits que sea el desplazamiento de los datos variables desde el principio del mensaje CPMGetRowsOut, más el valor de \_ ulClientBase especificado en el mensaje CPMGetRowsIn más reciente. Si se usan desplazamientos de 64 bits, el campo de desplazamiento de CRowVariant debe contener un valor de 64 bits, que es el desplazamiento desde el principio del mensaje CPMGetRowsOut, que se agrega a un valor de 64 bits compuesto por el uso de \_ ulClientBase como el nivel de 32-bits bajo y \_ ulReserved2 como el alto de 32 bits.

Por ejemplo, si el mensaje CPMSetBindingsIn especifica dos columnas: Size (VT \_ I4) y title (VT \_ LPWStr)-y \_ ulClientBase de CPMGetRowsIn se 0x10000, entonces dos filas tendrían el siguiente aspecto. La sección marcada en gris es la parte de longitud fija del búfer.

![ejemplo de mensaje de cpmsetbindingsin](images/cpmgetrowsout.gif)

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



 

**\_ hCursor**: identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a solicitar la información de finalización.

**\_ fQuick**: debe establecerse en 0x00000001. No se usa y el servidor debe pasarlo por alto.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

El mensaje CPMRatioFinishedOut responde a un mensaje CPMRatioFinishedIn con la relación de finalización de una consulta. El formato del mensaje CPMRatioFinishedOut que sigue al encabezado es:



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

\_cRows

\_fNewRows



 

**\_ ulNumerator**: entero de 32 bits sin signo que indica el numerador de la relación de finalización en términos de filas.

**\_ ulDenominator**: entero de 32 bits sin signo que indica el denominador de la relación de finalización en términos de filas. DEBE ser mayor que cero.

**\_ Crows**: entero de 32 bits sin signo que indica el número total de filas de la consulta.

**\_ fNewRows**: un valor booleano que indica si hay nuevas filas disponibles. Un valor de 0x00000001 indica que las nuevas filas están disponibles en el conjunto de filas. Un valor de 0x00000000 indica que el conjunto de filas no contiene ninguna fila nueva. Este campo no se debe establecer en ningún otro valor.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

El mensaje CPMFetchValueIn solicita un valor de propiedad que era demasiado grande para devolver en un conjunto de filas. Tal y como se especifica en la sección 3.2.4.2.5, este mensaje se envía repetidamente para recuperar todos los bytes de la propiedad, actualizando \_ cbSoFar para cada uno, hasta que el \_ campo fMoreExists del mensaje CPMFetchValueOut se establece en **false**.

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

\_WID

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (variable)

...

\_padding (variable)



 

**\_ WID**: entero de 32 bits sin signo que representa el identificador de documento que identifica el documento para el que se debe capturar una propiedad.

**\_ cbSoFar**: entero de 32 bits sin signo que contiene el número de bytes transferidos previamente para esta propiedad. DEBE establecerse en 0x00000000 en el primer mensaje.

**\_ cbPropSpec**: entero de 32 bits sin signo que contiene el tamaño del campo PropSpec, en bytes.

**\_ cbChunk**: entero de 32 bits sin signo que contiene el número máximo de bytes que el remitente puede aceptar en un mensaje de CPMFetchValueOut.

*Comportamiento de Windows: este campo se establece en 0x00004000 para todas las versiones de Windows.*

**PropSpec**: estructura CFullPropSpec que especifica la propiedad que se va a recuperar.

**\_ padding**: este campo debe tener la longitud necesaria (de 0 a 3 bytes) para rellenar el mensaje hasta un múltiplo de 4 bytes de longitud. El valor de los bytes de relleno puede ser cualquier valor arbitrario. El receptor debe omitir este campo.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

El mensaje CPMFetchValueOut responde a un mensaje CPMFetchValueIn con un valor de propiedad de una consulta anterior. Tal y como se especifica en la sección 3.1.5.2.8, este mensaje se envía después de cada mensaje de CPMFetchValueIn hasta que se transfieren todos los bytes de la propiedad.

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



 

**\_ cbValue**: entero de 32 bits sin signo que contiene el tamaño total, en bytes, en vValue.

**\_ fMoreExists**: un valor booleano que indica si hay mensajes CPMFetchValueOut adicionales disponibles. Si se establece en 0x00000001, hay mensajes CPMFetchValueOut adicionales. Si se establece en 0x00000000, no hay mensajes CPMFetchValueOut adicionales disponibles.

**\_ fValueExists**: un valor booleano que indica si hay un valor para la propiedad. Si se establece en 0x00000001, existe un valor para la propiedad. Si se establece en 0x00000000, no existe un valor para la propiedad.

**vType**: un valor de la enumeración VARENUM, vea la sección 2.2.1.1 para obtener más información, que describe el tipo de la propiedad.

**vValue**: una parte de una matriz de bytes que contiene una estructura SERIALIZEDPROPERTYVALUE, tal como se especifica en la sección 2.2.1.32, donde el desplazamiento del principio de la parte es el valor de \_ cbSoFar en CPMFetchValueIn. La longitud de la parte, indicada por el \_ campo cbValue, debe ser igual al valor de \_ CbChunk en CPMFetchValueIn si \_ fMoreExists está establecido en 0x00000001 y debe ser menor o igual que el valor de \_ cbChunk en caso contrario.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

El mensaje CPMGetNotify solicita que el cliente desea recibir una notificación de los cambios del conjunto de filas.

El mensaje no debe incluir un cuerpo; solo se enviará el encabezado del mensaje, como se especifica en la sección 2.2.2.

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



 

**\_ watchNotify**: el cambio en la consulta. DEBE ser uno de los siguientes valores:



| Value                                     | Significado                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | El número de filas del conjunto de filas de consulta ha cambiado. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | La consulta se ha completado.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | Se ha vuelto a ejecutar la consulta.                     |



 

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

\_bmk



 

**\_ hCursor**: un valor de 32 bits que representa el cursor de consulta Obtenido de CPMCreateQueryOut para el conjunto de filas que contiene el marcador.

**\_ chapt**: un valor de 32 bits que representa el identificador del segmento que contiene el marcador.

**\_ BMK**: un valor de 32 bits que representa el identificador del marcador para el que se va a recuperar la posición aproximada.

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



 

**\_ numerador**: entero de 32 bits sin signo que contiene el número de fila del marcador en el conjunto de filas. Si no hay ninguna fila, este campo debe establecerse en 0x00000000.

**\_ denominador**: entero de 32 bits sin signo que contiene el número de filas del conjunto de filas.

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



 

\_**hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut para el conjunto de filas que contiene los marcadores.

\_**chapt**: un valor de 32 bits que representa el identificador del capítulo que contiene los marcadores que se van a comparar.

\_**bmkFirst**: un valor de 32 bits que representa el identificador del primer marcador que se va a comparar.

\_**bmkSecond**: un valor de 32 bits que representa el identificador del segundo marcador que se va a comparar.

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



 

\_**dwComparison**: uno de los siguientes valores, que indica las posiciones relativas de los dos marcadores del capítulo.



| Value                               | Significado                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ lt 0x00000000            | El primer marcador se coloca antes del segundo.               |
| DBCOMPARE \_ EQ 0x00000001            | El primer marcador tiene la misma posición que el segundo.           |
| DBCOMPARE \_ gt 0x00000002            | El primer marcador se coloca después del segundo.                |
| DBCOMPARE \_ ne 0x00000003            | El primer marcador no tiene la misma posición que el segundo. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | El primer marcador no es comparable al segundo.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

El mensaje CPMRestartPositionIn mueve la posición de captura de un cursor al principio del capítulo. Como se especifica en la sección 3.1.5.2.12, el servidor responderá con el mismo mensaje, con los resultados de la solicitud contenidos en el \_ campo status del encabezado CISP.

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



 

**\_ hCursor**: un valor de 32 bits que representa el identificador obtenido a partir de un mensaje CPMCreateQueryOut, que identifica la consulta para la que se va a reiniciar la posición. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

**\_ chapt**: valor de 32 bits que representa el identificador de un capítulo del que se van a recuperar filas. Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

El mensaje CPMFreeCursorIn solicita el lanzamiento de un cursor. El formato del mensaje CPMFreeCursorIn que sigue al encabezado es:



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



 

**\_ hCursor**: un valor de 32 bits que representa el identificador del cursor del mensaje CPMCreateQueryOut que se va a liberar.

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



 

**\_ cCursorsRemaining**: entero de 32 bits sin signo que indica el número de cursores que todavía están en uso para la consulta.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

El mensaje CPMDisconnect finaliza la conexión con el servidor

El mensaje no debe incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.

### <a name="224-errors"></a>2.2.4 errores

Todos los mensajes de protocolo del servicio de indización de contenido deben devolver 0x00000000 en caso de éxito; de lo contrario, devuelven un código de error distinto de cero 32, que puede ser un valor HRESULT o un valor NTSTATUS (consulte la sección 1,8). Si un búfer es demasiado pequeño para ajustarse a un resultado, se debe devolver un código de estado de \_ recursos insuficientes \_ (0xC0000009A) y se debe volver a intentar la operación con un búfer mayor.

El resto de los valores de error deben tratarse de la misma.

(Tenga en cuenta que actualmente no se superponen los espacios de numeración de HRESULT y NTSTATUS excepto con valores idénticos, pero incluso si fueran conflictos en el futuro, no produciría ningún problema de protocolo, siempre que el valor de estado \_ Los recursos insuficientes \_ siguen siendo únicos, ya que todos los demás valores de error se tratan igual.)

## <a name="3-protocol-details"></a>3 Detalles del protocolo

-   [Detalles del servidor 3,1](#31-server-details)
-   [Detalles del cliente 3,2](#32-client-details)

Las solicitudes de mensajes de CISP para consultar de forma remota los catálogos del servicio de indexación no requieren ninguna secuencia determinada. Sin embargo, se recomienda que la capa superior se adhiere a una secuencia de mensajes significativa, como en el caso de los mensajes que se reciben fuera de esta secuencia o con datos no válidos, el servidor responderá con un error. Algunos mensajes también dependen de la capa superior que proporciona datos válidos que se recibieron en los mensajes anteriores de la secuencia.

En el diagrama siguiente se muestra una secuencia de mensajes típica para una consulta simple desde un cliente a un equipo remoto.

![secuencia de mensajes para consulta simple](images/protocoldetails.jpg)

Los mensajes representados en el diagrama anterior representan un subconjunto de todos los mensajes de CISP usados para consultar un catálogo de servicios de indexación remota.

### <a name="31-server-details"></a>Detalles del servidor 3,1

### <a name="311-abstract-data-model"></a>3.1.1 Modelo de datos abstracto

En la sección siguiente se especifican los datos y el estado mantenidos por el servidor CISP. Los datos que se proporcionan aquí son para facilitar la explicación de cómo se comporta el protocolo. En esta sección no se exige que las implementaciones se adhieren a este modelo, siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.

Un servicio de indización que implementa CISP debe mantener los siguientes elementos de datos abstractos:

-   La lista de clientes conectados al servidor
-   Información acerca de cada cliente, que incluye:
-   -   Versión del cliente (como se indica en el mensaje CPMConnectIn especificado en la sección 2.2.3.6)
    -   Catálogo asociado al cliente (mediante un mensaje CPMConnectIn)
    -   Propiedades de cliente adicionales como se especifica en la sección 2.2.1.21.1.
    -   Consulta de búsqueda del cliente
    -   Lista de identificadores de cursor para la consulta y posición en el conjunto de resultados para cada identificador.
    -   Conjunto actual de enlaces
    -   Estado actual de la consulta que incluye (para cada cursor):
    -   -   Número de filas en el resultado de la consulta
        -   Numerador y denominador de finalización de consulta
        -   Último número de filas, indicado por el mensaje CPMRatioFinishedOut más reciente para este cursor
        -   Si el servidor supervisa la consulta en busca de cambios en los resultados de la consulta y, si se supervisa, qué ha cambiado en los resultados de la consulta desde la última vez que se comunicó al cliente por CPMSendNotifyOut
        -   Lista de identificadores de capítulos, atendidos por esta consulta a un cliente.
        -   Lista de identificadores de marcador para cada cursor, servido por esta consulta a un cliente.

-   Estado actual del servicio de indización, que puede ser "no inicializado", "en ejecución" o "cerrando". Tenga en cuenta que la mayoría del servidor horario está en estado "en ejecución". A continuación se indica el diagrama de la máquina de Estados para el servidor:

    ![diagrama de equipo de estado del servidor de servicios de Index Server](images/abstractdatamodel.jpg)

-   Información sobre el catálogo: el número de documentos indizados, el tamaño del índice, el número de claves únicas, etc. (consulte la sección 2.2.3.1 para completar la lista), State (que corresponde a los valores de dwNewState de la sección 2.2.3.2).
-   Para cada idioma admitido, una base de datos de variaciones de palabras, tal como se describe en la sección 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Temporizadores

No se requieren temporizadores de protocolos.

### <a name="313-initialization"></a>3.1.3 Inicialización

Tras la inicialización, el servidor debe establecer su estado en "no inicializado" e iniciar la escucha de mensajes en la canalización con nombre especificada en la sección 1,9. Después de realizar cualquier otra inicialización interna, debe pasar al estado "en ejecución".

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Eventos desencadenados al más alto nivel

Ninguno.

### <a name="315-message-processing-and-sequencing-rules"></a>Reglas de procesamiento y secuenciación de mensajes de 3.1.5

Siempre que se produce un error durante el procesamiento de un mensaje enviado por un cliente, el servidor debe notificar un error al cliente de la siguiente manera:

-   Detener el procesamiento del mensaje enviado por el cliente
-   Responda con el encabezado del mensaje (solo) del mensaje enviado por el cliente, manteniendo el \_ campo MSG intacto.
-   Establezca el \_ campo Estado en el valor del código de error.

Cuando llega un mensaje, el servidor debe comprobar el \_ valor del campo MSG para ver si se trata de un tipo conocido (consulte la sección 2.2.2). Si no se conoce el tipo, debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).

El servidor debe validar el \_ valor del campo ulChecksum si el tipo de mensaje es uno de los siguientes:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Para validar el \_ valor del campo ulChecksum, el servidor debe comprobar el valor especificado por el cliente en el \_ campo iClientVersion del mensaje CPMConnectIn.

Si el \_ campo iClientVersion no se establece en 0x00000008 y el \_ campo ulChecksum no se establece en 0x00000000, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D). El servidor no debe validar el \_ campo ulChecksum para los clientes. establezca el \_ campo iClientVersion en un valor inferior a 0x00000008.

Si el \_ valor del campo iClientVersionfield es 0x00000008 o superior, el servidor debe validar que el \_ campo ulChecksum se calculó como se especifica en la sección 3.2.4. Si el \_ valor de ulChecksum no es válido, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).

A continuación, el servidor comprueba en qué estado se encuentra. Si su estado es "no inicializado", el servidor debe notificar un error de CI \_ E \_ no \_ inicializado (0x8004180B). Si el estado es "cerrando", el servidor debe notificar un \_ error de cierre de CI E \_ (0x80041812).

Una vez que se ha determinado que un encabezado es válido y el servidor está en estado "en ejecución", se debe realizar un procesamiento adicional específico del mensaje tal y como se especifica en las subsecciones siguientes.

### <a name="3151-remote-indexing-service-catalog-management"></a>Administración de catálogos del servicio de indexación remota de 3.1.5.1

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 recibir una solicitud de CPMCiStateInOut

Cuando el servidor recibe una solicitud de mensaje de CPMCIStateInOut desde el cliente, el servidor debe comprobar primero si el cliente está en una lista de clientes conectados. Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D). De lo contrario, debe responder al cliente con un mensaje CPMCIStateInOut, rellenándolo con información sobre el catálogo asociado del cliente, tal como se especifica en la sección 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 recibir una solicitud de CPMSetCatStateIn

Cuando el servidor recibe una solicitud de mensaje de CPMSetCatStateIn desde el cliente, el servidor debe hacer lo siguiente:

-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo, el servidor debe notificar un \_ error de acceso \_ denegado (0xC0000022).
-   Si \_ dwNewState no es igual que CiCAT \_ todos \_ abiertos, cambie el estado del catálogo especificado en el campo CatName de acuerdo con lo especificado en el \_ campo dwNewState. Vea la sección 2.2.3.2 para obtener más detalles. Si el servidor no encuentra un catálogo con el nombre especificado en el campo CatName, el servidor debe devolver un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Responder al cliente con un mensaje CPMSetCatStateOut, donde \_ DWOLDSTATE debe establecerse en el estado anterior del catálogo. Si \_ dwNewState es igual a CiCAT \_ todos los \_ abiertos, el servidor debe comprobar el estado de todos los catálogos y, si todos ellos se han iniciado, debe establecer \_ dwOldState en 0x00000001 y, de lo contrario, establecer \_ dwOldState en 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 recibir una solicitud de CPMUpdateDocumentsIn

Cuando el servidor recibe una solicitud de mensaje CPMUpdateDocumentsIn, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente está en una lista de clientes conectados (que tienen asociado un catálogo). Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).
-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo al servidor, el servidor debe notificar un error de \_ acceso \_ denegado (0xC0000022).
-   Comienza el proceso de indización de la ruta de acceso especificada por el cliente, realizando un examen completo o incremental, en función del valor del \_ campo Flag en el mensaje CPMUpdateDocumentsIn. Si la ruta de acceso no se ha indizado previamente, debe agregarse a la colección de ubicaciones indizadas y realizar un examen completo. Si se especifica un valor no válido del \_ campo de marca, el servidor debe actuar como si la \_ marca estuviera establecida en UPD \_ init y realizar un examen completo. Esta operación debe realizarse en el catálogo asociado al cliente.
-   Responda al cliente con el encabezado del mensaje de CPMUpdateDocumentsIn y establezca el \_ campo Estado en los resultados de la solicitud.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 recibir una solicitud de CPMForceMergeIn

Cuando el servidor recibe una solicitud de mensaje CPMForceMergeIn, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente está en una lista de clientes conectados (que tienen asociado un catálogo). Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).
-   Compruebe que el cliente tiene acceso administrativo. Si el cliente no tiene acceso administrativo, el servidor debe notificar un \_ error de acceso \_ denegado (0xC0000022).
-   Comience cualquier proceso de mantenimiento necesario para mejorar el rendimiento de las consultas en un catálogo, asociado al cliente.
-   Responda al cliente con un encabezado de mensaje para CPMForceMergeIn y establezca el \_ campo Estado en los resultados de la solicitud.

Tenga en cuenta que el proceso de mantenimiento es asincrónico y puede continuar después de que el cliente reciba el mensaje de respuesta. Este proceso no afecta directamente al Protocolo de ninguna manera (a excepción del tiempo de respuesta).

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 consulta de servicio de indexación remota

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 recibir una solicitud de CPMConnectIn

Cuando el servidor recibe una solicitud CPMConnectIn de un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente está en la lista de clientes conectados. En este caso, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Comprueba si el catálogo especificado existe y no está en estado detenido. Si no es así, el servidor debe tener un error de CI \_ E \_ no \_ Catalog (0x8004181D) de informe.
-   Agregue el cliente a la lista de clientes conectados.
-   Asocie el catálogo con el cliente.
-   Almacene la información que se pasa en el mensaje CPMConnectIn (como el nombre del catálogo, la versión del cliente, etc.) en el estado del cliente.
-   Responder al cliente con un mensaje CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 recibir una solicitud de CPMCreateQueryIn

Cuando el servidor recibe una solicitud de mensaje de CPMCreateQueryIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente está en la lista de clientes conectados. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el cliente ya tiene una consulta asociada. En este caso, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el catálogo asociado al cliente está en el estado que permite procesar la consulta (CICAT \_ ReadOnly o CiCAT \_ grabable). Si no es así, el servidor debe notificar un error QUERY \_ S \_ no \_ query (0x8004160C).
-   Analiza el conjunto de restricciones, los criterios de ordenación y las agrupaciones especificados en la consulta. Si el servidor encuentra un error, debe informar de un error adecuado. Si se produce un error en este paso por cualquier otro motivo, el servidor debe notificar el error encontrado. Para obtener información acerca de los errores de consulta del servicio de indización, consulte \[ MSDN-QUERYERR \] .
-   Guarde la consulta de búsqueda en el estado del cliente.
-   Realice los preparativos necesarios para servir las filas a un cliente y asocie la consulta con los identificadores de cursor adecuados (dependiendo de la información pasada en el mensaje CPMCreateQueryIn).
-   Agregue esos identificadores a la lista de identificadores de cursor del cliente e inicialice listas de identificadores de capítulo y marcadores.
-   Inicializa la lista de identificadores de capítulo para cada cursor de esta consulta en DB \_ null \_ HCHAPTER
-   Inicializa la lista de identificadores de marcador para cada cursor de esta consulta en un conjunto de DBBMK \_ First y DBBMK \_ Last.
-   Marque la consulta como no supervisada para los cambios.
-   Inicializa el número de filas en el número calculado actualmente de filas (que puede ser 0 si la consulta no se inició para ejecutar o algún número si la consulta está en un proceso de ejecución) e inicializa el numerador y el denominador de finalización de la consulta.
-   Responder al cliente con un mensaje CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 recibir una solicitud de CPMGetQueryStatusIn

Cuando el servidor recibe una solicitud de mensaje de CPMGetQueryStatusIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor está en una lista de identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Preparar un mensaje CPMGetQueryStatusOut. El servidor debe recuperar el estado de la consulta actual y establecerlo en el \_ campo QStatus (consulte 2.2.3.11 para ver los valores posibles). Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
-   Responder al cliente con el mensaje CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 recibir una solicitud de CPMGetQueryStatusExIn

Cuando el servidor recibe una solicitud de mensaje de CPMGetQueryStatusExIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor que se ha pasado está en una lista de identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Preparar un mensaje CPMGetQueryStatusExOut. El servidor debe recuperar el estado de la consulta actual y el progreso de la consulta y establecer QStatus (vea 2.2.3.11 para ver los valores posibles), \_ dwRatioFinishedDenominator y \_ dwRatioFinishedNumerator, respectivamente. A continuación, debe establecer el número de filas de los resultados de la consulta en \_ cRowsTotal. Si se produce un error en este paso por cualquier motivo, el servidor debe notificar que se ha detectado un error.
-   Recupere información sobre el catálogo del cliente y rellene \_ cFilteredDocuments y \_ cDocumentsToFilter. Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.
-   Recupere la posición del marcador indicado por el identificador en el \_ campo BMK y rellene el \_ campo iRowBmk restante en el mensaje CPMGetQueryStatusExOut. Si se produce un error en este paso por cualquier motivo, el servidor debe notificar que se ha detectado un error.
-   Responder al cliente con el mensaje CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 recibir una solicitud de CPMRatioFinishedIn

Cuando el servidor recibe una solicitud de mensaje de CPMRatioFinishedIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Preparar un mensaje CPMRatioFinishedOut. El servidor debe recuperar el estado de la consulta del cliente y rellenar los \_ campos ulNumerator, \_ ulDenominator y \_ Crows. Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.
-   Si \_ Crows es igual al último número de filas del que se ha comunicado esta consulta, establezca \_ fNewRows en 0x00000000; de lo contrario, establézcalo en 0x00000001.
-   Actualice el último número de filas del que se ha comunicado esta consulta al valor de \_ Crows.
-   Responder al cliente con el mensaje CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 recibir una solicitud de CPMSetBindingsIn

Cuando el servidor recibe una solicitud de mensaje de CPMSetBindingsIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Compruebe que la información de los enlaces es válida (es decir, la columna especifica el valor, la longitud o el estado que se va a devolver; no se superponen en los enlaces del valor, la longitud o el estado; y el valor, la longitud y el estado caben en el tamaño de fila especificado) y si no se notifica un error de la base de datos \_ \_ BADBINDINFO
-   Guarde la información de enlace asociada a las columnas especificadas en el campo aColumns. Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.
-   Responda al cliente con un encabezado de mensaje (solo) con \_ el mensaje establecido en CPMSetBindingsIn y \_ el estado establecido en los resultados del enlace especificado.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 recibir una solicitud de CPMGetRowsIn

Cuando el servidor recibe una solicitud de mensaje de CPMGetRowsIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor que se pasa está en athelist de los identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Compruebe si el cliente tiene un conjunto actual de enlaces. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Preparar un mensaje CPMGetRowsOut. El servidor debe colocar el cursor en los resultados de la consulta como se indica en la descripción de búsqueda. Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.
-   Obtiene tantas filas como quepan en un búfer, cuyo tamaño se indica mediante \_ cbReadBuffer, pero no más de lo indicado por \_ cRowsToTransfer. Al capturar filas, el servidor debe comparar el tipo de valor de propiedad de cada columna seleccionada con el tipo especificado en el conjunto actual de enlaces del cliente (sección 3.1.1). Si el tipo del enlace no es una variante de VT \_ , el servidor debe intentar convertir el valor de la propiedad de la columna a ese tipo. De lo contrario, si \_ se establece la marca DBPROP USEEXTENDEDDBTYPES en el conjunto de propiedades DBPROPSET QUERYEXT del cliente \_ , o si el valor de la propiedad de la columna no es un \_ tipo de vector VT, el valor de la propiedad se debe devolver en su tipo normal. Si ninguno de estos es el caso (es decir, el servidor tiene un \_ tipo de vector VT y el cliente no admite el \_ Vector VT), el servidor debe intentar convertirlo en un \_ tipo de matriz VT de la siguiente manera: los \_ elementos de matriz VT i8, VT \_ UI8, VT \_ FILETIME y VT \_ CLSID no se pueden convertir y se producirá un error en su lugar. Los \_ elementos de matriz VT LPSTR y VT \_ LPWStr deben convertirse en VT \_ BSTR; los elementos de la matriz de todos los demás tipos deben permanecer sin cambios. Por último, si las columnas de fila contienen identificadores de capítulo o de marcador, el servidor debe actualizar las listas correspondientes. Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.
-   Almacenar el número real de filas capturadas en \_ cRowsReturned.
-   Copie el campo Descripción de búsqueda y capítulo de CPMGetRowsIn en un mensaje de CPMGetRowsOut para enviarlo.
-   Almacene las filas capturadas en el campo Rows (vea la nota sobre el byte de estado siguiente y la sección 2.2.3.16 en la estructura del campo Rows).
-   Responder al cliente con el mensaje CPMGetRowsOut.

Nota sobre el campo de bytes de estado:

Si StatusUsed se establece en 0x01 en el CTableColumn del mensaje CPMSetBindingIn para la columna, el servidor debe establecer el byte de estado (que se encuentra en StatusOffset desde el inicio de la fila) para esta columna en uno de los valores siguientes:



| Value | Significado        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Si el valor de la propiedad no está presente en esta fila, el servidor debe establecer el byte de estado en StatusNull. Si el valor es demasiado grande para transferirse en el mensaje CPMGetRowsOut, el servidor debe establecer el byte de estado en StatusDeferred. En caso contrario, el servidor debe establecer el byte de estado en StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 recibir una solicitud de CPMFetchValueIn

Cuando el servidor recibe una solicitud de mensaje de CPMFetchValueIn desde un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Preparar un mensaje CPMFetchValueOut. Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
-   Busque el documento indicado por el \_ campo WID y compruebe si el identificador de propiedad de este documento (más adelante conocido como ' valor de propiedad ') indicado por la estructura PropSpec está disponible para este cliente. Si este valor no está disponible, el servidor debe establecer \_ fValueExists en 0x00000000 y, de lo contrario, establecer \_ fValueExists en 0x00000001. Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
-   Si \_ fValueExists es igual a 0x00000001, el servidor debe hacer lo siguiente:
-   -   Serialice el valor de propiedad en una estructura SERIALIZEDPROPERTYVALUE y copie, empezando por el \_ desplazamiento cbSoFar, como máximo \_ cbChunk bytes (pero no más allá del final de la propiedad serializada) al campo vValue. Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
    -   Establezca \_ cbValue en el número de bytes copiados en el paso anterior.
    -   Establezca vType en el tipo de propiedad del valor de propiedad.
    -   Si la longitud de la propiedad serializada es mayor que \_ cbSoFar se agrega a \_ cbValue, establezca \_ fMoreExists en 0x00000001; de lo contrario, establézcalo en 0x00000000.

-   Responder al cliente con el mensaje CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 recibir una solicitud de CPMGetNotify

Cuando el servidor recibe un mensaje CPMGetNotify de un cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Si no se ha producido ningún cambio en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut para este cliente, o si la consulta no está supervisada actualmente para los cambios del conjunto de resultados, el servidor debe responder con el mensaje CPMGetNotify y empezar a supervisar la consulta en busca de cambios en el conjunto de resultados. Si posteriormente hay un cambio en el conjunto de resultados de la consulta, el servidor debe enviar exactamente un mensaje CPMSendNotifyOut al cliente y debe especificar el cambio en el \_ campo watchNotify.
-   Si hubo cambios en el conjunto de resultados de la consulta desde el último mensaje de CPMSendNotifyOut, el servidor debe responder con CPMSendNotifyOut y debe especificar el cambio en el \_ campo watchNotify. Tenga en cuenta que, en el caso de muchos cambios en los resultados de la consulta, DBWATCHNOTIFY \_ ROWSCHANGED tiene prioridad (es decir, si la consulta se ha realizado, se vuelve a ejecutar y, a continuación, se ha cambiado el número de filas y la consulta se ha realizado de nuevo, el evento indicado sería DBWATCHNOTIFY \_ ROWSCHANGED).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 recibir una solicitud de CPMGetApproximatePositionIn

Cuando el servidor recibe una solicitud de mensaje de CPMGetApproximatePositionIn desde el cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor, el identificador de capítulo y el identificador de marcador pasados están en las listas correspondientes. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Busque una fila que esté asociada al identificador de marcador en los resultados de la consulta y aproxime la posición de la fila en el conjunto de filas, a la que hace referencia el identificador del capítulo, y determine el numerador y el denominador para la posición. Tenga en cuenta que cuando el identificador del capítulo es DB \_ null \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta. Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
-   Responder al cliente con un mensaje CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 recibir una solicitud de CPMCompareBmkIn

Cuando el servidor recibe una solicitud de mensaje de CPMCompareBmkIn desde el cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor, el identificador de capítulo y los identificadores de marcador pasados están en las listas correspondientes. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Preparar un mensaje CPMCompareBmkOut.
-   Si los identificadores de marcador son iguales, \_ DWCOMPARISON debe estar establecido en DBCOMPARE \_ EQ.
-   De lo contrario, si uno de los marcadores se DBBMK \_ primero o DBBMK \_ por último, entonces \_ dwComparison debe establecerse en DBCOMPARE \_ ne.
-   En caso contrario, el servidor debe hacer lo siguiente:
-   -   Buscar filas a las que hace referencia cada identificador de marcador en los resultados de la consulta
    -   Si alguna de las filas no está en el capítulo indicado por el identificador de capítulo en CPMCompareBmkIn, \_ DWCOMPARISON debe establecerse en DBCOMPARE \_ NOTCOMPARABLE.
    -   De lo contrario, cuando ambas filas están en el mismo capítulo, el servidor debe aproximar una posición de las filas del conjunto de filas al que se hace referencia en el identificador de este capítulo. A continuación, debe comparar los valores de posición y establecer \_ dwComparison en DBCOMPARE \_ lt si la posición de la primera fila es menor que la posición de la segunda fila; de lo contrario, \_ dwComparison debe establecerse en DBCOMPARE \_ gt.

-   Responder al cliente con el mensaje CPMCompareBmkOut rellenado.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 recibir una solicitud de CPMRestartPositionIn

Cuando el servidor recibe la solicitud de mensaje CPMRestartPositionIn desde el cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor y el identificador de capítulo pasados están en las listas correspondientes. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Mueva el cursor al principio del capítulo, identificado por el identificador del capítulo. Tenga en cuenta que cuando el identificador del capítulo es DB \_ null \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta. Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.
-   Responder al cliente con un mensaje CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 recibir una solicitud de CPMFreeCursorIn

Cuando el servidor recibe una solicitud de mensaje de CPMFreeCursorIn desde el cliente, el servidor debe hacer lo siguiente:

-   Compruebe si el cliente tiene una consulta asociada. Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).
-   Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente. Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).
-   Libere el cursor y los recursos asociados (consulte la sección 3.1.1 para obtener una lista completa) para este identificador de cursor.
-   Quite el cursor de la lista de cursores para ese cliente.
-   Responda con un mensaje de CPMFreeCursorOut, estableciendo el \_ campo cCursorsRemaining con el número de cursores restantes. en la lista de este cliente.
-   Si no hay más cursores para este cliente, el servidor debe liberar la consulta y los recursos asociados (consulte la sección 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 recibir una solicitud de CPMDisconnect

Cuando el servidor recibe una solicitud de mensaje de CPMDisconnect desde el cliente, el servidor debe quitar el cliente de la lista de clientes conectados y liberar todos los recursos asociados con el cliente.

### <a name="316-timer-events"></a>Eventos de temporizador de 3.1.6

Ninguno.

### <a name="317-other-local-events"></a>3.1.7 otros eventos locales

Cuando se detiene el servidor, primero debe realizar la transición al estado "cerrando". A continuación, debe dejar de escuchar la canalización, realizar cualquier otra tarea de apagado específica de la implementación y, a continuación, pasar al estado "detenido".

### <a name="32-client-details"></a>Detalles del cliente 3,2

### <a name="321-abstract-data-model"></a>3.2.1 modelo de datos abstracto

En la sección siguiente se especifican los datos y el estado que mantiene el cliente del protocolo del servicio de indización de contenido. Los datos proporcionados son para facilitar la explicación de cómo se comporta el protocolo. En esta sección no se exige que las implementaciones se adhieren a este modelo, siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.

Un cliente tiene el siguiente estado abstracto:

-   **Último mensaje enviado**: una copia del último mensaje enviado al servidor.
-   **Valor de propiedad actual**: valor parcial de una propiedad "diferida", que se encuentra en proceso de recuperación.
-   **Bytes recibidos actuales**: el número de bytes recibidos para el valor actual de la propiedad hasta ahora.
-   **Estado de conexión de canalización con nombre**: conexión al servidor

### <a name="322-timers"></a>3.2.2 temporizadores

No se requieren temporizadores de protocolos.

### <a name="323-initialization"></a>inicialización de 3.2.3

No se realiza ninguna acción hasta que se recibe una solicitud de nivel superior.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer eventos desencadenados

Cuando se recibe una solicitud de una capa superior, el cliente debe crear una conexión de canalización con nombre en el servidor, con los detalles especificados en la sección 2,1. Si no puede hacerlo, debe haber un error en la solicitud de nivel superior. Es decir, en caso de que se produzca un error de conexión, es responsabilidad del nivel superior volver a intentarlo si lo desea.

Un encabezado debe anteponerse al conjunto de campos especificado en la sección 2.2.2.

En el caso de los mensajes que se especifican como que requieren una suma de comprobación distinto de cero, el \_ valor de ulChecksum se debe calcular de la manera siguiente:

1.  El contenido del mensaje después del \_ campo ulReserved2 en el encabezado del mensaje debe interpretarse como una secuencia de enteros de 32 bits. El cliente debe calcular la suma de los valores numéricos proporcionados por estos enteros.
2.  Calcula la operación XOR bit a bit de este valor con 0x59533959.
3.  Resta el valor proporcionado por \_ MSG del valor que es el resultado de la operación XOR bit a bit.

### <a name="3241-remote-indexing-service-catalog-management"></a>Administración de catálogos del servicio de indexación remota de 3.2.4.1

Cada mensaje se desencadena mediante una solicitud de la capa superior. No hay ninguna secuencia de mensajes impuesta por el cliente para las solicitudes de mensajes CISP para administrar de forma remota los catálogos, pero (con la excepción de un mensaje CPMSetCatStateIn) el servidor solo responderá correctamente si el cliente se conectó anteriormente mediante un mensaje de CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 enviar una solicitud de CPMCiStateInOut

Normalmente, el nivel superior solicita al cliente de protocolo que envíe un mensaje de CPMCiStateInOut cuando requiere información sobre los servicios de Index Server en el servidor.

Cuando se solicita el envío de este mensaje, el cliente debe hacer lo siguiente:

-   Envíe un mensaje CPMCiStateInOut como se especifica en la sección 2.2.3.1 al servidor.
-   Espere para recibir el mensaje CPMCiStateInOut del servidor, descartando de forma silenciosa el resto de mensajes.
-   Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, la estructura informativa de vuelta a la capa superior.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 enviar una solicitud de CPMSetCatStateIn

Normalmente, el nivel superior solicita al cliente de protocolo que envíe un mensaje de CPMSetCatStateIn cuando requiere información sobre un catálogo o todo el catálogo. En este mensaje, la capa más alta debe proporcionar al cliente de protocolo un valor para \_ dwNewState y, si es necesario, el nombre del catálogo.

Cuando se solicita el envío de este mensaje, el cliente debe hacer lo siguiente:

-   Envíe un mensaje CPMSetCatStateIn como se especifica en 2.2.3.2 al servidor.
-   Espere a recibir un mensaje CPMSetCatStateOut del servidor, descartando de forma silenciosa el resto de los mensajes.
-   Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, dwOldState de \_ nuevo a la capa superior.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 enviar una solicitud de CPMUpdateDocumentsIn

Normalmente, el nivel superior solicita que se envíe este mensaje cuando es necesario actualizar documentos en una ruta de acceso existente o agregar una nueva ruta de acceso al índice. Por lo tanto, la capa superior es proporcionar la ruta de acceso y el tipo de un examen, que se especifica como en la sección 2.2.3.4, donde una actualización incremental o completa está pensada para las rutas de acceso existentes, y la nueva inicialización está destinada a nuevas rutas.

Para atender la solicitud de nivel superior, el cliente debe hacer lo siguiente:

-   Envíe un mensaje CPMUpdateDocumentsIn como se especifica en la sección 2.2.3.4 al servidor.
-   Espere para recibir el mensaje de CPMUpdateDocumentsIn de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.
-   Vuelva a informar del valor del \_ campo Estado de la respuesta a la capa superior.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 enviar una solicitud de CPMForceMergeIn

Normalmente, el nivel superior solicita que se envíe este mensaje cuando es necesario mejorar el rendimiento de las consultas o forma parte del mantenimiento de los servicios de Index Server programados.

Para atender a la capa más alta, el cliente debe hacer lo siguiente:

-   Envíe el mensaje CPMForceMergeIn como se especifica en la sección 2.2.3.5 al servidor.
-   Espere para recibir un mensaje de CPMUpdateDocumentsIn de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.
-   Vuelva a informar del valor del \_ campo Estado de la respuesta a la capa superior.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2 mensajes de consulta del catálogo del servicio de indexación remota

Con la excepción de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, hay una relación uno a uno entre los mensajes de CISP y las solicitudes de nivel superior. En el caso de las dos excepciones mencionadas anteriormente, puede haber varios mensajes generados por el cliente para satisfacer los requisitos de tamaño o para recuperar una propiedad completa. El nivel superior normalmente realiza un seguimiento de toda la información específica de la consulta (por ejemplo, los identificadores de cursor abiertos, los valores válidos para los identificadores de marcador y de capítulo, los valores de WID para los valores de propiedad aplazados, etc.) y también realiza el seguimiento de si el cliente está en un estado conectado, pero el cliente no lo exige.

Con fines ilustrativos, la parte del cliente del diagrama de la sección 3 muestra esta secuencia para una consulta de servicio de indexación simple.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 enviar una solicitud de CPMConnectIn

Este mensaje suele ser la primera solicitud de la capa superior (como si el cliente no está conectado, el servidor producirá un error en la mayoría de los mensajes con la excepción de CPMSetCatStateIn). El nivel superior proporciona al cliente de protocolo la información necesaria para conectarse.

Para atender el nivel superior, el cliente debe hacer lo siguiente:

-   Rellene el mensaje con la información que el cliente de nivel superior proporcionó (consulte la sección 2.2.3.6) en \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 y aPropertySet.
-   Establezca \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet y cExtPropSet como se especifica en 2.2.3.6.
-   Establezca la suma de comprobación en el \_ campo ulChecksum.
-   Envíe el mensaje CPMConnectIn al servidor.
-   Espere para recibir un mensaje de CPMConnectOut de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.
-   Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, serverVersion de \_ nuevo a la capa superior.

Para fines informativos, se espera que las capas más altas realicen normalmente las siguientes acciones tras una conexión correcta, pero que no las aplique el cliente de CISP:

-   Usar mensajes de administración de catálogos de servicio de indexación remota para tareas administrativas
-   Use una solicitud CPMCreateQueryIn para crear una consulta de búsqueda con el fin de recuperar los resultados del catálogo.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 enviar una solicitud de CPMCreateQueryIn

La capa superior normalmente proporcionará información para la creación de la consulta una vez que el cliente del protocolo esté conectado. La capa superior proporciona al cliente un conjunto de restricciones, conjunto de columnas, reglas de ordenación y conjunto de categorización (se pueden omitir cada una de ellas), propiedades de conjunto de filas y estructura del asignador de IDENTIFICADOres de propiedad.

Cuando se recibe esta solicitud de una capa superior, el cliente debe hacer lo siguiente:

-   Prepare un CPMCreateQueryOut como se indica a continuación.
-   -   Si hay un conjunto de columnas, establezca CColumnsSetPreset en 0x01 y rellene el campo ColumnsSet.
    -   Si hay restricciones, establezca CRestrictionPresent en 0x01 y rellene el campo de restricción.
    -   Si hay un conjunto de ordenación, rellene el campo SortSet.
    -   Si hay un conjunto de categorización, establezca CSortSetPresent en 0x01 y rellene el campo CategorizationSet.
    -   Establecer el resto de campos tal como se especifica en 2.2.3.8

-   Calcula \_ el campo ulCheckSum en el encabezado.
-   Envíe el mensaje CPMCreateQueryIn al servidor.
-   Espere para recibir el mensaje CPMCreateQueryOut (vea los detalles en la sección 3.2.5.1.1) y descarte de forma silenciosa el resto de los mensajes.
-   Notifique el valor del \_ campo de estado de la respuesta y, si fue correcto, la matriz de identificadores de cursor y valores booleanos informativos (como se especifica en 2.2.3.9) de nuevo a la capa superior.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 enviar una solicitud de CPMSetBindingsIn

Normalmente, el nivel superior establecerá enlaces para cada columna que se va a devolver en las filas cuando ya tenga un identificador de cursor válido (después de recibir correctamente CPMCreateQueryOut, vea la sección 3.2.5.1.1). Se espera que el mayor proporcione una matriz de estructuras CTableColumn, como se especifica en la sección 2.2.4.31, para el campo aColumns y un identificador de cursor válido.

Cuando se recibe esta solicitud desde el nivel superior, el cliente debe hacer lo siguiente:

-   Calcule el número de estructuras CTableColumn en la matriz aColumns y establezca el campo cColumns en este valor.
-   Calcule el tamaño total en bytes de los campos cColumns y aColumns y establezca el \_ campo cbBindingDesc en este valor.
-   Establezca los campos especificados en el mensaje CPMSetBindingsIn en los valores proporcionados por el nivel de aplicación superior. Establezca el \_ campo ulChecksum en el valor calculado tal y como se especifica en la sección 3.2.5.
-   Envíe el mensaje CPMSetBindignsIn completado al servidor.
-   Espere para recibir un mensaje de CPMSetBindingsIn del servidor, descartando otros mensajes.
-   Indica el estado del \_ campo de estado de la respuesta a la capa superior.

Para fines informativos, se espera que las capas más altas pidan normalmente a un cliente que envíe un mensaje CPMGetRowsIn, pero el protocolo del servicio de indización de contenido no lo exige.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 enviar una solicitud de CPMGetRowsIn

Cuando el nivel superior está a punto de recibir información de filas, proporcionará al cliente de protocolo un identificador de cursor y de capítulo válido y proporcionará la descripción de búsqueda adecuada. Normalmente, se espera que una capa superior lo haga cuando tiene un cursor o un identificador de capítulo válido y los enlaces se han establecido con el mensaje CPMSetBindingsIn. Para tener acceso al conjunto de filas en un capítulo, el nivel superior es usar el identificador de capítulo recibido del servidor en un mensaje CPMGetRowsOut anterior.

Cuando se recibe esta solicitud desde el nivel superior, el cliente debe hacer lo siguiente:

-   Determine el valor entero sin signo que se va a especificar para el \_ campo cbReadBuffer. Para determinar este valor, el cliente debe tomar el valor máximo de lo siguiente:
-   -   1000 veces el valor del \_ campo RowsToTransfer de c.
    -   Valor de \_ cbRowWidth, redondeado al múltiplo de 512 Byte más próximo.
    -   Tome el mayor de estos dos valores, hasta el límite de 16 k.
    -   En los casos en los que una sola fila es mayor que 16 k, el servidor no puede devolver resultados a esta consulta.

Especifique una base de cliente para los datos de fila de tamaño variable en el campo espacio de direcciones de cliente en \_ ulClientBase.

*Comportamiento de Windows: para que un cliente de 32 bits se comunique con un servidor de 32 bits o un cliente de 64 bits hablando con un servidor de 64 bits, este valor se establece en una dirección de memoria del búfer de recepción en el proceso de la aplicación. Esto permite que los punteros, que se reciben en el campo Rows de CPMGetRowsOut sean punteros de memoria correctos en un proceso de aplicación cliente. De lo contrario, se establece en 0x00000000.*

-   Calcule el tamaño de la descripción de búsqueda y establézcalo en el \_ campo cbSeek.
-   Establezca el valor de cbReserved (que actuaría como desplazamiento para el inicio de filas) en el valor de \_ cbSeek más 0x14.
-   Envíe un mensaje CPMConnectIn como se especifica en 2.2.3.15 al servidor.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 enviar una solicitud de CPMFetchValueIn

Si el cliente recibe una respuesta CPMGetRowsOut del servidor con el campo de estado de la columna establecido en StatusDeferred (0x01) significa que el valor de la propiedad no se incluyó en el campo Rows del mensaje CPMGetRowsOut. En este caso, la capa más alta normalmente solicita al cliente del protocolo que recupere el valor por medio del mensaje CPMFetchValueIn y proporciona el valor PropSpec y \_ WID para una propiedad aplazada, que el cliente de protocolo debe usar en el primer mensaje de CPMFetchValueIn.

Si éste es el primer mensaje CPMFetchValueIn que el cliente ha enviado para solicitar la propiedad especificada, el cliente debe hacer lo siguiente:

-   Establezca todos los campos de un mensaje como se especifica en la sección 2.2.3.19.
-   Establezca \_ cbSoFar en 0x00000000.
-   Establecer bytes actuales recibidos en 0.
-   Envíe el mensaje CPMFetchValueIn al servidor.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 enviar una solicitud de CPMFreeCursorIn

Una vez que el nivel superior ya no usa la consulta de búsqueda, puede liberar los recursos en el servidor solicitando al cliente que envíe un mensaje de CPMFreeCursorIn.

Cuando se recibe esta solicitud, el cliente debe enviar un mensaje CPMFreeCursorIn como se especifica en 2.2.3.28 al servidor, que contiene el identificador especificado por la capa superior.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 enviar un mensaje de CPMDisconnect

Si el nivel superior no tiene más consultas para el servicio de indexación, para liberar más recursos del servidor, la aplicación puede solicitar que el cliente envíe un mensaje CPMDisconnect al servidor. Cuando se recibe esta consulta, el cliente debe enviar simplemente el mensaje como se ha solicitado. No hay ninguna respuesta a este mensaje del servidor.

### <a name="325-message-processing-and-sequencing-rules"></a>Reglas de procesamiento y secuenciación de mensajes 3.2.5

Cuando el cliente recibe una respuesta de mensaje del servidor, el cliente debe utilizar el último mensaje enviado para determinar si el mensaje recibido del servidor es el esperado por el cliente. \_Se deben omitir todos los mensajes con el campo MSG diferente del último mensaje de envío.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 recibir una respuesta CPMCreateQueryOut

Cuando el cliente recibe una respuesta del mensaje CPMCreateQueryOut desde el servidor, el cliente debe devolver el \_ Estado y, si el estado es correcto, los valores de identificador de cursor a una capa superior. Todas las acciones posteriores se encuentran hasta el nivel superior.

Como el nivel más alto es consciente de la estructura de la consulta, siempre se espera que se devuelva el número de identificadores de cursor correctos en el mensaje CPMCreateOueryOut. Los identificadores de cursor se devuelven en el orden siguiente: el primer identificador está en el conjunto de filas sin capítulo, el segundo es el primer conjunto de filas de capítulo (que es la agrupación de los resultados en función de la primera categoría especificada en el campo CategorizationSet del mensaje CPMCreateQueryIn).

Para fines informativos, se espera que las capas superiores puedan realizar las siguientes acciones, pero el cliente de CISP no las aplica:

-   Use CPMSetBindingsIn para establecer enlaces para columnas individuales y realizar las siguientes acciones en la ruta de acceso de la consulta.
-   Use CPMGetQueryStatusIn para comprobar el progreso de la ejecución de una consulta.
-   Use CPMRatioFinishedIn para solicitar el porcentaje de finalización de la consulta.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 recibir una respuesta CPMGetRowsOut

Cuando el cliente recibe una respuesta del mensaje CPMGetRowsOut desde el servidor, el cliente debe hacer lo siguiente:

-   Compruebe si el \_ campo de estado del encabezado indica éxito o error.
-   Si el \_ valor de estado es \_ búfer de estado \_ demasiado \_ pequeño (0xC0000023), el cliente debe comprobar el último mensaje enviado. Si no contiene un mensaje CPMGetRowsIn, el mensaje recibido debe omitirse de forma silenciosa. De lo contrario, el cliente debe enviar al servidor un nuevo mensaje CPMGetRowsIn con todos los campos idénticos al almacenado, con la excepción de que el \_ CBREADBUFFER debe aumentarse en 512 (pero no mayor que 0x4000). Si el \_ Estado es el búfer de estado \_ \_ demasiado \_ pequeño (0XC0000023) y el último mensaje enviado ya tiene \_ CBREADBUFFER igual a 0x4000 cliente debe notificar el error hasta el nivel superior.
-   Si el \_ valor de estado es cualquier otro valor de error, el cliente debe indicar el error hasta el nivel superior.
-   Si el \_ valor de estado indica que la operación se ha realizado correctamente, los resultados se deben indicar hasta el nivel superior que solicita la información, y las acciones adicionales están en el nivel más alto.

Para fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones, pero el cliente del protocolo del servicio de indización de contenido no las aplica:

-   Si los valores de las filas representan los identificadores de documento, el capítulo o los marcadores de marcador, el nivel superior normalmente los almacenará para su uso en operaciones posteriores que impliquen identificadores de documento, capítulos o identificadores de marcador válidos.
-   El nivel superior normalmente almacenará o mostrará o utilizará los datos de los valores de fila.
-   En el caso de los valores que se marcaron como el nivel más alto aplazado, capturará el valor mediante mensajes CPMFetchValueIn.
-   La descripción de la búsqueda se devuelve también al nivel superior y puede ser reutilizada o examinada por el nivel superior.

Para fines informativos, si la capa superior solicitó controladores a capítulos y marcadores que se recibieron en las filas, puede hacer lo siguiente:

-   Use CPMGetQueryStatusExIn para comprobar el progreso de la ejecución de una consulta, así como información de estado adicional, como el número de documentos filtrados, los documentos que quedan por filtrar, la proporción de documentos procesados por la consulta, el número total de filas de la consulta y la posición del marcador en el conjunto de filas.
-   Use CPMGetNotify para solicitar que el servidor notifique al cliente los cambios del conjunto de filas.
-   Use CPMGetApproximatePositionIn para solicitar la posición aproximada de un marcador en un capítulo.
-   Use CPMCompareBmkIn para solicitar una comparación de dos marcadores en un capítulo.
-   Use CPMRestartPositionIn para que el servidor cambie la ubicación del cursor al inicio del conjunto de filas.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 recibir una respuesta CPMFetchValueOut

Cuando el cliente recibe una respuesta del mensaje CPMGetRowsOut desde el servidor, el cliente debe hacer lo siguiente:

-   Compruebe si el \_ campo de estado del encabezado indica éxito o error. En caso de error, notifique a la capa superior. De lo contrario, continúe a continuación.
-   Compruebe \_ fValueExist y, si está establecido en 0x00000000, notifique a la capa superior que no se encontró el valor.
-   De lo contrario, anexe \_ cbValue bytes de vValue al valor de propiedad actual.
-   Si \_ \_ fMoreExists se establece en 0x00000001, se incrementan los \_ bytes actuales recibidos por \_ cbValue y se envía un mensaje de CPMFetchValueIn al servidor, estableciendo \_ CbSoFar en el valor de bytes actuales recibidos, \_ cbPropSpec en cero y \_ cbChunk en el tamaño de búfer que desea la capa superior.
-   Si \_ fMoreExists se establece en 0x00000000, indique el valor de propiedad del valor de propiedad actual a la capa superior.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 recibir una respuesta CPMFreeCursorOut

Cuando el cliente recibe una respuesta de mensaje CPMFreeCursorOut correcta del servidor, el cliente debe devolver el \_ valor de cCursorsRemaining a la capa superior.

La siguiente información se proporciona solo con fines informativos y no la aplica el cliente de CISP. Se espera que el nivel superior realice un seguimiento de los identificadores de cursor y no use los que ya se han liberado. Una vez que el número de \_ cCursorsRemaining es igual a 0x00000000, el nivel superior puede utilizar la conexión para especificar otra consulta (mediante un mensaje CPMCreateQueryIn).

### <a name="326-timer-events"></a>Eventos de temporizador de 3.2.6 procedimientos

Ninguno.

### <a name="327-other-local-events"></a>3.2.7 otros eventos locales

Ninguno.

## <a name="4-protocol-examples"></a>4 Ejemplos de protocolo

-   [4,1 ejemplo 1](#41-example-1)
-   [ejemplo 2 de 4,2](#42-example-2)

### <a name="41-example-1"></a>4,1 ejemplo 1

En el ejemplo siguiente, se considera un escenario en el que el usuario JOHN del equipo A desea obtener los tamaños de los archivos que contienen la palabra "Microsoft" del conjunto de documentos almacenados en el servidor X en el sistema de catálogos. Supongamos que el equipo A ejecuta un sistema operativo Windows XP de 32 bits y el equipo X está ejecutando un sistema operativo Windows Server 2003 de 32 bits.

1.  El usuario inicia una aplicación de búsqueda y entra en la consulta de búsqueda. A su vez, la aplicación pasa la consulta de búsqueda al cliente del protocolo.
2.  El cliente de Protocolo establece una conexión con el servidor de indexación X. El cliente de protocolo usa el \\ elemento de CI de canalización con nombre \\ \_ SKADS para conectarse al servidor X a través de SMB.
3.  A continuación, el cliente de protocolo prepara un mensaje CPMConnectIn con los valores siguientes:

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectIn.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada como se especifica en la sección 3.2.4.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ iClientVersion** se establece en 0x00000008, lo que indica que el servidor va a validar el campo de suma de comprobación.
    -   **\_ fClientIsRemote** se establece en 0x00000001, lo que indica que el servidor es un servidor remoto.
    -   **\_ cbBlob1** se establece en el tamaño, en bytes, de los campos cPropSet, PropertySet1 y PropertySet2 combinados.
    -   **\_ cbBlob2** se establece en 0x00000004 (lo que significa que no hay conjuntos de propiedades adicionales).
    -   **MachineName** se establece en.
    -   **Username** se establece en John.
    -   **cPropSets** se establece en 0x00000002.
    -   El campo **PropertySet1** es de tipo CDbPropSet. La estructura CDbPropSet que consta del campo PropertySet1 se rellena de la siguiente manera:
        -   El campo **GuidPropSet** está establecido en A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).
        -   el campo **cProperties** se establece en 0x00000004.
        -   el campo **aProps** es una matriz de estructuras CDbProp.

            Para el **elemento \[ aProps \] 0** :

            -   **PropId** se establece en 0X00000002 (DBPROP \_ CI \_ Catalog \_ Name).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS** se establece en 0x00000000.
            -   Para el elemento **colid** :
                -   **eKind** está establecido en 0X00000001 (DBKIND \_ GUID \_ PROPID)
                -   **GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el elemento **vValue** :
                -   **vType** se establece en 0X001F (VT \_ LPWStr).
                -   **vValue** se establece en "System", el nombre del catálogo deseado.

            Para el **elemento \[ aProps \] 1** :

            -   **PropId** se establece en 0X00000007 (DBPROP \_ CI \_ query \_ Type)
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS** es Set to0x00000000.
            -   Para el elemento **colid** :
                -   **eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el elemento **vValue** :
                -   **vType** se establece en 0X0003 (VT \_ I4).
                -   **vValue** se establece en 0X00000000 (CiNormal), lo que significa que es una consulta normal.

            Para el **elemento \[ aProps \] 2** :

            -   **PropId** se establece en 0X00000004 (DBPROP \_ CI \_ Scope \_ Flags).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS** se establece en 0x00000000.
            -   Para el elemento **colid** :
                -   **eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el elemento **vValue** :
                -   **vType**: 0X1003 (VT \_ Vector \| VT \_ I4)
                -   **vValue**: 0x00000001/0x00000001 (un elemento con el valor 1), lo que significa que las subcarpetas de búsqueda

            Para el **elemento \[ aProps \] 3** :

            -   **PropId**: 0X00000003 (DBPROP \_ CI \_ incluir \_ ámbitos)
            -   **DBPROPOPTIONS**: 0x0000000
            -   **DBPROPSTATUS**: 0x00000000
            -   Para el elemento **colid** :
                -   **eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.
                -   **ulID** está establecido en 0x00000000
            -   Para el elemento **vValue** :
                -   **vType** se establece en 0X101F (VT \_ Vector \| VT \_ LPWStr).
                -   **vValue** se establece en 0x00000001/0x00000002/" \\ " (un elemento con una cadena terminada en NULL de 2 caracteres), es decir, el ámbito raíz.

    -   El campo **PropertySet2** es de tipo CDbPropSet.

        La estructura CDbPropSet que consta del campo PropertySet1 se rellena de la siguiente manera:

        -   **GuidPropSet** se establece en AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).
        -   el campo **cProperties** está establecido en 0x00000001.
        -   El campo **aProps** es una matriz de estructuras CDbProp.

            Para el **elemento \[ aProps \] 0** :

            -   **PropId** se establece en 0X00000002 (DBPROP \_ Machine).
            -   **DBPROPOPTIONS** se establece en 0x0000000.
            -   **DBPROPSTATUS** se establece en 0x00000000.
            -   Para el elemento **colid** :
                -   **eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.
                -   **ulID** se establece en 0x00000000.
            -   Para el elemento **vValue** :
                -   **vType**: 0X0008 (VT \_ BSTR)
                -   **vValue**: 0x04/"x" (4 bytes/cadena Unicode terminada en null), lo que significa "x": el nombre de un servidor.

    -   el campo **cExtPropSet** está establecido en 0x00000000.
    -   la matriz **aPropertySets** no existe.
    -   Se rellenan varios campos de relleno según sea necesario. El mensaje se envía al servidor.

4.  El servidor comprueba que **\_ ulChecksum** es correcto, comprueba que el usuario está autorizado para hacer esta solicitud y responde con un mensaje CPMConnectOut.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectOut.
    -   **\_ status** se establece en 0x0000000, lo que indica que se ha realizado correctamente.
    -   **\_ ulChecksum** se establece en 0.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   el campo **\_ serverVersion** está establecido en 0x00000007 (32 de windows XP o 32 bits Windows Server 2003).
    -   los campos **\_ reservados** se rellenan con datos arbitrarios.

5.  El cliente prepara un mensaje CPMCreateQueryIn.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryIn.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada según 3.2.5.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   El campo **tamaño** se establece en el tamaño del resto del mensaje.
    -   El campo **CColumnSetPresent** se establece en 0x01.
    -   El campo **ColumnSet** es de tipo CColumnSet. La estructura CColumnSet que consta de este campo se establece de la manera siguiente:
        -   el campo **\_ Count** se establece en 0x00000001, lo que indica que se devuelve una columna.
        -   la matriz de **índices** es 0x00000000 que indica la primera entrada en \_ aPropSpec.
    -   El campo **CRestrictionPresent** se establece en 0x01, lo que indica que el campo **Restriction** está presente.
    -   El campo de **restricción** es de tipo CRestriction y está establecido en:
        -   **\_ ulType** se establece en 0x00000004 (RTContent).
        -   **\_ Weight** se establece en 0x00000000.
    -   El resto del campo contiene una estructura CContentRestriction:
        -   La **\_ propiedad** se establece en GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13 que representa el cuerpo del documento.
        -   **\_ CC** está establecido en 0x00000009.
        -   **\_ pwcsphrase** se establece en la cadena "Microsoft".
        -   **\_ LCID** se establece en 0Xc0a (para inglés).
        -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).
    -   **CSortPresent** está establecido en 0x00.
    -   **CCategorizationSetPresent** está establecido en 0x00.
    -   **RowSetProperties** se establece de la siguiente manera:
        -   **\_ uBooleanOptions** se establece en 0x00000001 (secuencial).
        -   **\_ ulMaxOpenRows** se establece en 0x00000000.
        -   **\_ ulMemoryUsage** se establece en 0x00000000.
        -   \_**cMaxResults** se establece en 0x00000100 (devuelve como máximo 256 filas).
        -   **\_ cCmdTimeOut** se establece en 0x00000000 (nunca se agota el tiempo de espera).
    -   **PidMapper** se establece en:
        -   **\_ Count** se establece en 0x00000001.
        -   **\_ aPropSpec** se establece en GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0X00000001 (para PRSPEC \_ PROPID)/0x0000000c, que representa la propiedad de tamaño de archivo de Windows.

6.  El servidor lo procesa y responde con un mensaje CPMCreateQueryOut.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryOut.
    -   **\_ status** se establece en Success.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ fTrueSeqeuntial** se establece en 0x00000000, lo que indica que la consulta puede utilizar un índice.
    -   **\_ fWorkIdUnique** se establece en 0x00000001.
    -   La matriz **aCursors** contiene un solo elemento, que representa un identificador de cursor para esta consulta. El valor depende del estado del servidor. Supongamos que el valor devuelto es 0xAAAAAAAA.

7.  El cliente emite un mensaje de solicitud CPMSetBindingsIn para definir el formato de una fila.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000D0, lo que indica que se trata de un mensaje CPMSetBindingsIn.
    -   **\_ status** se establece en Success.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ hCursor** se establece en 0xAAAAAAAA.
    -   **\_ cbRow** se establece en 0x10 (lo suficientemente grande como para ajustarse a las columnas).
    -   **\_ cbBindingDesc** se establece en el tamaño de los campos **\_ cColumns** y **\_ aColumns** combinados.
    -   **\_ cColumns** se establece en 0x00000001.
    -   la matriz **\_ aColumns** se establece para que contenga una estructura CTableColumn que contenga:
    -   -   **\_ PropSpec** se establece en GUID b725f130-47ef-101A-A5-F1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x0000000c, que representa la propiedad de tamaño de archivo de Windows.
        -   **\_ vType** se establece en 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed** se establece en 0x01 (columna transferida en la fila).
        -   **\_ ValueOffset** se establece en 0x0002 (al principio de la fila).
        -   El **\_ valor** de se establece en 0x08 (tamaño de una \_ UI8 de VT).
        -   **\_ StatusUsed** se establece en 0x01.
        -   **\_ StatusOffset** está establecido en 0x0A.
        -   **\_ LengthUsed** está establecido en 0x00.

8.  El servidor lo procesa y responde con un mensaje CPMSetBindingsIn.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000D0.
    -   **\_ status** se establece en Success.
    -   **\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).
    -   **\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).

9.  El cliente emite un mensaje de solicitud CPMGetRowsIn. Supongamos que el cliente está preparado para aceptar 100 filas en este momento y los desea en orden ascendente.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsIn.
    -   **\_ status** se establece en 0x00000000
    -   **\_ ulChecksum** contiene la suma de comprobación, calculada según la sección 0.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ hCursor** se establece en 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** se establece en 0x00000064.
    -   **\_ cRowWidth** se establece en 0x00000010 (de los enlaces).
    -   **\_ cbSeek** se establece en 0x14, que es el tamaño de los campos ETYPE, \_ chapt y CRowSeekNext combinados.
    -   **\_ cbReserved** se establece en 0x18 (0x14 más \_ cbSeek).
    -   **\_ cbReadBuffer** se establece en 0x800 (0x64 \* 0x10 redondeado hacia arriba al siguiente múltiplo de 0x200).
    -   **\_ ulClientBase** se establece en 0x00000000.
    -   **\_ fBwdfetch** se establece en 0x00000000, lo que indica que las filas se van a capturar en orden hacia delante.
    -   **ETYPE** se establece en 0x0000001, lo que indica que el cliente desea filas siguientes.
    -   **\_ chapt** está establecido en 0 (no es un resultado en el capítulo).
    -   **SeekDescription** se establece en CRowSeekNext. La estructura CRowSeekNext contiene los siguientes valores:
        -   **CiTblChapt** se establece en 0x00000000.
        -   **\_ hRegion** se establece en 0x00000000.
        -   **\_ cSkip** se establece en 0, lo que indica que el cliente no desea omitir filas.

10. El servidor lo procesa y responde con un mensaje CPMGetRowsOut. Supongamos que el servidor encontró 100 documentos que contienen la palabra "Microsoft".

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsOut.
    -   **\_ status** se establece en Success.
    -   **\_ ulChecksum** se establece en 0x00000000.
    -   **\_ ulReserved2** se establece en 0x00000000.

    El cuerpo del mensaje se rellena de la siguiente manera:

    -   **\_ CRowsReturned** se establece en 0x00000064.
    -   **ETYPE** se establece en 0x00000001.
    -   **\_ chapt** está establecido en 0x00000000 (no en un resultado en el capítulo).
    -   **SeekDescription** contiene una estructura CRowSeekNext, que se rellena de la siguiente manera:
        -   **CiTblChapt** se establece en 0x00000000.
        -   **\_ hRegion** se establece en 0x00000000.
        -   **\_ cSkip** se establece en 0, lo que indica que el cliente no desea omitir filas.
    -   **Rows** contiene el tamaño de los documentos 100 que contienen la palabra "Microsoft". Dado que se trata de datos de tamaño fijo, simplemente está estructurado como una lista de enteros de 8 bytes sin signo de 100.

11. El cliente envía un mensaje CPMDisconnect para finalizar la conexión.

    El encabezado del mensaje se rellena de la siguiente manera:

    -   **\_ MSG** se establece en 0x000000C9, lo que indica que se trata de un mensaje CPMDisconnect.
    -   **\_ status** se establece en 0x00000000.
    -   **\_ ulChecksum** se establece en 0x00000000.

12. El servidor procesa el mensaje y quita todo el estado del cliente.

### <a name="42-example-2"></a>ejemplo 2 de 4,2

En el ejemplo anterior, la consulta era bastante sencilla. Ahora vamos a considerar una consulta ligeramente más compleja. Supongamos que el usuario desea recuperar el tamaño de los documentos que contienen las siguientes palabras: "Microsoft" y "Office". Esto se especifica cambiando el campo de restricción incluido en el mensaje CPMCreateQueryIn enviado en el paso 5 de la siguiente manera:

El campo de **restricción** es de tipo CRestriction y se establece en:

-   -   **\_ ulType** se establece en 0x00000004 (RTAnd).
    -   **\_ Weight** se establece en 0x00000000.

El resto del campo contiene una estructura CNodeRestriction:

-   -   **\_ cNode** se establece en 0x00000002, lo que indica que hay dos nodos en la matriz de nodos.
    -   El campo **\_ panode** es una matriz de dos estructuras CRestriction.

        el **\_ nodo \[ 0 \]** contiene:

        -   -   **\_ ulType** se establece en 0x00000004 (RTContent).
            -   **\_ Weight** se establece en 0x00000000.
            -   El resto del campo contiene una estructura CContentRestriction:
                -   La **\_ propiedad** se establece en GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13.
                -   **\_ CC** está establecido en 0x00000009.
                -   **\_ pwcsphrase** se establece en la cadena "Microsoft".
                -   **\_ LCID** se establece en 0Xc0a (para inglés).
                -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).

        el **\_ nodo \[ 1 \]** contiene:

        -   -   **\_ ulType** se establece en 0x00000004 (RTContent).
            -   **\_ Weight** se establece en 0x00000000.
            -   El resto del campo contiene una estructura CContentRestriction:
                -   La **\_ propiedad** se establece en GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13.
                -   **\_ CC** está establecido en 0x00000006.
                -   **\_ pwcsphrase** se establece en la cadena "Office".
                -   **\_ LCID** se establece en 0Xc0a (para inglés).
                -   **\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).

## <a name="5-security"></a>5 Seguridad

### <a name="51-security-considerations-for-implementers"></a>5.1 Consideraciones de seguridad para los implementadores

Las implementaciones de indexación que indexan contenido seguro deben considerar el uso del contexto de usuario proporcionado por \[ MS SMB MS-SMB \] para recortar los resultados de la búsqueda y devolver solo aquellos accesibles para el autor de la llamada.

### <a name="52-index-of-security-parameters"></a>5.2 Índice de parámetros de seguridad



| Parámetro de seguridad  | Sección |
|---------------------|---------|
| Nivel de suplantación | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 índice de comportamiento específico de la versión



| Comportamiento específico de la versión                                                                         | Sección   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista. | 1.3.2     | X            | X          | X                   |
| Las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB                                  | 1.4       | X            | X          | X                   |
| Valores de NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| El cliente establece el \_ campo de estado en cada encabezado de mensaje.                                        | 2.2.2     | X            | X          | X                   |
| el valor de cPendingScans suele ser cero                                                               | 2.2.3.1   | X            | X          | X                   |
| valor iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_valor cbChunk                                                                                   | 2.2.3.19  | X            | X          | X                   |
| direcciones de memoria de 32 bits y de 64 bits                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





