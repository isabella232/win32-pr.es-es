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
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="34943-103">Adición de nombres y descripciones de contadores al registro</span><span class="sxs-lookup"><span data-stu-id="34943-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34943-104">Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="34943-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="34943-105">En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método.</span><span class="sxs-lookup"><span data-stu-id="34943-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="34943-106">Los nombres y descripciones de todos los objetos de rendimiento V1 y sus contadores deben estar instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="34943-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="34943-107">Para almacenar los nombres y las descripciones de los objetos y contadores de su [proveedor v1](providing-counter-data.md):</span><span class="sxs-lookup"><span data-stu-id="34943-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="34943-108">[Cree un archivo de encabezado. h](#creating-a-symbolic-constants-h-file) que contenga las constantes simbólicas de los desplazamientos de los objetos y contadores.</span><span class="sxs-lookup"><span data-stu-id="34943-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="34943-109">[Cree una inicialización (. INI)](#creating-an-initialization-ini-file) que contiene las cadenas.</span><span class="sxs-lookup"><span data-stu-id="34943-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="34943-110">Al instalar el componente, [ejecute la herramienta **LODCTR**](#running-the-lodctr-tool) para instalar los nombres y las descripciones en el registro.</span><span class="sxs-lookup"><span data-stu-id="34943-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="34943-111">Al desinstalar el componente, ejecute la herramienta Unlodctr para quitar los nombres y las descripciones del registro.</span><span class="sxs-lookup"><span data-stu-id="34943-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="34943-112">Crear un archivo de constantes simbólicas (. h)</span><span class="sxs-lookup"><span data-stu-id="34943-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="34943-113">Cree un archivo de encabezado. h que defina constantes (macros) para los desplazamientos a los objetos y contadores que proporciona el proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="34943-114">El encabezado. h se usa como entrada para **LODCTR** durante la instalación del proveedor y el código de C/C++ del proveedor también puede utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="34943-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="34943-115">Los valores constantes deben ser consecutivos, incluso números que empiezan por cero.</span><span class="sxs-lookup"><span data-stu-id="34943-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="34943-116">Agrupe las constantes por objetos (es decir, inicie cada grupo con el desplazamiento del objeto y, a continuación, siga con los desplazamientos de los contadores para ese objeto).</span><span class="sxs-lookup"><span data-stu-id="34943-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="34943-117">Las constantes del encabezado determinan el orden en que se agregan los contadores al nombre y al texto de ayuda del registro.</span><span class="sxs-lookup"><span data-stu-id="34943-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="34943-118">El proveedor utiliza los desplazamientos para determinar qué objeto se está consultando y los valores de índice que se van a utilizar al devolver los datos.</span><span class="sxs-lookup"><span data-stu-id="34943-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="34943-119">Para obtener más información, consulte [implementación de OpenPerformanceData](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="34943-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="34943-120">A continuación se muestra un ejemplo de un archivo de constante simbólica, denominado contraoffsets. h, que se usa en el ejemplo de [creación de una DLL de extensión de rendimiento](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="34943-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

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

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="34943-121">Crear una inicialización (. INI)</span><span class="sxs-lookup"><span data-stu-id="34943-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="34943-122">La inicialización (. INI) contiene el nombre y las cadenas de ayuda de cada objeto y contador definido en el archivo de símbolos.</span><span class="sxs-lookup"><span data-stu-id="34943-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="34943-123">El. El archivo INI se usa como entrada para **LODCTR** durante la instalación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="34943-124">El. El archivo INI se debe codificar como UTF-16LE (con marca de orden de bytes) y debe tener las siguientes secciones y claves:</span><span class="sxs-lookup"><span data-stu-id="34943-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

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

### <a name="info-section"></a><span data-ttu-id="34943-125">sección [info]</span><span class="sxs-lookup"><span data-stu-id="34943-125">[info] section</span></span>

<span data-ttu-id="34943-126">La `[info]` sección contiene información general sobre el proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="34943-127">Las claves de sección se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="34943-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="34943-128">Clave</span><span class="sxs-lookup"><span data-stu-id="34943-128">Key</span></span>|<span data-ttu-id="34943-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="34943-129">Description</span></span>
|---|-----------
|<span data-ttu-id="34943-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="34943-130">**DriverName**</span></span>| <span data-ttu-id="34943-131">Especifique el nombre de la clave de rendimiento del proveedor que se encuentra en el registro, en la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` clave.</span><span class="sxs-lookup"><span data-stu-id="34943-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="34943-132">Para obtener información sobre la creación de esta clave, consulte [crear la clave de rendimiento de la aplicación](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="34943-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="34943-133">**SymbolFile**</span><span class="sxs-lookup"><span data-stu-id="34943-133">**SymbolFile**</span></span>| <span data-ttu-id="34943-134">Especifique el archivo de encabezado. h que contiene los valores simbólicos de los objetos y contadores del proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="34943-135">Durante la instalación (al invocar **LODCTR**), el archivo de encabezado debe estar en el mismo directorio que. Archivo INI.</span><span class="sxs-lookup"><span data-stu-id="34943-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="34943-136">**Confiar**</span><span class="sxs-lookup"><span data-stu-id="34943-136">**Trusted**</span></span>| <span data-ttu-id="34943-137">Si incluye esta clave en la `[info]` sección, **LODCTR** agregará un valor del registro de código de validación de biblioteca a su clave de rendimiento con una firma binaria de la dll de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="34943-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="34943-138">Cuando PERFLIB llama a la DLL, compara la firma con el archivo DLL para determinar si se ha modificado el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="34943-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="34943-139">Se omite el valor de la clave de **confianza** .</span><span class="sxs-lookup"><span data-stu-id="34943-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="34943-140">Las `DriverName` `SymbolFile` claves y son necesarias.</span><span class="sxs-lookup"><span data-stu-id="34943-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="34943-141">sección [objetos]</span><span class="sxs-lookup"><span data-stu-id="34943-141">[objects] section</span></span>

<span data-ttu-id="34943-142">En la `[objects]` sección se proporciona una lista de los objetos de rendimiento que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="34943-143">Se utiliza para determinar si cada símbolo de la `[text]` sección hace referencia a un objeto o a un contador.</span><span class="sxs-lookup"><span data-stu-id="34943-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="34943-144">Para cada objeto (CounterSet) admitido por el proveedor, agregue una clave denominada `<symbol>_<langid>_NAME=` a la `[objects]` sección, donde `<symbol>` es el nombre del objeto y `<langid>` es el identificador de idioma de uno de los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="34943-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="34943-145">Se omite el valor.</span><span class="sxs-lookup"><span data-stu-id="34943-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34943-146">La `[objects]` sección mejora el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="34943-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="34943-147">Aunque la sección objetos es opcional, siempre debe incluir esta sección en su. Archivo INI.</span><span class="sxs-lookup"><span data-stu-id="34943-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="34943-148">Si incluye esta sección, solo se llama a la DLL de rendimiento si admite el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="34943-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="34943-149">Si no incluye la sección objetos, se llama a la DLL para cada consulta, ya que el sistema no sabe qué objetos admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="34943-150">Si no se incluye la sección Object, **LODCTR** genera un mensaje en el registro de eventos de la aplicación que indica que el objeto. El archivo INI no contiene una sección de objetos.</span><span class="sxs-lookup"><span data-stu-id="34943-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="34943-151">El identificador de evento de este mensaje es 2000.</span><span class="sxs-lookup"><span data-stu-id="34943-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="34943-152">sección [Languages]</span><span class="sxs-lookup"><span data-stu-id="34943-152">[languages] section</span></span>

<span data-ttu-id="34943-153">`[languages]`En esta sección se proporciona una lista de los identificadores de idioma de cada lenguaje para los que el proveedor proporciona cadenas de nombre y ayuda.</span><span class="sxs-lookup"><span data-stu-id="34943-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="34943-154">Todos los proveedores deben admitir `009` (Inglés).</span><span class="sxs-lookup"><span data-stu-id="34943-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="34943-155">Para cada idioma admitido, agregue una clave denominada `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="34943-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="34943-156">El valor se omite, pero para fines de documentación el valor se establece normalmente en el nombre del idioma correspondiente, por ejemplo, `009=English` .</span><span class="sxs-lookup"><span data-stu-id="34943-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="34943-157">Para la mayoría de los lenguajes, debe usar el identificador de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="34943-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="34943-158">La lista completa de identificadores de idioma está en el archivo de encabezado Winnt. h, bajo el encabezado "ID. de idioma principal".</span><span class="sxs-lookup"><span data-stu-id="34943-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="34943-159">Convierta el valor que se encuentra en Winnt. h en una secuencia de 3 dígitos hexadecimales quitando el `0x` prefijo y agregando los `0` dígitos iniciales hasta que la secuencia tenga 3 dígitos de longitud.</span><span class="sxs-lookup"><span data-stu-id="34943-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="34943-160">Por ejemplo, para especificar cadenas en inglés (0x9), use 009.</span><span class="sxs-lookup"><span data-stu-id="34943-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="34943-161">Para especificar cadenas italianas (0x10), use 010.</span><span class="sxs-lookup"><span data-stu-id="34943-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="34943-162">Los idiomas chino y Portugués requieren los identificadores principal y de subidioma.</span><span class="sxs-lookup"><span data-stu-id="34943-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="34943-163">Use 404, 804, 416 o 816 en lugar de 004 o 016.</span><span class="sxs-lookup"><span data-stu-id="34943-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="34943-164">[texto] sección</span><span class="sxs-lookup"><span data-stu-id="34943-164">[text] section</span></span>

<span data-ttu-id="34943-165">`[text]`En la sección se proporcionan el nombre y las cadenas de ayuda de los objetos y contadores.</span><span class="sxs-lookup"><span data-stu-id="34943-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="34943-166">Para cada objeto o contador, y para cada idioma admitido, debe proporcionar una clave de nombre (que contenga el nombre o la cadena de título para el objeto o el contador) y, opcionalmente, puede proporcionar una clave de ayuda (que contiene la descripción o la cadena de explicación del objeto o contador).</span><span class="sxs-lookup"><span data-stu-id="34943-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="34943-167">Las claves deben denominarse `<symbol>_<langid>_NAME` y `<symbol>_<langid>_HELP` , donde `<symbol>` es la constante simbólica del objeto o contador (tal y como se define en el archivo. h constante simbólico) y `<langid>` es el identificador de idioma que se usa para esta cadena.</span><span class="sxs-lookup"><span data-stu-id="34943-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="34943-168">Por ejemplo, las cadenas en inglés para un contador con símbolo `MY_COUNTER` se especifican como:</span><span class="sxs-lookup"><span data-stu-id="34943-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="34943-169">Las teclas de texto pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="34943-169">The text keys can appear in any order.</span></span> <span data-ttu-id="34943-170">Las cadenas de texto no deben contener caracteres de formato, como tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="34943-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="34943-171">Archivo INI de ejemplo</span><span class="sxs-lookup"><span data-stu-id="34943-171">Example INI file</span></span>

<span data-ttu-id="34943-172">A continuación se muestra un ejemplo de un archivo de inicialización que se usa en el ejemplo de [creación de un archivo dll de extensión de rendimiento](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="34943-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

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

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="34943-173">Ejecutar la herramienta LODCTR</span><span class="sxs-lookup"><span data-stu-id="34943-173">Running the Lodctr tool</span></span>

<span data-ttu-id="34943-174">Para cargar los nombres y las cadenas de ayuda definidas en su. Archivo INI (durante la instalación del proveedor), ejecute la herramienta **LODCTR** desde la carpeta que contiene el. Archivo INI y archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="34943-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="34943-175">La herramienta se incluye con el equipo.</span><span class="sxs-lookup"><span data-stu-id="34943-175">The tool is included with the computer.</span></span> <span data-ttu-id="34943-176">Debe ejecutar **LODCTR** con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="34943-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="34943-177">El parámetro de **LODCTR** es la ruta de acceso a. Archivo INI.</span><span class="sxs-lookup"><span data-stu-id="34943-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="34943-178">Por ejemplo, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="34943-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="34943-179">Para descargar los nombres y las cadenas de ayuda (durante la desinstalación), ejecute la herramienta **Unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="34943-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="34943-180">Debe ejecutar **Unlodctr** con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="34943-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="34943-181">El parámetro para **Unlodctr** es el drivername del proveedor (el nombre de la clave de rendimiento del proveedor).</span><span class="sxs-lookup"><span data-stu-id="34943-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="34943-182">Por ejemplo, `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="34943-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="34943-183">Antes de ejecutar **LODCTR**, asegúrese de que la aplicación tiene una entrada en la clave **servicios** .</span><span class="sxs-lookup"><span data-stu-id="34943-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="34943-184">Para obtener más información, consulte [crear la clave de rendimiento de la aplicación](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="34943-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="34943-185">Si la clave no existe, **LODCTR** no actualizará el registro con sus nombres y descripciones.</span><span class="sxs-lookup"><span data-stu-id="34943-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="34943-186">Como alternativa a ejecutar **LODCTR**, puede llamar a [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definido en Loadperf. h) desde el programa de instalación para cargar las descripciones de los nombres de los contadores.</span><span class="sxs-lookup"><span data-stu-id="34943-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="34943-187">Después, puede llamar a [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="34943-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="34943-188">La utilidad **LODCTR** copia las cadenas de. En los **contadores** y los valores del registro de **ayuda** en las subclaves del lenguaje adecuado.</span><span class="sxs-lookup"><span data-stu-id="34943-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="34943-189">Si la subclave del lenguaje correspondiente no existe, no se copian las cadenas para ese idioma.</span><span class="sxs-lookup"><span data-stu-id="34943-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="34943-190">La utilidad también actualiza el **último contador** y el último valor de la **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="34943-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="34943-191">Los nombres y descripciones de los contadores de rendimiento se almacenan en la siguiente ubicación del registro.</span><span class="sxs-lookup"><span data-stu-id="34943-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

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

<span data-ttu-id="34943-192">Además de agregar valores en la clave **Perflib** , la herramienta **LODCTR** también agrega los siguientes valores al nodo **servicios** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34943-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="34943-193">En la mayoría de los casos, la aplicación y el proveedor tendrán una relación uno a uno; sin embargo, es posible que un proveedor proporcione datos de contador para varias aplicaciones, por lo que la clave se basa en la aplicación y no en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="34943-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

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
