---
description: Puede usar las funciones del registro para recopilar datos de rendimiento.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Usar las funciones del registro para consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ce2a4ba9992510cb296b037cfd98965410c48939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667237"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Usar las funciones del registro para consumir datos de contador

Utilice las [funciones del registro](/windows/desktop/SysInfo/registry-functions) para recopilar datos de rendimiento de la `HKEY_PERFORMANCE_DATA` clave del registro especial.

Los datos de rendimiento no se almacenan realmente en el registro. Llamar a las funciones del registro hace que el sistema recopile los datos del proveedor de datos de rendimiento adecuado.

> [!Note]
> Normalmente no debe usar las funciones del registro para consumir datos de contador. En su lugar, debe [usar las funciones de la aplicación auxiliar de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md). Las funciones de PDH son más fáciles de usar y evitan muchos problemas de rendimiento y confiabilidad que se pueden producir a través del uso incorrecto de las funciones del registro.

> [!Note]
> No puede usar las funciones del registro si está escribiendo aplicaciones de Windows OneCore. En su lugar, use [las funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

Las funciones del registro son la API de bajo nivel para recopilar datos de **proveedores de v1**. Las funciones del registro también admiten la recopilación de datos de **proveedores V2** a través de una capa de traducción que llama a las [funciones de consumidor V2](using-the-perflib-functions-to-consume-counter-data.md).

Para obtener los datos de rendimiento del sistema local, llame a la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) . Use `HKEY_PERFORMANCE_DATA` como clave. La primera llamada abre la clave. No es necesario abrir la clave explícitamente primero.

Para obtener datos de rendimiento de un sistema remoto, llame a la función [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) . Use el nombre de equipo del sistema remoto y use `HKEY_PERFORMANCE_DATA` como clave. Esta llamada recupera una clave que representa los datos de rendimiento del sistema remoto. Use esta clave en lugar de `HKEY_PERFORMANCE_DATA` la clave para recuperar los datos.

Asegúrese de usar la función [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) para cerrar el identificador de la clave cuando termine de obtener los datos de rendimiento. Esto es importante para los casos locales y remotos:

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` no cierra realmente un identificador del registro, pero borra todos los datos almacenados en caché y libera los archivos dll de rendimiento cargados.
- `RegCloseKey(hkeyRemotePerformanceData)` cierra el identificador del registro del equipo remoto.

> [!IMPORTANT]
> No llame a `RegCloseKey(HKEY_PERFORMANCE_DATA)` durante `DLL_PROCESS_DETACH` .

Use el `lpValueName` parámetro de la función [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para indicar la información que se va a recuperar. En la tabla siguiente se enumeran los valores que se pueden especificar para `lpValueName` . Tenga en cuenta que las cadenas de valor no distinguen mayúsculas de minúsculas.

|Value|Descripción
|-----|-----------
|`Global`| Recupera los datos de rendimiento de todos los objetos de rendimiento registrados en el equipo, excepto los incluidos en la `Costly` categoría.
|`OLD_Global`| **Windows Vista y versiones posteriores:** Recupera los datos de rendimiento de todos los objetos de rendimiento **v1** registrados en el equipo, excepto los incluidos en la `Costly` categoría. Utilice esto en lugar de `Global` para evitar la recopilación de datos innecesarios del proveedor V2 cuando sepa que los datos de interés provienen de un proveedor v1.
|`n1 n2 ...`| Recupera los datos de rendimiento de uno o más objetos de rendimiento. Especifique el índice decimal asociado a cada objeto que desea recuperar en una lista separada por espacios. Por ejemplo, si desea recuperar objetos del sistema y de memoria y ha determinado que los índices de las cadenas de nombre correspondientes son 2 y 4, especifique la cadena `"2 4"` . Tenga en cuenta que la consulta puede devolver un número diferente de objetos de los solicitados. Esto puede ocurrir si el objeto especificado no está disponible, si el objeto especificado depende de otro tipo de objeto o si un proveedor devuelve datos que no se solicitaron directamente. Por ejemplo, los subprocesos dependen de los procesos, por lo que si se solicitan datos del `Thread` objeto, los resultados incluirán datos del `Process` objeto.
|`Counter n`| Recupera cadenas de nombre para el identificador de idioma especificado, por ejemplo, Inglés para `Counter 9` . Utilice las cadenas de nombre devueltas para buscar el índice correspondiente a un nombre determinado o para buscar el nombre correspondiente a un índice determinado. Vea [recuperar nombres de contadores y texto de ayuda](retrieving-counter-names-and-help-text.md) para obtener información detallada. Tenga en cuenta que la lista devuelta incluye nombres de objeto (CounterSet) y nombres de contador, no hay ninguna forma sencilla de determinar si un nombre es un nombre de objeto o un nombre de contador.
|`Help n`| Recupera las cadenas de ayuda para el identificador de idioma especificado, por ejemplo, Inglés para `Help 9` . Use las cadenas de ayuda devueltas para buscar descripciones correspondientes a objetos (CounterSet) o índices de ayuda de contador. Vea [recuperar nombres de contadores y texto de ayuda](retrieving-counter-names-and-help-text.md) para obtener información detallada.
|`Costly`| En **desuso:** Recupera los datos de rendimiento de los tipos de objeto cuyos datos son caros de recopilar en términos de tiempo de procesador o uso de memoria. Esta recopilación puede tardar varios minutos en un equipo con mucha carga. Debe realizar la recopilación en un subproceso de trabajo si la aplicación necesita responder al usuario durante esta recopilación de datos.

Para obtener más información sobre el formato de los datos de rendimiento que devuelve el registro, vea [performance Data Format](performance-data-format.md).

Para obtener un ejemplo en el que se obtienen los nombres y las descripciones de los contadores registrados en el equipo, vea [recuperar nombres de contadores y texto de ayuda](retrieving-counter-names-and-help-text.md).

Para obtener un ejemplo en el que se obtiene acceso a los componentes de los datos de rendimiento, vea [Mostrar los nombres de objeto, instancia y contador](displaying-object-instance-and-counter-names.md).

Para obtener un ejemplo en el que se recuperan, calculan e imprimen valores de contador, vea [recuperar datos de contadores](retrieving-counter-data.md) y [calcular valores de contadores](calculating-counter-values.md).
