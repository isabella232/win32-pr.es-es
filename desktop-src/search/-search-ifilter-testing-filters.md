---
description: El conjunto de pruebas de IFilter valida los controladores de filtro.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Probar controladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153969"
---
# <a name="testing-filter-handlers"></a>Probar controladores de filtro

El conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valida los controladores de filtro. El conjunto de pruebas lo hace mediante la llamada a métodos de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y la comprobación de los valores devueltos para la compatibilidad con la especificación de interfaz de **IFilter** ; y comprobar que los identificadores de fragmentos son únicos y aumentan, que la interfaz de **IFilter** se comporta de forma coherente después de la reinicialización, y que las llamadas a métodos de **IFilter** con parámetros no válidos devuelven los códigos de error esperados. Los programas del conjunto de pruebas también vuelcan la salida de un archivo filtrado por un controlador de filtro y comprueban la información de registro de **IFilter** en el registro.

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
- [Asegurarse de que los elementos registrados se indexan](#ensuring-registered-items-get-indexed)
  - [Archivo de registro de ejemplo](#sample-log-file)
  - [Archivo de volcado de ejemplo](#sample-dump-file)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

> [!NOTE]  
> Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.

## <a name="command-line-invocation"></a>Invocación de Command-Line

El conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) consta de tres aplicaciones de línea de comandos: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)y [filtreg.exe](#filtregexe) y un archivo de inicialización, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente. Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.

### <a name="ifilttstexe"></a>ifilttst.exe

El programa ifilttst.exe ejecuta varias pruebas para validar un controlador de filtro. En el ejemplo siguiente se muestra cómo invocar el programa ifilttst.exe desde la línea de comandos:


```
ifilttst /i test.htm /l /d /v 1
```

En el ejemplo se realizan las tareas siguientes:

- Indica al programa que filtre el archivo test.htm
- Redirige los mensajes de registro a test.htm. log.
- Redirige los mensajes de volcado a test.htm. DMP
- Establece el nivel de detalle en 1

Para que el comando anterior funcione, se deben encontrar tres archivos en el directorio de trabajo actual: `test.htm` , [ifilttst.exe](#ifilttstexe)y [ifilttst.ini](#ifilttstini). Los modificadores de la línea de comandos se muestran en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Modificador y posibles variables</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i nombre de archivo</strong></td>
<td>El archivo o directorio de entrada que se va a filtrar. El nombre de archivo puede contener los caracteres comodín <code>*</code> y <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>l</strong></td>
<td>Los mensajes de registro se dirigen a un archivo en lugar de a la pantalla. Los mensajes de registro describen las pruebas individuales realizadas y los resultados de superación y error de las pruebas. El nombre del archivo de registro es el mismo que el nombre del archivo de entrada, pero con la extensión. log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Los mensajes de volcado de memoria se dirigen a un archivo en lugar de a la pantalla. Los mensajes de volcado describen el contenido de los fragmentos. La estructura de fragmentos se vuelca cuando el nivel de detalle es 3. El nombre del archivo de volcado es el mismo que el nombre del archivo de entrada, pero con una extensión. DMP.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Deshabilitar el registro. Esta marca invalida el <code>/l</code> modificador.</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Deshabilite el volcado. Esta marca invalida el <code>/d</code> modificador.</td>
</tr>
<tr class="even">
<td><strong>/v (entero)</strong></td>
<td>Nivel de detalle. El valor predeterminado es 3.
<ul>
<li>0: la prueba solo registra mensajes relativos a errores específicos de la interfaz de <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> . La prueba vuelca el contenido del fragmento.</li>
<li>1-la prueba registra los mensajes de advertencia y los del nivel 0.</li>
<li>2-la prueba registra mensajes relativos a las pruebas superadas, así como a las de nivel 1.</li>
<li>3-la prueba registra los mensajes informativos, así como los de nivel 2. Además, la prueba vuelca la estructura del fragmento.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t (entero)</strong></td>
<td>Número de subprocesos que se van a iniciar. El valor predeterminado es 1.</td>
</tr>
<tr class="even">
<td><strong>/r (entero</strong>)]</td>
<td>Filtra subdirectorios de forma recursiva. El parámetro de entero opcional especifica la profundidad a la que se debe ejercitar la recursividad. Si no se especifica ningún entero, o si el entero es 0, se asume la recursividad completa. De forma predeterminada, la profundidad de recursividad es 1.</td>
</tr>
<tr class="odd">
<td><strong>/c entero</strong></td>
<td>Número de veces que se va a crear un bucle. Si el entero es 0, la prueba se repite infinitamente. De forma predeterminada, la prueba se repite solo una vez.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Debe incluir un espacio entre el modificador de la línea de comandos y el valor.

### <a name="filtdumpexe"></a>filtdump.exe

El programa filtdump.exe carga un controlador de filtro para un documento especificado e imprime el resultado generado por el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . En el ejemplo siguiente se muestra cómo invocar el programa filtdump.exe.

```
filtdump filename.ext
```
Filtdump.exe usa el método [ILoadFilter:: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) para cargar el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) adecuado para la extensión de nombre de archivo especificada e imprime los resultados. Por ejemplo, el comando siguiente indica a filtdump.exe que cargue el controlador de filtro de smpfilt.dll para la extensión. SMP, extraiga todo el texto y las propiedades del archivo Perfile. SMP e imprima los resultados.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

El programa filtreg.exe inspecciona la información de instalación de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el registro. Para invocar el programa filtreg.exe desde la línea de comandos, escriba su nombre, como en el ejemplo siguiente.

```
filtreg
```

En Filtreg.exe se enumeran todas las extensiones de nombre de archivo que tienen controladores de filtros asociados mediante la impresión de la extensión de nombre de archivo y el nombre del archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de la extensión. Se trata de una manera sencilla de comprobar la instalación correcta de un **IFilter**.

### <a name="ifilttstini"></a>ifilttst.ini

Una interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se inicializa llamando al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . El método **IFilter:: init** toma los cuatro parámetros siguientes:

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

El usuario del programa ifilttst.exe del conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) puede especificar los valores de estos parámetros en un archivo denominado ifilttst.ini. En la tabla siguiente se describen las entradas del archivo de ifilttst.ini que especifican los tres primeros parámetros (los parámetros de entrada). Para obtener un archivo de ejemplo, vea [archivo de ifilttst.ini de ejemplo](#sample-ifilttstini-file).

> [!NOTE]  
> No hay ninguna entrada de tabla para el parámetro *pdwFlags* porque es un parámetro de salida. no es necesario que tenga ningún valor especial antes de la llamada al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

 | Entrada         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Marcas         | Los nombres de las marcas de [**\_ inicialización IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) que van a estar unidas por el operador o para formar el parámetro *grfFlags* del método [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Los nombres de las marcas deben estar en mayúsculas y en la misma línea.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Entero decimal que representa el valor del parámetro *cAttributes* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Esta entrada debe comenzar con *aAttributes* y debe ser diferente de las demás entradas de *aAttributes* dentro de la sección. Los nombres válidos para la entrada *aAttributes* son: *aAttributes*, *aAttributes1*, *aAttributes2*, etc. El primer token debe ser un GUID. Se debe dar formato al GUID exactamente como se muestra en la `[Test3]` sección del [archivo de ifilttst.ini de ejemplo](#sample-ifilttstini-file). El segundo token puede ser un identificador de propiedad (PID) que consta de un número en notación hexadecimal o un puntero a una cadena de caracteres anchos (LPWStr). Se puede especificar LPWStr mediante la inclusión de la cadena entre comillas dobles, como se muestra en la `[Test6]` sección del archivo de ifilttst.ini de ejemplo. |

Si no se especifican las entradas flags y *cAttributes* , el valor predeterminado es 0. Si establece *cAttributes* en 2, debe especificar dos nombres de *aAttributes* . En la `[Test5]` sección del ejemplo, *cAttributes* es 1, pero no se ha especificado ningún *aAttributes* . Después, la prueba llama al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *cAttributes* igual a 1 y *aAttributes* igual a **null**. Este es un caso de prueba útil porque es probable que provoque una infracción de acceso en el método **IFilter:: init** .

Si ifilttst.exe no encuentra un archivo denominado ifilttst.ini en el directorio de trabajo, se usa una configuración predeterminada para inicializar el objeto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . En el ejemplo siguiente se muestra la configuración predeterminada.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Archivo de ifilttst.ini de ejemplo

El archivo ifilttst.ini se organiza en secciones, con el nombre de sección entre corchetes. En el ejemplo, las secciones se denominan `[Test1]` , `[Test2]` , y así sucesivamente. Todos los nombres de sección deben ser únicos. La prueba Lee los valores de la primera sección e inicializa el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con esos valores. Después, todas las pruebas se ejecutan con esta configuración de **IFilter** . A continuación, se libera y se reinicializa el **IFilter** , con los parámetros que se enumeran anteriormente. El proceso se repite hasta que se prueban todas las configuraciones.

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

Una vez inicializado el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , el programa ifilttst.exe realiza una serie de pruebas en el **IFilter**. Además de seguir los procedimientos de prueba de **IFilter** , asegúrese de que la implementación de **IFilter** emplea prácticas de código seguro. Consulte "prácticas de código seguro para Windows Search" en [implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Prueba de validación

La prueba de validación recorre el objeto un fragmento cada vez, comprobando cada fragmento individual y todos los códigos de retorno. La prueba de validación guarda todas las estructuras de [**\_ fragmentos de estadísticas**](/windows/win32/api/filter/ns-filter-stat_chunk) devueltas en una lista.

La prueba de validación comprueba las condiciones siguientes:

- [**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.** los identificadores de fragmentos de idChunk deben ser únicos y aumentar.
- [**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.*el parámetro flags* es un estado de fragmento reconocido, como [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), \_ texto de fragmento o \_ constantes de valor CenabledHUNK.
- [**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.** el parámetro breakType es un tipo de interrupción reconocido (0, 1, 2, 3, 4).
- Si los atributos de inicialización de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) especifican que el **IFilter** debe devolver solo fragmentos que contienen propiedades internas de tipo de valor, *idChunkSource* debe ser igual a 0.
- Si el fragmento no se deriva, es decir, si no es una propiedad de tipo de valor interna, se [**declarará \_ fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* debe ser igual al **\_ fragmento STAT**.*idChunk*.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S \_ o cualquier otro valor de retorno aceptable, como filtro \_ e \_ fin \_ de \_ fragmentos, filtro \_ e \_ vínculo \_ no disponible, etc.
- Si el fragmento contiene texto, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve s \_ correcto, filtrar el \_ \_ último \_ texto o filtrar \_ E \_ no \_ más \_ texto.
- Si [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve \_ \_ \_ el último texto del filtro, la siguiente llamada a **IFILTER:: gettext** devuelve el filtro \_ E \_ ningún \_ \_ texto más.
- Si el fragmento contiene un valor, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve d \_ o el filtro \_ E \_ no tiene \_ más \_ valores.

### <a name="consistency-test"></a>Prueba de coherencia

El programa ifilttxt.exe reinicializa la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros que en la prueba de validación y realiza una prueba de coherencia. Si la implementación de **IFilter** se ha inicializado con la marca [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ Indexing \_ Only, la prueba libera la interfaz **IFilter** y la vuelve a enlazar antes de realizar otra llamada al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

La prueba de coherencia comprueba las condiciones siguientes:

- Cada estructura de [**\_ fragmentos de estadísticas**](/windows/win32/api/filter/ns-filter-stat_chunk) devuelta por el método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) es idéntica **al \_ fragmento de STAT** correspondiente devuelto en la prueba de validación.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S \_ o cualquier otro valor de retorno aceptable, como filtro \_ e \_ fin \_ de \_ fragmentos, filtro \_ e \_ vínculo \_ no disponible, etc.

### <a name="invalid-input-test"></a>Prueba de entrada no válida

El programa ifilttst.exe reinicializa la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros y realiza una prueba de entrada no válida. En esta prueba se recorre el documento un fragmento cada vez que realiza llamadas a funciones incorrectamente, por ejemplo, al llamar al método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) cuando el campo Chuck actual contiene texto. La prueba comprueba la compatibilidad de todos los códigos de retorno con la especificación **IFilter** .

La prueba de entrada no válida comprueba las condiciones siguientes:

- Si el fragmento actual contiene texto, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve \_ \_ los valores Filter e no \_ , y una llamada a [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) se realiza correctamente.
- Si el fragmento actual contiene un valor, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve Filter \_ E \_ no \_ Text y una llamada a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) se realiza correctamente.
- Si la llamada anterior a [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devolvió el filtro \_ e \_ no hay \_ más \_ texto, las llamadas sucesivas a **IFilter:: gettext** devuelven el filtro \_ e \_ no hay \_ más \_ texto.
- Si la llamada anterior a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devolvió el filtro \_ e \_ no hay \_ más \_ valores, las llamadas sucesivas a **IFilter:: GetValue** devuelven el filtro \_ e \_ ningún \_ \_ valor más.
- Si la llamada anterior a [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devolvió el filtro \_ e \_ final \_ de \_ fragmentos, las sucesivas llamadas a **IFilter:: GetChunk** devuelven el filtro \_ de devolución e \_ final \_ de los \_ fragmentos.

> [!NOTE]  
> La prueba de entrada no válida compara las estructuras de fragmentos actuales con las devueltas en la prueba de validación para asegurarse de que son idénticas.

### <a name="testing-different-ifilter-configurations"></a>Probar diferentes configuraciones de IFilter

El programa ifilttst.exe libera la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y vuelve a enlazar, esta vez inicializándose con el siguiente conjunto de parámetros. La prueba repite el ciclo: prueba de validación, prueba de coherencia y prueba de entrada no válida, hasta que se hayan probado todas las configuraciones de **IFilter** deseadas especificadas en [ifilttst.ini](#ifilttstini) archivo.

## <a name="ensuring-registered-items-get-indexed"></a>Asegurarse de que los elementos registrados se indexan

La prueba final de su [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantiza que su **IFilter** está correctamente registrado y que se invoca para indexar los elementos que ha registrado para usarlos. Puede usar el administrador de catálogos para iniciar la reindización o usar el administrador de ámbito de rastreo (CSM) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador. Una vez completada la indexación, use la interfaz de usuario de búsqueda de Windows para buscar una cadena en el contenido o las propiedades de los elementos. Si los elementos se indexaron, aparecerán en los resultados de la búsqueda.

Para obtener más información acerca de la reindización, consulte [uso del administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md). En el ejemplo de código ReindexMatchingUrls se muestran las maneras de especificar qué archivos se van a volver a indizar y cómo. En el ejemplo de código CrawlScopeCommandLine se muestra cómo definir las opciones de la línea de comandos para las operaciones de indización del administrador de ámbito de rastreo (CSM). Ambos ejemplos de código están disponibles en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>Archivo de registro de ejemplo

Previa solicitud, el programa de Ifilttst.exe puede generar un registro que contenga una descripción de los pasos que se realizan durante la ejecución. Los ejemplos siguientes son fragmentos de un archivo de registro, con el nivel de detalle establecido en el valor 3 más alto.

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

La primera línea es un mensaje informativo, que indica que se ha cargado una nueva configuración del archivo de ifilttst.ini. La línea (3) indica el nombre de la sección en el ifilttst.ini archivo desde el que se ha leído la configuración actual. Las líneas (4) a (7) muestran los parámetros en [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init). Las líneas que comienzan con `INFO` son mensajes informativos sobre el enlace del [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el inicio de la prueba de validación. Las líneas que comienzan con `PASS` son mensajes relativos a las pruebas específicas que se han superado.

La línea del siguiente ejemplo de registro es una advertencia. Las advertencias informan sobre el comportamiento de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es problemático, aunque es legal. Esta advertencia indica que el método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha devuelto un fragmento de texto que no contiene texto.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

El mensaje de error de ejemplo siguiente indica que el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento que no se solicitó.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

En el caso de este mensaje de error de ejemplo, el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento con un PID de `0x5` . La inspección de `[Test1]` la sección en ifilttst.ini mostraría que el **IFilter** se configuró para no emitir fragmentos con este PID. Por ejemplo, si \_ \_ no se especifican los atributos IFilter init Apply de \_ Índice \_ ni IFilter \_ init \_ \_ \_ , se han especificado otros atributos en la entrada flags y, si *cAttributes* eran 0, **IFILTER** solo emitirá fragmentos con un PID de `0x13` y correspondiente al contenido de PID \_ STG \_ .

### <a name="sample-dump-file"></a>Archivo de volcado de ejemplo

Previa solicitud, el programa de Ifilttst.exe puede generar un volcado de memoria que contiene los fragmentos que encuentra y su contenido. El ejemplo siguiente es un extracto de este archivo de volcado de memoria.

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

Las nueve primeras líneas describen la estructura de fragmentos actual. El GUID y el PID se corresponden con el contenido de PSGUID \_ Storage/PID \_ STG \_ . Se trata de un fragmento que contiene texto sin formato. El texto está en la siguiente estructura de fragmentos:

```
10. This is an HTML IFilter test page
```

El siguiente fragmento, a partir de la línea 11, tiene un GUID diferente, que corresponde a `HTML IFilter` , y un PID diferente, que corresponde a un elemento HTML href. Se trata de una propiedad de tipo de valor interna, exportada por `HTML IFilter` .

El siguiente fragmento, a partir de la línea 21, tiene el mismo GUID y el mismo PID, pero su estado de fragmento es `VALUE` en lugar de `TEXT` . Tenga en cuenta que el texto de estos dos últimos fragmentos es el mismo que el del primer fragmento. Pero como el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) está diseñado para tres atributos (texto sin formato, HTML href como texto y HTML href como valor) para que se aplique a esta frase, los resultados se emiten en tres fragmentos independientes.

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)
