---
description: Los nombres y descripciones de todos los objetos de rendimiento y sus contadores se almacenan en el Registro.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Adición de nombres y descripciones de contadores al registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169157"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Adición de nombres y descripciones de contadores al registro

> [!IMPORTANT]
> Debido a limitaciones significativas de rendimiento y confiabilidad, el método para proporcionar datos de contadores de rendimiento que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en Proporcionar datos de contador mediante la versión [2.0 para](providing-counter-data-using-version-2-0.md) crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método.

Los nombres y descripciones de todos los objetos de rendimiento V1 y sus contadores deben estar instalados en el sistema. Para almacenar nombres y descripciones de los objetos y contadores del [proveedor V1:](providing-counter-data.md)

- [Cree un archivo de encabezado .h](#creating-a-symbolic-constants-h-file) que contenga las constantes simbólicas para los desplazamientos de los objetos y contadores.
- [Cree un archivo de inicialización (.INI)](#creating-an-initialization-ini-file) que contenga las cadenas.
- Al instalar el componente, [ejecute la herramienta **lodctr**](#running-the-lodctr-tool) para instalar los nombres y descripciones en el registro.
- Al desinstalar el componente, ejecute la herramienta unlodctr para quitar los nombres y descripciones del Registro.

## <a name="creating-a-symbolic-constants-h-file"></a>Creación de un archivo de constantes simbólicas (.h)

Cree un archivo de encabezado .h que defina constantes (macros) para los desplazamientos a los objetos y contadores que proporciona el proveedor. El encabezado .h se usa como entrada para **lodctr** durante la instalación del proveedor y también se puede usar en el código de C/C++ del proveedor.

Los valores constantes deben ser consecutivos, incluso números que empiezan por cero. Agrupa las constantes por objetos (es decir, inicia cada grupo con el desplazamiento del objeto y, a continuación, sigue con los desplazamientos de los contadores de ese objeto).

Las constantes del encabezado determinan el orden en que se agregan los contadores al nombre y al texto de ayuda en el Registro. El proveedor usa los desplazamientos para determinar qué objeto se consulta y los valores de índice que se usarán al devolver los datos. Para obtener más información, [vea Implementar OpenPerformanceData.](implementing-openperformancedata.md)

A continuación se muestra un ejemplo de un archivo constante simbólico, denominado CounterOffsets.h, que se usa en el ejemplo crear un [archivo DLL de extensión de](creating-a-performance-extension-dll.md) rendimiento.

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

## <a name="creating-an-initialization-ini-file"></a>Creación de un archivo de inicialización (.INI)

El archivo de inicialización (.INI) contiene el nombre y las cadenas de ayuda para cada objeto y contador definidos en el archivo de símbolos. El .INI se usa como entrada para **lodctr** durante la instalación del proveedor.

El .INI debe codificarse como UTF-16LE (con marca de orden de bytes) y debe tener las siguientes secciones y claves:

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

### <a name="info-section"></a>[info] sección

La `[info]` sección contiene información general sobre el proveedor. Las claves de sección se definen de la siguiente manera:

|Clave|Descripción
|---|-----------
|**DriverName**| Especifique el nombre de la clave de rendimiento del proveedor ubicada en el Registro bajo la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` clave. Para obtener información sobre cómo crear esta clave, vea [Creating the Application's Performance Key](creating-the-applications-performance-key.md).
|**SymbolFile**| Especifique el archivo de encabezado .h que contiene valores simbólicos de los objetos y contadores del proveedor. Durante la instalación (al invocar **lodctr**), el archivo de encabezado debe estar en el mismo directorio que el .INI archivo.
|**Confianza**| Si incluye esta clave en la sección `[info]` , **lodctr** agregará un valor del Registro de código de validación de biblioteca a la clave de rendimiento con una firma binaria del archivo DLL de rendimiento. Cuando PERFLIB llama al archivo DLL, compara la firma con el archivo DLL para determinar si el archivo DLL se ha modificado. Se omite el **valor de la** clave de confianza.

Las `DriverName` claves y son `SymbolFile` necesarias.

### <a name="objects-section"></a>Sección [objects]

En `[objects]` la sección se proporciona una lista de los objetos de rendimiento que admite el proveedor. Se usa para determinar si cada símbolo de la `[text]` sección hace referencia a un objeto o a un contador.

Para cada objeto (contraconjunto) admitido por el proveedor, agregue una clave denominada a la sección , donde es el nombre del objeto y es el identificador de idioma de uno de los `<symbol>_<langid>_NAME=` `[objects]` `<symbol>` `<langid>` idiomas admitidos. El valor se omite.

> [!IMPORTANT]
> La `[objects]` sección mejora el rendimiento del sistema. Aunque la sección objects es opcional, siempre debe incluir esta sección en el .INI archivo. Si incluye esta sección, solo se llama al archivo DLL de rendimiento si admite el objeto solicitado. Si no incluye la sección de objetos, se llama al archivo DLL para cada consulta porque el sistema no sabe qué objetos admite el proveedor. Si no se incluye la sección de objeto, **lodctr** genera un mensaje en el registro de eventos de la aplicación que indica que el archivo .INI no contenía una sección de objetos. El identificador de evento de este mensaje es 2000.

### <a name="languages-section"></a>[idiomas] sección

En la sección se proporciona una lista de los identificadores de idioma de cada idioma para el que el proveedor proporciona el nombre `[languages]` y las cadenas de ayuda. Todos los proveedores deben admitir `009` (inglés).

Para cada idioma admitido, agregue una clave denominada `<langid>=` . El valor se omite, pero para fines de documentación, el valor normalmente se establece en el nombre del idioma correspondiente, por ejemplo, `009=English` .

Para la mayoría de los idiomas, debe usar el identificador de idioma principal. La lista completa de identificadores de idioma se encuentra en el archivo de encabezado Winnt.h, bajo el encabezado "Primary Language Ids" (Identificadores de idioma principal). Convierta el valor encontrado en Winnt.h en una secuencia de 3 dígitos hexadecimales quitando el prefijo y agregando dígitos iniciales hasta que la secuencia tiene 3 dígitos `0x` `0` de longitud. Por ejemplo, para especificar cadenas en inglés (0x9), use 009. Para especificar cadenas en italiano (0x10), use 010.

Los idiomas chino y portugués requieren los identificadores principal y subidioma. Use 404, 804, 416 o 816 en lugar de 004 o 016.

### <a name="text-section"></a>[texto] sección

La `[text]` sección proporciona el nombre y las cadenas de ayuda para los objetos y contadores.

Para cada objeto o contador, y para cada idioma admitido, debe proporcionar una clave NAME (que contiene el nombre o la cadena de título para el objeto o contador) y, opcionalmente, puede proporcionar una clave HELP (que contiene la cadena de descripción o explicación del objeto o contador). Las claves deben tener el nombre y , donde es la constante simbólica para el objeto o contador (como se define en el archivo .h de constante simbólica) y es el identificador de lenguaje utilizado para `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` esta `<symbol>` `<langid>` cadena.

Por ejemplo, las cadenas en inglés para un contador con símbolo `MY_COUNTER` se especificarían como:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Las claves de texto pueden aparecer en cualquier orden. Las cadenas de texto no deben contener caracteres de formato, como tabulaciones.

### <a name="example-ini-file"></a>Archivo INI de ejemplo

A continuación se muestra un ejemplo de un archivo de inicialización que se usa en el ejemplo [de creación de un archivo DLL de extensión de](creating-a-performance-extension-dll.md) rendimiento.

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

## <a name="running-the-lodctr-tool"></a>Ejecución de la herramienta Lodctr

Para cargar los nombres y las cadenas de ayuda definidas en el archivo .INI (durante la instalación del proveedor), ejecute la herramienta **lodctr** desde la carpeta que contiene el archivo .INI y el archivo de encabezado. La herramienta se incluye con el equipo. Debe ejecutar **lodctr con** privilegios elevados. El parámetro para **lodctr** es la ruta de acceso al .INI archivo. Por ejemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Para descargar los nombres y las cadenas de ayuda (durante la desinstalación), ejecute **la herramienta unlodctr.** Debe ejecutar **unlodctr con** privilegios elevados. El parámetro para **unlodctr** es driverName del proveedor (el nombre de la clave de rendimiento del proveedor). Por ejemplo, `unlodctr "MyProvider"`.

Antes de **ejecutar lodctr,** asegúrese de que la aplicación tiene una entrada bajo la **clave Servicios.** Para más información, consulte [Creación de la clave de rendimiento de la aplicación.](creating-the-applications-performance-key.md) Si la clave no existe, **lodctr** no actualizará el registro con sus nombres y descripciones.

Como alternativa a ejecutar **lodctr,** puede llamar a [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido en Loadperf.h) desde el programa de instalación para cargar las descripciones de los nombres de los contadores. A continuación, puede llamar [**a UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante la desinstalación.

La **utilidad lodctr** copia las cadenas del archivo .INI en los valores del Registro **Counters** y **Help** en las subclaves de lenguaje adecuadas. Si la subclave de idioma correspondiente no existe, no se copian las cadenas de ese idioma. La utilidad también actualiza los valores **Last Counter (Último contador)** **y Last Help (Última** ayuda). Los nombres y descripciones de los contadores de rendimiento se almacenan en la siguiente ubicación del Registro.

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

Además de agregar valores bajo la clave **PerfLib,** la herramienta **lodctr** también agrega los siguientes valores al nodo **Servicios** de la aplicación. En la mayoría de los casos, la aplicación y el proveedor tendrán una relación uno a uno. sin embargo, es posible que un proveedor proporcione datos de contador para varias aplicaciones, por lo que la clave se basa en la aplicación y no en el proveedor.

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
