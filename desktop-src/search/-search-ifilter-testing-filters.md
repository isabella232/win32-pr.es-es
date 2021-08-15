---
description: El conjunto de pruebas IFilter valida los controladores de filtro.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Probar controladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b77fe098c2413e4f582ebfd98985dd09bf0ab9b5fc2def85fc7e954804dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463103"
---
# <a name="testing-filter-handlers"></a>Probar controladores de filtro

El [**conjunto de pruebas IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valida los controladores de filtro. Para ello, el conjunto de pruebas llama a métodos [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y comprueba el cumplimiento de los valores devueltos con la especificación de **la interfaz IFilter.** y comprobar que los identificadores de fragmento son únicos y crecientes, que la interfaz **IFilter** se comporta de forma coherente después de la nueva inicialización y que cualquier **método IFilter** llama a con parámetros no válidos devuelve códigos de error esperados. Los programas del conjunto de pruebas también vuelca la salida de un archivo filtrado por un controlador de filtros y comprueban la información de registro **de IFilter** en el registro.

Este tema se organiza de la siguiente manera:

- [Invocación de línea de comandos](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Procedimiento de prueba de IFilter](#ifilter-test-procedure)
  - [Prueba de validación](#validation-test)
  - [Prueba de coherencia](#consistency-test)
  - [Prueba de entrada no válida](#invalid-input-test)
  - [Probar diferentes configuraciones de IFilter](#testing-different-ifilter-configurations)
- [Asegurarse de que los elementos registrados se indexa](#ensuring-registered-items-get-indexed)
  - [Archivo de registro de ejemplo](#sample-log-file)
  - [Archivo de volcado de ejemplo](#sample-dump-file)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

> [!NOTE]  
> Si se instala un nuevo controlador de filtro para un tipo de archivo como reemplazo de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtros es responsable de replicar cualquier funcionalidad necesaria del filtro anterior.

## <a name="command-line-invocation"></a>Command-Line invocación

El [**conjunto de pruebas IFilter**](/windows/win32/api/filter/nn-filter-ifilter) consta de tres aplicaciones de línea de [ comandos:ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)y [filtreg.exe](#filtregexe) y un archivo de [ inicialización,ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros DEBEN escribirse en código nativo debido a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.

### <a name="ifilttstexe"></a>ifilttst.exe

El ifilttst.exe ejecuta varias pruebas para validar un controlador de filtro. En el ejemplo siguiente se muestra cómo invocar el programa ifilttst.exe desde la línea de comandos:


```
ifilttst /i test.htm /l /d /v 1
```

En el ejemplo se realizan las siguientes tareas:

- Dirige al programa para filtrar el archivo test.htm
- Redirige los mensajes de registro a test.htm.log
- Redirige los mensajes de volcado a test.htm.dmp
- Establece el nivel de detalle en 1

Para que el comando anterior funcione, deben encontrarse tres archivos en el directorio de trabajo actual: `test.htm` , [ifilttst.exe](#ifilttstexe)y [ifilttst.ini](#ifilttstini). Los modificadores de línea de comandos se muestran en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Modificador y variables posibles</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Nombre de archivo /i</strong></td>
<td>El archivo o directorio de entrada que se va a filtrar. El nombre de archivo puede contener los caracteres comodín <code>*</code> y <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>Los mensajes de registro se dirigen a un archivo en lugar de a la pantalla. Los mensajes de registro describen las pruebas individuales realizadas y los resultados de superación o error de las pruebas. El nombre del archivo de registro es el mismo que el nombre del archivo de entrada, pero con una extensión .log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Los mensajes de volcado se dirigen a un archivo en lugar de a la pantalla. Los mensajes de volcado de memoria describen el contenido de los fragmentos. La estructura del fragmento se vuelca cuando el nivel de detalle es 3. El nombre del archivo de volcado es el mismo que el nombre del archivo de entrada, pero con una extensión .dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Deshabilite el registro. Esta marca invalida el <code>/l</code> modificador .</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Deshabilite el volcado. Esta marca invalida el <code>/d</code> modificador .</td>
</tr>
<tr class="even">
<td><strong>Entero /v</strong></td>
<td>Nivel de detalle. El valor predeterminado es 3.
<ul>
<li>0 : la prueba registra solo los mensajes relacionados con errores específicos de la interfaz <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter.</strong></a> La prueba vuelca el contenido del fragmento.</li>
<li>1 - La prueba registra los mensajes de advertencia, así como los del nivel 0.</li>
<li>2 - La prueba registra mensajes relativos a las pruebas superdas, así como a las del nivel 1.</li>
<li>3 - La prueba registra mensajes informativos, así como los del nivel 2. Además, la prueba vuelca la estructura del fragmento.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Entero /t</strong></td>
<td>Número de subprocesos que se inician. El valor predeterminado es 1.</td>
</tr>
<tr class="even">
<td><strong>/r integer</strong>]</td>
<td>Filtra los subdirectorios de forma recursiva. El parámetro integer opcional especifica la profundidad a la que se va a realizar la recursividad. Si no se especifica ningún entero o si el entero es 0, se supone una recursividad completa. De forma predeterminada, la profundidad de recursividad es 1.</td>
</tr>
<tr class="odd">
<td><strong>Entero /c</strong></td>
<td>Número de veces que se debe recorrer en bucle. Si el entero es 0, la prueba recorre en bucle de forma infinita. De forma predeterminada, la prueba solo se recorre una vez.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Debe incluir un espacio entre el modificador de línea de comandos y el valor .

### <a name="filtdumpexe"></a>filtdump.exe

El filtdump.exe carga un controlador de filtro para un documento especificado e imprime la salida producida por el archivo DLL [**de IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) En el ejemplo siguiente se muestra cómo invocar el filtdump.exe programa.

```
filtdump filename.ext
```
Filtdump.exe usa el método [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) para cargar el archivo DLL [**de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) adecuado para la extensión de nombre de archivo especificada e imprime los resultados. Por ejemplo, el siguiente comando indica filtdump.exe que cargue el controlador de filtro de smpfilt.dll para la extensión .smp, extraiga todo el texto y las propiedades del archivo myfile.smp e imprima los resultados.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

El filtreg.exe inspecciona la información [**de instalación de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el Registro. Para invocar el filtreg.exe desde la línea de comandos, escriba su nombre, como en el ejemplo siguiente.

```
filtreg
```

Filtreg.exe enumera todas las extensiones de nombre de archivo que tienen controladores de filtro asociados mediante la impresión de la extensión de nombre de archivo y el nombre del archivo DLL [**de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para la extensión. Se trata de una manera sencilla de comprobar la instalación correcta de **un IFilter.**

### <a name="ifilttstini"></a>ifilttst.ini

Una [**interfaz IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se inicializa mediante una llamada al [**método IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) El **método IFilter::Init** toma los cuatro parámetros siguientes:

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

El usuario del programa ifilttst.exe del conjunto de pruebas [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) puede especificar los valores de estos parámetros en un archivo denominado ifilttst.ini. En la tabla siguiente se describen las entradas del ifilttst.ini que especifican los tres primeros parámetros (los parámetros de entrada). Para obtener un archivo de ejemplo, vea [Sample ifilttst.ini File](#sample-ifilttstini-file).

> [!NOTE]  
> No hay ninguna entrada de tabla para el *parámetro pdwFlags* porque es un parámetro de salida; no necesita tener ningún valor especial antes de la llamada al [**método IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init)

 | Entrada         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Marcas         | Nombres de las marcas [**\_ IFILTER INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) que se van a unir mediante el operador OR para formar el parámetro *grfFlags* del [**método IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) Todos los nombres de marca deben estar en mayúsculas y en la misma línea.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Entero decimal que representa el valor del *parámetro cAttributes.*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Esta entrada debe comenzar con *aAttributes* y debe ser diferente de las *otras entradas aAttributes* dentro de la sección . Los nombres legales de la *entrada aAttributes* son: *aAttributes*, *aAttributes1,* *aAttributes2,* etc. El primer token debe ser un GUID. El GUID debe tener el formato exacto como se muestra en la `[Test3]` sección del archivo de ifilttst.ini [ejemplo](#sample-ifilttstini-file). El segundo token puede ser un identificador de propiedad (PID) que consta de un número en notación hexadecimal o un puntero a una cadena de caracteres anchos (lpwstr). Se puede especificar un lpwstr si se incluye la cadena entre comillas dobles, como se muestra en la sección del archivo de ifilttst.ini `[Test6]` ejemplo. |

Si no se especifican las entradas Flags y *cAttributes,* el valor predeterminado es 0. Si establece *cAttributes* en 2, debe especificar dos *nombres aAttributes.* En la `[Test5]` sección del ejemplo, *cAttributes* es 1, pero no se ha especificado *aAttributes.* A continuación, la prueba llama al [**método IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *cAttributes* igual a 1 y *aAttributes* igual a **NULL.** Se trata de un caso de prueba útil porque es probable que cause una infracción de acceso en el **método IFilter::Init.**

Si ifilttst.exe encuentra un archivo denominado ifilttst.ini en el directorio de trabajo, se usa una configuración predeterminada para inicializar el [**objeto IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) En el ejemplo siguiente se muestra la configuración predeterminada.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Archivo de ifilttst.ini ejemplo

El ifilttst.ini se organiza en secciones, con el nombre de la sección entre corchetes. En el ejemplo, las secciones se denominan `[Test1]` `[Test2]` , , etc. Todos los nombres de sección deben ser únicos. La prueba lee los valores de la primera sección e inicializa [**el IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con esos valores. A continuación, todas las pruebas se ejecutan con esta **configuración de IFilter.** A **continuación, el IFilter** se libera y reinicializa con los parámetros enumerados anteriormente. El proceso se repite hasta que se prueban todas las configuraciones.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>Procedimiento de prueba de IFilter

Una vez [**inicializado el IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) el ifilttst.exe realiza una serie de pruebas en **el IFilter**. Además de seguir los procedimientos **de prueba de IFilter,** asegúrese de que la implementación **de IFilter** emplea prácticas de código seguro. Vea "Secure Code Practices for Windows Search" (Prácticas de código seguro para la búsqueda de filtros) en [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md)(Implementar controladores de filtro en Windows Search).

### <a name="validation-test"></a>Prueba de validación

La prueba de validación pasa por el objeto fragmento a fragmento a la vez, comprobando cada fragmento individual y todos los códigos de retorno. La prueba de validación guarda todas las estructuras [**\_ STAT CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) devueltas en una lista.

La prueba de validación comprueba las condiciones siguientes:

- EL [**FRAGMENTO \_ DE STAT**](/windows/win32/api/filter/ns-filter-stat_chunk).*Los identificadores de fragmento idChunk* deben ser únicos y aumentar.
- EL [**FRAGMENTO \_ DE STAT**](/windows/win32/api/filter/ns-filter-stat_chunk).*El parámetro flags* es un estado de fragmento reconocido, como las constantes [**CHUNKSTATE,**](/windows/win32/api/filter/ne-filter-chunkstate)CHUNK TEXT o \_ CenabledHUNK \_ VALUE.
- EL [**FRAGMENTO \_ DE STAT**](/windows/win32/api/filter/ns-filter-stat_chunk).*El parámetro breakType* es un tipo de interrupción reconocido (0, 1, 2, 3, 4).
- Si los [**atributos de inicialización**](/windows/win32/api/filter/nn-filter-ifilter) de IFilter especifican que **el IFilter** debe devolver solo fragmentos que contengan propiedades internas de tipo de valor, *idChunkSource* debe ser igual a 0.
- Si el fragmento no se deriva, es decir, si no es una propiedad interna de tipo de valor, [**stat \_ chunk**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource debe* ser igual **a STAT \_ CHUNK.***idChunk*.
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S OK u otro valor devuelto aceptable, como \_ FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK \_ \_ UNAVAILABLE, etc.
- Si el fragmento contiene texto, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve S \_ OK, FILTER \_ S LAST TEXT o FILTER E NO MORE \_ \_ \_ \_ \_ \_ TEXT.
- Si [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve FILTER S LAST TEXT, la siguiente llamada a \_ \_ \_ **IFilter::GetText** devuelve FILTER \_ E NO MORE \_ \_ \_ TEXT.
- Si el fragmento contiene un valor, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve S \_ OK o FILTER E NO MORE \_ \_ \_ \_ VALUES.

### <a name="consistency-test"></a>Prueba de coherencia

El ifilttxt.exe programa vuelve a inicializar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros que en la prueba de validación y realiza una prueba de coherencia. Si la implementación de **IFilter** se ha inicializado con la marca [**IFILTER \_ INIT IFILTER**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) INIT INDEXING ONLY, la prueba libera la interfaz IFilter y la vuelve a enlazar antes de realizar otra llamada al método \_ \_ \_ [**IFilter::Init.**](/windows/win32/api/filter/nf-filter-ifilter-init) 

La prueba de coherencia comprueba las condiciones siguientes:

- Cada [**estructura \_ STAT CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) devuelta por el método [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) es idéntica al FRAGMENTO DE STAT correspondiente devuelto en la prueba de validación. **\_**
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S OK u otro valor devuelto aceptable, como \_ FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK \_ \_ UNAVAILABLE, etc.

### <a name="invalid-input-test"></a>Prueba de entrada no válida

El ifilttst.exe programa vuelve a inicializar la [**interfaz IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros y realiza una prueba de entrada no válida. Esta prueba pasa por el documento de un fragmento a la vez realizando llamadas de función incorrectamente, como llamar al método [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) cuando el objeto contains actual contiene texto. La prueba comprueba si todos los códigos de retorno cumplen la **especificación de IFilter.**

La prueba de entrada no válida comprueba las condiciones siguientes:

- Si el fragmento actual contiene texto, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve FILTER E NO VALUES y una llamada \_ \_ a \_ [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) se realiza correctamente.
- Si el fragmento actual contiene un valor, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve FILTER E NO TEXT y una llamada \_ \_ a \_ [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) se realiza correctamente.
- Si la llamada anterior a [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devolvió FILTER E NO MORE TEXT, las llamadas sucesivas a \_ \_ \_ \_ **IFilter::GetText** devuelven FILTER \_ E NO MORE \_ \_ \_ TEXT.
- Si la llamada anterior a [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devolvió FILTER E NO MORE VALUES, las llamadas sucesivas a \_ \_ \_ \_ **IFilter::GetValue** devuelven FILTER \_ E NO MORE \_ \_ \_ VALUES.
- Si la llamada anterior a [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devolvió FILTER E END OF CHUNKS, las llamadas sucesivas a \_ \_ \_ \_ **IFilter::GetChunk** devuelven FILTER \_ E END OF \_ \_ \_ CHUNKS.

> [!NOTE]  
> La prueba de entrada no válida compara las estructuras de fragmentos actuales con las devueltas en la prueba de validación para asegurarse de que son idénticas.

### <a name="testing-different-ifilter-configurations"></a>Probar diferentes configuraciones de IFilter

El ifilttst.exe programa libera la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y vuelve a enlazamiento, esta vez inicializándose con el siguiente conjunto de parámetros. La prueba repite el ciclo: prueba de validación, prueba de coherencia y prueba [](#ifilttstini) de entrada no válida, hasta que se hayan probado todas las configuraciones de **IFilter** deseadas especificadas enifilttst.iniarchivo.

## <a name="ensuring-registered-items-get-indexed"></a>Asegurarse de que los elementos registrados se indexa

La prueba final del [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantiza que el **IFilter** está registrado correctamente y que se invoca para indexar los elementos que registró para usarlo. Puede usar el Administrador de catálogos para iniciar la re indexación o usar el Administrador del ámbito de rastreo (CSM) para configurar reglas predeterminadas que indiquen las direcciones URL que desea que rastree el indexador. Una vez completada la indexación, use la interfaz Windows search para buscar una cadena en el contenido o las propiedades de los elementos. Si los elementos se han indexado, aparecerán en los resultados de la búsqueda.

Para obtener más información sobre la re-indexación, vea Usar el Administrador [de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [Usar el Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md). El ejemplo de código ReindexMatchingUrls muestra maneras de especificar qué archivos se van a volver a indexar y cómo. El ejemplo de código CrawlScopeCommandLine muestra cómo definir opciones de línea de comandos para Administrador del ámbito de rastreo de indexación de Administrador del ámbito de rastreo (CSM). Ambos ejemplos de código están disponibles [en GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>Archivo de registro de ejemplo

Tras la solicitud, Ifilttst.exe programa puede generar un registro que contenga una descripción de los pasos que realiza durante la ejecución. Los ejemplos siguientes son extractos de un archivo de registro, con el nivel de detalle establecido en el valor 3 más alto posible.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

La primera línea es un mensaje informativo, que indica que se ha cargado una nueva configuración desde el ifilttst.ini archivo. La línea (3) indica el nombre de la sección en el ifilttst.ini del que se ha leído la configuración actual. Las líneas (de 4) a (7) enumera los parámetros de [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init). Las líneas que `INFO` empiezan por son mensajes informativos sobre el enlace de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el inicio de la prueba de validación. Las líneas que `PASS` empiezan por son mensajes relacionados con pruebas específicas que se han superado.

La línea del siguiente ejemplo de registro es una advertencia. Las advertencias llaman la atención [**sobre el comportamiento de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es problemático, aunque es legal. Esta advertencia indica que el [**método IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha devuelto un fragmento de texto que no contiene texto.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

El siguiente mensaje de error de ejemplo indica que [**el IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento que no se solicitó.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

En el caso de este mensaje de error de ejemplo, [**el IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento con un PID de `0x5` . La inspección de `[Test1]` la sección ifilttst.ini mostraría que el **IFilter** se configuró para no emitir fragmentos con este PID. Por ejemplo, si no se especificaron IFILTER INIT APPLY INDEX ATTRIBUTES ni IFILTER INIT APPLY OTHER ATTRIBUTES en la entrada Flags y \_ \_ si \_ \_ \_ \_ \_ \_ *cAttributes* fuera 0, **IFilter** `0x13` \_ \_ emitiría solo fragmentos con un PID de y correspondientes a PID STG CONTENTS.

### <a name="sample-dump-file"></a>Archivo de volcado de ejemplo

Tras la solicitud, Ifilttst.exe programa puede generar un volcado de memoria que contenga los fragmentos que encuentra y su contenido. El ejemplo siguiente es un extracto de este archivo de volcado de memoria.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

Las nueve primeras líneas describen la estructura de fragmentos actual. El GUID y el PID corresponden al CONTENIDO de \_ \_ STG de PSGUID \_ STORAGE/PID. Se trata de un fragmento que contiene texto sin formato. El texto está en la siguiente estructura de fragmentos:

```
10. This is an HTML IFilter test page
```

El siguiente fragmento, a partir de la línea 11, tiene un GUID diferente, correspondiente a , y un PID diferente, correspondiente `HTML IFilter` a un HREF HTML. Se trata de una propiedad de tipo de valor interno, exportada por `HTML IFilter` .

El fragmento siguiente, a partir de la línea 21, tiene el mismo GUID y PID, pero su estado de fragmento es `VALUE` en lugar de `TEXT` . Tenga en cuenta que el texto de estos dos últimos fragmentos es el mismo que para el primer fragmento. Pero dado que [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) está diseñado para aplicar tres atributos (texto sin formato, HREF HTML como texto y HREF HTML como valor) a esta frase, los resultados se emiten en tres fragmentos independientes.

## <a name="additional-resources"></a>Recursos adicionales

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)

[Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)
