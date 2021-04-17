---
description: Los nombres y descripciones de todos los objetos de rendimiento y sus contadores se almacenan en el registro.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Adición de nombres y descripciones de contadores al registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667352"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Adición de nombres y descripciones de contadores al registro

> [!IMPORTANT]
> Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método.

Los nombres y descripciones de todos los objetos de rendimiento V1 y sus contadores deben estar instalados en el sistema. Para almacenar los nombres y las descripciones de los objetos y contadores de su [proveedor v1](providing-counter-data.md):

- [Cree un archivo de encabezado. h](#creating-a-symbolic-constants-h-file) que contenga las constantes simbólicas de los desplazamientos de los objetos y contadores.
- [Cree una inicialización (. INI)](#creating-an-initialization-ini-file) que contiene las cadenas.
- Al instalar el componente, [ejecute la herramienta **LODCTR**](#running-the-lodctr-tool) para instalar los nombres y las descripciones en el registro.
- Al desinstalar el componente, ejecute la herramienta Unlodctr para quitar los nombres y las descripciones del registro.

## <a name="creating-a-symbolic-constants-h-file"></a>Crear un archivo de constantes simbólicas (. h)

Cree un archivo de encabezado. h que defina constantes (macros) para los desplazamientos a los objetos y contadores que proporciona el proveedor. El encabezado. h se usa como entrada para **LODCTR** durante la instalación del proveedor y el código de C/C++ del proveedor también puede utilizarlo.

Los valores constantes deben ser consecutivos, incluso números que empiezan por cero. Agrupe las constantes por objetos (es decir, inicie cada grupo con el desplazamiento del objeto y, a continuación, siga con los desplazamientos de los contadores para ese objeto).

Las constantes del encabezado determinan el orden en que se agregan los contadores al nombre y al texto de ayuda del registro. El proveedor utiliza los desplazamientos para determinar qué objeto se está consultando y los valores de índice que se van a utilizar al devolver los datos. Para obtener más información, consulte [implementación de OpenPerformanceData](implementing-openperformancedata.md).

A continuación se muestra un ejemplo de un archivo de constante simbólica, denominado contraoffsets. h, que se usa en el ejemplo de [creación de una DLL de extensión de rendimiento](creating-a-performance-extension-dll.md) .

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Crear una inicialización (. INI)

La inicialización (. INI) contiene el nombre y las cadenas de ayuda de cada objeto y contador definido en el archivo de símbolos. El. El archivo INI se usa como entrada para **LODCTR** durante la instalación del proveedor.

El. El archivo INI se debe codificar como UTF-16LE (con marca de orden de bytes) y debe tener las siguientes secciones y claves:

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>sección [info]

La `[info]` sección contiene información general sobre el proveedor. Las claves de sección se definen de la siguiente manera:

|Clave|Descripción
|---|-----------
|**DriverName**| Especifique el nombre de la clave de rendimiento del proveedor que se encuentra en el registro, en la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` clave. Para obtener información sobre la creación de esta clave, consulte [crear la clave de rendimiento de la aplicación](creating-the-applications-performance-key.md).
|**SymbolFile**| Especifique el archivo de encabezado. h que contiene los valores simbólicos de los objetos y contadores del proveedor. Durante la instalación (al invocar **LODCTR**), el archivo de encabezado debe estar en el mismo directorio que. Archivo INI.
|**Confiar**| Si incluye esta clave en la `[info]` sección, **LODCTR** agregará un valor del registro de código de validación de biblioteca a su clave de rendimiento con una firma binaria de la dll de rendimiento. Cuando PERFLIB llama a la DLL, compara la firma con el archivo DLL para determinar si se ha modificado el archivo DLL. Se omite el valor de la clave de **confianza** .

Las `DriverName` `SymbolFile` claves y son necesarias.

### <a name="objects-section"></a>sección [objetos]

En la `[objects]` sección se proporciona una lista de los objetos de rendimiento que admite el proveedor. Se utiliza para determinar si cada símbolo de la `[text]` sección hace referencia a un objeto o a un contador.

Para cada objeto (CounterSet) admitido por el proveedor, agregue una clave denominada `<symbol>_<langid>_NAME=` a la `[objects]` sección, donde `<symbol>` es el nombre del objeto y `<langid>` es el identificador de idioma de uno de los idiomas admitidos. Se omite el valor.

> [!IMPORTANT]
> La `[objects]` sección mejora el rendimiento del sistema. Aunque la sección objetos es opcional, siempre debe incluir esta sección en su. Archivo INI. Si incluye esta sección, solo se llama a la DLL de rendimiento si admite el objeto solicitado. Si no incluye la sección objetos, se llama a la DLL para cada consulta, ya que el sistema no sabe qué objetos admite el proveedor. Si no se incluye la sección Object, **LODCTR** genera un mensaje en el registro de eventos de la aplicación que indica que el objeto. El archivo INI no contiene una sección de objetos. El identificador de evento de este mensaje es 2000.

### <a name="languages-section"></a>sección [Languages]

`[languages]`En esta sección se proporciona una lista de los identificadores de idioma de cada lenguaje para los que el proveedor proporciona cadenas de nombre y ayuda. Todos los proveedores deben admitir `009` (Inglés).

Para cada idioma admitido, agregue una clave denominada `<langid>=` . El valor se omite, pero para fines de documentación el valor se establece normalmente en el nombre del idioma correspondiente, por ejemplo, `009=English` .

Para la mayoría de los lenguajes, debe usar el identificador de idioma principal. La lista completa de identificadores de idioma está en el archivo de encabezado Winnt. h, bajo el encabezado "ID. de idioma principal". Convierta el valor que se encuentra en Winnt. h en una secuencia de 3 dígitos hexadecimales quitando el `0x` prefijo y agregando los `0` dígitos iniciales hasta que la secuencia tenga 3 dígitos de longitud. Por ejemplo, para especificar cadenas en inglés (0x9), use 009. Para especificar cadenas italianas (0x10), use 010.

Los idiomas chino y Portugués requieren los identificadores principal y de subidioma. Use 404, 804, 416 o 816 en lugar de 004 o 016.

### <a name="text-section"></a>[texto] sección

`[text]`En la sección se proporcionan el nombre y las cadenas de ayuda de los objetos y contadores.

Para cada objeto o contador, y para cada idioma admitido, debe proporcionar una clave de nombre (que contenga el nombre o la cadena de título para el objeto o el contador) y, opcionalmente, puede proporcionar una clave de ayuda (que contiene la descripción o la cadena de explicación del objeto o contador). Las claves deben denominarse `<symbol>_<langid>_NAME` y `<symbol>_<langid>_HELP` , donde `<symbol>` es la constante simbólica del objeto o contador (tal y como se define en el archivo. h constante simbólico) y `<langid>` es el identificador de idioma que se usa para esta cadena.

Por ejemplo, las cadenas en inglés para un contador con símbolo `MY_COUNTER` se especifican como:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Las teclas de texto pueden aparecer en cualquier orden. Las cadenas de texto no deben contener caracteres de formato, como tabulaciones.

### <a name="example-ini-file"></a>Archivo INI de ejemplo

A continuación se muestra un ejemplo de un archivo de inicialización que se usa en el ejemplo de [creación de un archivo dll de extensión de rendimiento](creating-a-performance-extension-dll.md) .

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Ejecutar la herramienta LODCTR

Para cargar los nombres y las cadenas de ayuda definidas en su. Archivo INI (durante la instalación del proveedor), ejecute la herramienta **LODCTR** desde la carpeta que contiene el. Archivo INI y archivo de encabezado. La herramienta se incluye con el equipo. Debe ejecutar **LODCTR** con privilegios elevados. El parámetro de **LODCTR** es la ruta de acceso a. Archivo INI. Por ejemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Para descargar los nombres y las cadenas de ayuda (durante la desinstalación), ejecute la herramienta **Unlodctr** . Debe ejecutar **Unlodctr** con privilegios elevados. El parámetro para **Unlodctr** es el drivername del proveedor (el nombre de la clave de rendimiento del proveedor). Por ejemplo, `unlodctr "MyProvider"`.

Antes de ejecutar **LODCTR**, asegúrese de que la aplicación tiene una entrada en la clave **servicios** . Para obtener más información, consulte [crear la clave de rendimiento de la aplicación](creating-the-applications-performance-key.md). Si la clave no existe, **LODCTR** no actualizará el registro con sus nombres y descripciones.

Como alternativa a ejecutar **LODCTR**, puede llamar a [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido en Loadperf. h) desde el programa de instalación para cargar las descripciones de los nombres de los contadores. Después, puede llamar a [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante la desinstalación.

La utilidad **LODCTR** copia las cadenas de. En los **contadores** y los valores del registro de **ayuda** en las subclaves del lenguaje adecuado. Si la subclave del lenguaje correspondiente no existe, no se copian las cadenas para ese idioma. La utilidad también actualiza el **último contador** y el último valor de la **ayuda** . Los nombres y descripciones de los contadores de rendimiento se almacenan en la siguiente ubicación del registro.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Además de agregar valores en la clave **Perflib** , la herramienta **LODCTR** también agrega los siguientes valores al nodo **servicios** de la aplicación. En la mayoría de los casos, la aplicación y el proveedor tendrán una relación uno a uno; sin embargo, es posible que un proveedor proporcione datos de contador para varias aplicaciones, por lo que la clave se basa en la aplicación y no en el proveedor.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
