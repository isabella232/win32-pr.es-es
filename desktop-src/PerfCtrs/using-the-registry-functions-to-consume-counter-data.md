---
description: Puede usar las funciones del Registro para recopilar datos de rendimiento.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Usar las funciones del Registro para consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 69f64f6e4cb44dd98d4f5097ca791054cd04c7e07219dc0e270cbfdff4cdbdc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033125"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Usar las funciones del Registro para consumir datos de contador

Use las [funciones del Registro](/windows/desktop/SysInfo/registry-functions) para recopilar datos de rendimiento de la clave del Registro `HKEY_PERFORMANCE_DATA` especial.

Los datos de rendimiento no se almacenan realmente en el Registro. Llamar a las funciones del Registro hace que el sistema recopile los datos del proveedor de datos de rendimiento adecuado.

> [!Note]
> Normalmente, no debe usar las funciones del Registro para consumir datos de contador. En su lugar, debe usar las funciones del Asistente de datos [de rendimiento (PDH).](using-the-pdh-functions-to-consume-counter-data.md) Las funciones PDH son más fáciles de usar y evitan muchos problemas de rendimiento y confiabilidad que pueden producirse a través de un uso incorrecto de las funciones del Registro.

> [!Note]
> No puede usar las funciones del Registro si está escribiendo Windows OneCore aplicaciones. En su lugar, use [las funciones de consumidor de PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

Las funciones del Registro son la API de bajo nivel para recopilar datos de **proveedores V1.** Las funciones del Registro también admiten la recopilación de datos de proveedores **V2** a través de una capa de traducción que llama a las funciones [de consumidor V2](using-the-perflib-functions-to-consume-counter-data.md).

Para obtener datos de rendimiento del sistema local, llame a la [**función RegQueryValueEx.**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) Use `HKEY_PERFORMANCE_DATA` como clave. La primera llamada abre la clave. No es necesario abrir la clave explícitamente primero.

Para obtener datos de rendimiento de un sistema remoto, llame a [**la función RegConnectRegistry.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) Use el nombre de equipo del sistema remoto y use `HKEY_PERFORMANCE_DATA` como clave. Esta llamada recupera una clave que representa los datos de rendimiento del sistema remoto. Use esta clave en lugar `HKEY_PERFORMANCE_DATA` de la clave para recuperar los datos.

Asegúrese de usar la [**función RegCloseKey para**](/windows/desktop/api/winreg/nf-winreg-regclosekey) cerrar el identificador de la clave cuando haya terminado de obtener los datos de rendimiento. Esto es importante para los casos locales y remotos:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` no cierra realmente un identificador del Registro, pero borra todos los datos almacenados en caché y libera los archivos DLL de rendimiento cargados.
- `RegCloseKey(hkeyRemotePerformanceData)` cierra el identificador al registro del equipo remoto.

> [!IMPORTANT]
> No llame a `RegCloseKey(HKEY_PERFORMANCE_DATA)` durante `DLL_PROCESS_DETACH` .

Use el parámetro `lpValueName` de la [**función RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para indicar la información que se va a recuperar. En la tabla siguiente se enumeran los valores que puede especificar para `lpValueName` . Tenga en cuenta que las cadenas de valor no distinguen mayúsculas de minúsculas.

|Value|Descripción
|-----|-----------
|`Global`| Recupera los datos de rendimiento de todos los objetos de rendimiento registrados en el equipo, excepto los incluidos en la `Costly` categoría .
|`OLD_Global`| **Windows Vista y versiones posteriores:** Recupera los datos de rendimiento de todos **los objetos de rendimiento V1** registrados en el equipo, excepto los incluidos en la categoría `Costly` . Úsese esto en lugar de para evitar la recopilación de datos de proveedor V2 innecesarios cuando sepa que los datos de interés `Global` proceden de un proveedor V1.
|`n1 n2 ...`| Recupera los datos de rendimiento de uno o varios objetos de rendimiento. Especifique el índice decimal asociado a cada objeto que desea recuperar en una lista separada por espacios. Por ejemplo, si desea recuperar objetos System y Memory y ha determinado que los índices de las cadenas de nombre correspondientes son 2 y 4, especifique la cadena `"2 4"` . Tenga en cuenta que la consulta puede devolver un número diferente de objetos de los que solicitó. Esto puede ocurrir si el objeto especificado no está disponible, si el objeto especificado depende de otro tipo de objeto o si un proveedor devuelve datos que no se solicitaron directamente. Por ejemplo, los subprocesos dependen de los procesos, por lo que si solicita datos del objeto , los resultados `Thread` incluirán datos del `Process` objeto .
|`Counter n`| Recupera cadenas de nombre para el identificador de idioma especificado, por ejemplo, inglés para `Counter 9` . Use las cadenas de nombre devueltas para buscar el índice correspondiente a un nombre determinado o para buscar el nombre correspondiente a un índice determinado. Consulte [Recuperación de nombres de contadores y Texto de ayuda](retrieving-counter-names-and-help-text.md) para obtener más información. Tenga en cuenta que la lista devuelta incluye nombres de objeto (conjunto de contadores) y nombres de contador; no hay ninguna manera sencilla de determinar si un nombre es un nombre de objeto o un nombre de contador.
|`Help n`| Recupera las cadenas de ayuda para el identificador de idioma especificado, por ejemplo, inglés para `Help 9` . Use las cadenas de ayuda devueltas para buscar descripciones correspondientes a los índices de ayuda de objeto (contraconjunto) o de contador. Consulte [Recuperación de nombres de contadores y Texto de ayuda](retrieving-counter-names-and-help-text.md) para obtener más información.
|`Costly`| **En desuso:** Recupera los datos de rendimiento de los tipos de objeto cuyos datos son caros de recopilar en términos de tiempo de procesador o uso de memoria. Esta colección puede tardar varios minutos en una máquina cargada con gran carga. Debe realizar la recopilación en un subproceso de trabajo si la aplicación necesita responder al usuario durante esta recopilación de datos.

Para obtener más información sobre el formato de los datos de rendimiento que devuelve el Registro, vea [Formato de datos de rendimiento](performance-data-format.md).

Para obtener un ejemplo que obtiene los nombres y descripciones de los contadores registrados en el equipo, vea Recuperar nombres de contador y [Texto de ayuda](retrieving-counter-names-and-help-text.md).

Para obtener un ejemplo que tiene acceso a los componentes de los datos de rendimiento, vea Mostrar nombres de [objeto, instancia y contador](displaying-object-instance-and-counter-names.md).

Para obtener un ejemplo que recupera, calcula e imprime valores de contador, vea Recuperar datos [de contador](retrieving-counter-data.md) y Calcular valores [de contador](calculating-counter-values.md).
