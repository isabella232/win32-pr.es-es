---
description: La herramienta CTRPP es un preprocesador que analiza y valida el manifiesto de contadores.
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: eacfbb83abd56becc579c6b9bbaedacda96f94b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119110"
---
# <a name="ctrpp"></a>CTRPP

La herramienta CTRPP es un preprocesador que analiza y valida el manifiesto para el proveedor V2. La herramienta genera recursos con las cadenas necesarias para los consumidores del proveedor y genera un encabezado con código que se usa para proporcionar los `.rc` `.h` datos del contador. Debe ejecutar la herramienta CTRPP durante la compilación del proveedor. Debe usar el código generado como punto de partida al desarrollar el proveedor en lugar de intentar generar este código usted mismo.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumentos

|Opción              |Descripción
|--------------------|-----------
|*inputFile*         |**Obligatorio:** Especifica el nombre del archivo `.man` (manifiesto XML) que define los contadores.
|**-o** *codeFile*   |**Obligatorio:** Especifica el nombre del archivo `.h` de código que va a generar CTRPP. Este archivo contendrá funciones auxiliares insertadas de C/C++ que simplifican la inicialización y la desinicialización del proveedor.
|**-rc** *rcFile*    |**Obligatorio:** Especifica el nombre del `.rc` (archivo de recursos) que va a generar CTRPP. Este archivo contendrá la tabla de cadenas del proveedor.
|**-ch** *symFile*   |Especifica el nombre del archivo de símbolos opcional que `.h` va a generar CTRPP. Este archivo contendrá símbolos de C/C++ para los nombres y GUID de cada conjunto de contadores del proveedor.
|**Prefijo -prefix** |Especifica el prefijo que se usará para las variables y funciones definidas en el archivo de encabezado generado.
|**-NotificationCallback**|Cambia la firma predeterminada de la función [**CounterInitialize**](counterinitialize.md) para incluir parámetros para especificar el nombre de las funciones de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest), [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)y [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Este argumento tiene el mismo efecto que incluir el `callback` atributo en el elemento [**provider.**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
|**-migrate** *outputFile*|En lugar de generar archivos y , actualiza el manifiesto inputFile a la versión más reciente y `.h` `.rc` lo guarda en *outputFile*  . Este modificador no se puede usar con otros modificadores. Uso: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**En desuso:** Se agregó compatibilidad con proveedores de modo kernel en Windows 7. De forma predeterminada, el código generado por CTRPP para los proveedores de modo kernel será incompatible con versiones anteriores de Windows (el controlador no se cargará debido a que faltan `Pcw***` API). Se `-BackCompat` establece para habilitar la compatibilidad con versiones anteriores de Windows. El controlador cargará dinámicamente las API necesarias y el código generado deshabilitará de forma silenciosa el proveedor si las API no están disponibles.
|**-MemoryRoutines** |**En desuso:** Cuando se usa con el `-Legacy` modificador , incluye plantillas para rutinas de memoria en el código generado. De lo contrario, este argumento tiene el mismo efecto que el `-NotificationCallback` modificador .
|**-Legacy**         |**En desuso:** Genera archivos , , y mediante las plantillas de código de `*.h` `*.c` Windows Vista `*.rc` `*_r.h` (genera PerfAutoInitialize y PerfAutoCleanup en lugar de CounterInitialize y CounterCleanup). Este modificador se puede usar con **-MemoryRoutines** y **-NotificationCallback,** pero no se puede usar con ningún otro modificador. No use los **modificadores -o** **o -rc** con este modificador. Los archivos generados se denominarán en función del nombre del manifiesto y se escribirán en el directorio que contiene el manifiesto. Uso: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Observaciones

La herramienta CTRPP genera un archivo de código, un archivo `.h` de recursos y, opcionalmente, genera un `.rc` archivo de `.h` símbolos.

### <a name="using-the-generated-resource-file"></a>Uso del archivo de recursos generado

La herramienta CTRPP generará un archivo de recursos que contiene las cadenas localizables que necesitan los consumidores de los contraconjuntos `.rc` del proveedor.

> [!IMPORTANT]
> Los recursos de este archivo deben incluirse en el archivo binario del proveedor y la ruta de acceso completa al binario del proveedor debe registrarse durante la instalación del manifiesto del proveedor. Los consumidores que no puedan encontrar y cargar los recursos no podrán usar los contraconjuntos del proveedor.

Los recursos de cadena deben controlarse de la siguiente manera:

- El desarrollador edita el archivo de manifiesto de proveedor ( ) para establecer el atributo del proveedor en el nombre de un binario de proveedor (.DLL, .SYS o .EXE) que contendrá los recursos de cadena para el proveedor y se instalará como parte del componente `.man` `applicationIdentity` del proveedor.
- La herramienta CTRPP lee el manifiesto del proveedor y genera un `.rc` archivo.
- La [herramienta RC (compilador de recursos)](../menurc/resource-compiler.md) compila los datos del archivo generado por CTRPP para generar un archivo `.rc` que contiene los recursos `.res` binarios. Esto se puede hacer compilando directamente el archivo generado por CTRPP O compilando otro archivo que incluya el archivo generado por CTRPP a través de `.rc` `.rc` una directiva `.rc` `#include` .
- El vinculador inserta los datos del archivo generado por RC `.res` en el binario del proveedor.
- Durante la instalación, el binario del proveedor se copia en el sistema del usuario y el manifiesto del proveedor se registra mediante [la herramienta lodctr](/windows-server/administration/windows-commands/lodctr). La herramienta lodctr convierte el atributo del manifiesto del proveedor en una ruta de acceso completa y registra la ruta de acceso completa al binario del `applicationIdentity` proveedor en el registro.
  - Si el binario del proveedor está en el mismo directorio que el manifiesto, use: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr combinará la ruta de acceso del manifiesto especificada con el atributo `applicationIdentity` del manifiesto para formar la ruta de acceso completa.
  - De lo contrario, use `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr combinará la ruta de acceso binaria especificada con el atributo `applicationIdentity` del manifiesto para formar la ruta de acceso completa.
  - Con fines de diagnóstico, puede inspeccionar la ruta de acceso completa registrada comprobando el `ApplicationIdentity` valor de la clave del Registro `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Si el archivo binario usa LAM para la localización, asegúrese de copiar el archivo DE LAN junto con el binario.
- Durante la recopilación de conjuntos de contadores, el consumidor usa la ruta de acceso completa registrada al binario del proveedor para buscar y cargar las cadenas necesarias desde los recursos binarios del proveedor.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Uso del archivo de código generado en un proveedor de modo de usuario

La herramienta CTRPP generará un archivo `.h` de código de C/C++. Si el atributo del manifiesto del proveedor se establece en , el archivo de código generado contendrá las siguientes definiciones que son útiles para codificar `providerType` un proveedor en modo de `userMode` usuario:

- Una función de inicialización de proveedor [ * **denominada prefix*CounterInitialize**](counterinitialize.md).
- Una función de limpieza de proveedor [ * **denominada prefix*CounterCleanup**](countercleanup.md).
- Variable global ***provider** _ que almacena el identificador del proveedor abierto por la función _ *_prefix_CounterInitialize**. El nombre de la variable es el valor del `symbol` atributo del elemento en el `provider` manifiesto. Esta variable debe usarse en llamadas a `PerfCreateInstance` `PerfDeleteInstance` , y otras API para controlar los datos del proveedor.
- Para cada conjunto de contadores, una variable global ***counterset*GUID** con el GUID del conjunto de contadores. El nombre de la variable es el valor del atributo del elemento más el `counterSet` `symbol` sufijo "GUID", por ejemplo, `MyCounterSetGUID` . Esta variable debe usarse en llamadas a `PerfCreateInstance` `PerfDeleteInstance` , y otras API para controlar los datos del proveedor.
- Para cada contador, una macro ***de*** contador con el valor del `id` contador. El nombre de la macro es el valor del `counter` atributo del `symbol` elemento. Esta macro debe usarse en llamadas a `PerfSetCounterRefValue` `PerfSetULongLongCounterValue` , y otras API para establecer los datos del proveedor.

En los nombres de función, ***prefix*** hace referencia al valor del parámetro `-prefix` de línea de comandos. Si no `-prefix` se usa el parámetro , las funciones se denominarán y `CounterInitialize` `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Uso del archivo de código generado en un proveedor de modo kernel

La herramienta CTRPP generará un archivo `.h` de código de C/C++. Si el atributo del manifiesto del proveedor se establece en , el archivo de código generado contendrá las siguientes definiciones que son útiles para codificar los conjuntos de contadores de un proveedor en modo `providerType` `kernelMode` kernel:

- Una función de inicialización de conjunto de <b> *contadores denominada prefix* Register *Counterset*</b>. Esta función rellena una estructura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) y, a continuación, invoca [a PcwRegister,](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)colocando el identificador de registro del conjunto de contadores resultante en la variable ***counterset*** global.
- Una función de limpieza del conjunto de <b> *contadores denominada prefix* Unregister *Counterset*</b>. Esta función invoca [PcwUnregister en](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) el identificador de registro del conjunto de contadores en la variable ***counterset*** global.
- Una función de creación de instancias denominada <b> *prefix* Create *Counterset*</b>. Esta función rellena una matriz de estructuras [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) y, a continuación, invoca [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) mediante el identificador de registro del conjunto de contadores en la variable ***counterset*** global.
- Una función de limpieza de instancia denominada <b> *prefix* Close *Counterset*</b>. Esta función invoca [a PcwCloseInstance.](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance)
- Una función de informes de instancia denominada <b> *prefix**Add Counterset*</b> que se usará desde la función de devolución de llamada del conjunto de contadores. Esta función rellena una matriz de estructuras [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) y, a continuación, invoca [a PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **Windows SDK 20H1 y versiones posteriores:** Una función de inicialización RegInfo denominada <b> *prefix* InitRegistrationInformation *Counterset*</b> para su uso en escenarios avanzados. Esta función rellena una [estructura RegInfo.](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) Esta función se puede usar en casos en los que el prefijo generado <b> Register *Counterset*</b> no satisface sus necesidades, por ejemplo, cuando desea personalizar los valores de la estructura RegInfo o cuando desea almacenar el identificador devuelto en otra variable.

En los nombres de función, ***prefix*** hace referencia al valor del parámetro `-prefix` de línea de comandos. Si no `-prefix` se usa el parámetro , las funciones no tendrán ningún prefijo.

> [!NOTE]
> La función <b> *Add**Counterset del*</b> prefijo generado se usa cuando se tiene una devolución de llamada de conjunto de contadores. Las funciones <b> *Create**Counterset (Crear conjunto de contadores)*</b> y <b> *Prefix**Close Counterset*</b> (Cerrar conjunto de contadores) generados se usan cuando no tiene una devolución de llamada de conjunto de contadores.

### <a name="using-the-generated-symbol-file"></a>Uso del archivo de símbolos generado

Si el **parámetro -ch** se especifica en la línea de comandos, la herramienta CTRPP generará un archivo `.h` de símbolos. Este archivo contiene los símbolos de C/C++ para los nombres y GUID de cada conjunto de contadores del proveedor. Los símbolos se pueden usar al escribir programas codificados de forma hard para consumir los datos de este contraconjunto mediante las funciones [perfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisitos

| Requisito             | Valor |
|-------------------------|-------|
| Cliente mínimo compatible| Solo aplicaciones de escritorio de Windows Vista \[\]
| Servidor mínimo compatible| Solo aplicaciones de escritorio de Windows Server 2008 \[\]
