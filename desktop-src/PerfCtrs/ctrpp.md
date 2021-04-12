---
description: La herramienta CTRPP es un preprocesador que analiza y valida el manifiesto de los contadores.
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
ms.openlocfilehash: dce12de641dda7b07871a4447190772533598748
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361970"
---
# <a name="ctrpp"></a>CTRPP

La herramienta CTRPP es un preprocesador que analiza y valida el manifiesto del proveedor V2. La herramienta genera `.rc` recursos con las cadenas que necesitan los consumidores del proveedor y genera un `.h` encabezado con el código que se usa para proporcionar los datos del contador. Debe ejecutar la herramienta CTRPP durante la compilación del proveedor. Debe usar el código generado como punto de partida al desarrollar el proveedor en lugar de intentar generar este código.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argumentos

|Opción              |Descripción
|--------------------|-----------
|*ArchivoDeEntrada*         |**Requerido:** Especifica el nombre del `.man` archivo (manifiesto XML) que define los contadores.
|**-o** *Codefile*   |**Requerido:** Especifica el nombre del `.h` archivo de código que va a generar CTRPP. Este archivo contendrá funciones auxiliares insertadas de C/C++ que simplifican la inicialización y la anulación de la inicialización del proveedor.
|**-RC** *rcFile*    |**Requerido:** Especifica el nombre del `.rc` (archivo de recursos) que va a generar CTRPP. Este archivo contendrá la tabla de cadenas del proveedor.
|**-CH** *symFile*   |Especifica el nombre del archivo de `.h` símbolos opcional que va a generar CTRPP. Este archivo contendrá símbolos de C/C++ para los nombres y GUID de cada CounterSet en el proveedor.
|- *prefijo* **de prefijo**|Especifica el prefijo que se va a usar para las variables y funciones definidas en el archivo de encabezado generado.
|**-NotificationCallback**|Cambia la firma predeterminada de la función de [**Contrainicialización**](counterinitialize.md) para incluir los parámetros para especificar el nombre de las funciones de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest), [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)y [*FreeMemory (*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Este argumento tiene el mismo efecto que incluir el `callback` atributo en el elemento de [**proveedor**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) .
|**-migrar** *outputFile*|En lugar de generar `.h` `.rc` archivos y, actualiza el manifiesto de *ArchivoDeEntrada* a la versión más reciente y lo guarda en *outputFile*. Este modificador no se puede usar con otros modificadores. Uso: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |En **desuso:** En Windows 7 se ha agregado compatibilidad con proveedores de modo kernel. De forma predeterminada, el código generado por CTRPP para los proveedores de modo kernel no será compatible con versiones anteriores de Windows (el controlador no se cargará debido a que faltan `Pcw***` API). Establezca `-BackCompat` para habilitar la compatibilidad con versiones anteriores de Windows. El controlador cargará dinámicamente las API necesarias y el código generado deshabilitará de forma silenciosa el proveedor si las API no están disponibles.
|**-MemoryRoutines** |En **desuso:** Cuando se usa con el `-Legacy` modificador, incluye plantillas para las rutinas de memoria en el código generado. De lo contrario, este argumento tiene el mismo efecto que el `-NotificationCallback` modificador.
|**-Heredado**         |En **desuso:** Genera `*.h` `*.c` archivos,, `*.rc` y `*_r.h` con las plantillas de código de Windows Vista (genera PerfAutoInitialize y PerfAutoCleanup en lugar de la contrainicialización y la limpieza). Este modificador se puede usar con **-MemoryRoutines** y **-NotificationCallback** , pero no se puede usar con ningún otro modificador. No use los modificadores **-o** o **-RC** con este modificador. Los archivos generados se nombrarán según el nombre del manifiesto y se escribirán en el directorio que contenía el manifiesto. Uso: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Observaciones

La herramienta CTRPP genera un `.h` archivo de código, un `.rc` archivo de recursos y, opcionalmente, genera un `.h` archivo de símbolos.

### <a name="using-the-generated-resource-file"></a>Usar el archivo de recursos generado

La herramienta CTRPP generará un `.rc` archivo de recursos que contiene las cadenas localizables que necesitan los consumidores de los contraconjuntos del proveedor.

> [!IMPORTANT]
> Los recursos de este archivo se deben incluir en el binario del proveedor y la ruta de acceso completa al binario del proveedor se debe registrar durante la instalación del manifiesto del proveedor. Los consumidores que no pueden localizar y cargar los recursos no podrán usar los valores de su proveedor.

Los recursos de cadena deben administrarse de la siguiente manera:

- El desarrollador edita el archivo de manifiesto del proveedor ( `.man` ) para establecer el `applicationIdentity` atributo del proveedor en el nombre de un binario de proveedor (. DLL,. SYS o. EXE) que contendrá los recursos de cadena para el proveedor y se instalará como parte del componente de proveedor.
- La herramienta CTRPP lee el manifiesto del proveedor y genera un `.rc` archivo.
- La herramienta [RC (compilador de recursos)](../menurc/resource-compiler.md) compila los datos del archivo generado por CTRPP `.rc` para generar un `.res` archivo que contiene los recursos binarios. Para ello, puede compilar directamente el archivo generado por CTRPP `.rc` o compilar otro `.rc` archivo que incluya el archivo generado por CTRPP `.rc` a través de una `#include` Directiva.
- El vinculador incrusta los datos del archivo generado por RC `.res` en el binario del proveedor.
- Durante la instalación, el binario del proveedor se copia en el sistema del usuario y el manifiesto del proveedor se registra mediante la [herramienta LODCTR](/windows-server/administration/windows-commands/lodctr). La herramienta LODCTR convierte el `applicationIdentity` atributo del manifiesto del proveedor en una ruta de acceso completa y registra la ruta de acceso completa al binario del proveedor en el registro.
  - Si el binario del proveedor está en el mismo directorio que el manifiesto, use: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . LODCTR combinará la ruta de acceso del manifiesto especificada con el atributo del manifiesto `applicationIdentity` para formar la ruta de acceso completa.
  - De lo contrario, use `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. LODCTR combinará la ruta de acceso binaria especificada con el atributo del manifiesto `applicationIdentity` para formar la ruta de acceso completa.
  - Con fines de diagnóstico, puede inspeccionar la ruta de acceso completa registrada comprobando el `ApplicationIdentity` valor de la clave del registro `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Si el binario usa MUI para la localización, asegúrese de copiar el archivo MUI junto con el binario.
- Durante la colección CounterSet, el consumidor utiliza la ruta de acceso completa registrada al binario del proveedor para buscar y cargar las cadenas necesarias de los recursos del binario del proveedor.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Usar el archivo de código generado en un proveedor de modo de usuario

La herramienta CTRPP generará un `.h` archivo de código de C/C++. Si el atributo del manifiesto del proveedor `providerType` está establecido en `userMode` , el archivo de código generado contendrá las siguientes definiciones que son útiles para codificar un proveedor de modo usuario:

- Una función de inicialización de proveedor denominada [ * **prefix * contrainitial**](counterinitialize.md).
- Una función de limpieza de proveedor denominada [ * **prefix * contracleanup**](countercleanup.md).
- Una variable global ***Provider** _ que almacena el identificador de proveedor abierto por la función _ *_prefix_CounterInitialize**. El nombre de la variable es el valor del `symbol` atributo del `provider` elemento en el manifiesto. Esta variable se debe usar en las llamadas a `PerfCreateInstance` , `PerfDeleteInstance` y otras API para controlar los datos del proveedor.
- Para cada CounterSet, una variable global ***CounterSet * GUID** con el GUID de CounterSet. El nombre de la variable es el valor del `counterSet` atributo del elemento `symbol` más el sufijo "GUID", por ejemplo, `MyCounterSetGUID` . Esta variable se debe usar en las llamadas a `PerfCreateInstance` , `PerfDeleteInstance` y otras API para controlar los datos del proveedor.
- Para cada contador, una macro de ***contador*** con el valor del contador `id` . El nombre de la macro es el valor del `counter` atributo del elemento `symbol` . Esta macro se debe usar en las llamadas a `PerfSetCounterRefValue` , `PerfSetULongLongCounterValue` y otras API para configurar los datos del proveedor.

En los nombres de función, el ***prefijo*** hace referencia al valor del `-prefix` parámetro de línea de comandos. Si `-prefix` no se usa el parámetro, las funciones se denominarán `CounterInitialize` y `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Usar el archivo de código generado en un proveedor de modo kernel

La herramienta CTRPP generará un `.h` archivo de código de C/C++. Si el atributo del manifiesto del proveedor `providerType` está establecido en `kernelMode` , el archivo de código generado contendrá las siguientes definiciones que son útiles para codificar los contraconjuntos de un proveedor de modo kernel:

- Una función de inicialización de CounterSet denominada <b> *prefix* registra *CounterSet*</b>. Esta función rellena una estructura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) y después invoca [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister), colocando el identificador de registro CounterSet resultante en la variable global ***CounterSet*** .
- Una función de limpieza CounterSet denominada <b> *prefix* unregister *CounterSet*</b>. Esta función invoca [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) en el identificador de registro de CounterSet en la variable global ***CounterSet*** .
- Una función de creación de instancia denominada <b> *prefix* Create *CounterSet*</b>. Esta función rellena una matriz de estructuras [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) y, a continuación, invoca [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) con el identificador de registro CounterSet en la variable global ***CounterSet*** .
- Una función de limpieza de instancia denominada <b> *prefix* Close *CounterSet*</b>. Esta función invoca [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Una función de creación de informes de instancia denominada <b> *prefix* Add *CounterSet*</b> que se va a usar desde la función de devolución de llamada CounterSet. Esta función rellena una matriz de estructuras [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) y, a continuación, invoca [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **Windows SDK 20H1 y versiones posteriores:** Una función de inicialización de RegInfo denominada <b> *prefix* InitRegistrationInformation *CounterSet*</b> para su uso en escenarios avanzados. Esta función rellena una estructura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) . Esta función se puede usar en casos en los que el valor de <b>*CounterSet* del registro de *prefijo*</b> generado no satisface sus necesidades, por ejemplo, cuando desea personalizar los valores de la estructura RegInfo o cuando desea almacenar el identificador devuelto en otra variable.

En los nombres de función, el ***prefijo*** hace referencia al valor del `-prefix` parámetro de línea de comandos. Si `-prefix` no se usa el parámetro, las funciones no tendrán ningún prefijo.

> [!NOTE]
> La función de <b> *prefijo* de agregar *CounterSet*</b> generada se usa cuando se tiene una devolución de llamada CounterSet. Las funciones generadas de <b> *prefijo* de creación *CounterSet*</b> y de cierre de <b> *prefijo*</b> CounterSet se usan cuando no se tiene una devolución de llamada CounterSet.

### <a name="using-the-generated-symbol-file"></a>Usar el archivo de símbolos generado

Si se especifica el parámetro **-CH** en la línea de comandos, la herramienta CTRPP generará un `.h` archivo de símbolos. Este archivo contiene los símbolos de C/C++ para los nombres y GUID de cada CounterSet en el proveedor. Los símbolos se pueden usar al escribir programas que están codificados de forma rígida para consumir los datos de este CounterSet mediante las [funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisitos

|                         ||
|-------------------------|----
| Cliente mínimo compatible| Solo aplicaciones de escritorio de Windows Vista \[\]
| Servidor mínimo compatible| Solo aplicaciones de escritorio de Windows Server 2008 \[\]
