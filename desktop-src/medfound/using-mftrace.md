---
description: MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Microsoft Media Foundation.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Usar MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f888ba8b202e4b77a3a571a25874032ec233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812584"
---
# <a name="using-mftrace"></a>Usar MFTrace

MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Microsoft Media Foundation.

MFTrace usa la biblioteca de desvíos para enlazar en Media Foundation llamadas API y generar registros de seguimiento. MFTrace también puede registrar seguimientos de cualquier componente que use el seguimiento de eventos para Windows (ETW) o el preprocesador de seguimiento de software (WPP) para generar seguimientos. Los registros de seguimiento pueden generarse iniciando un nuevo proceso desde MFTrace o adjuntando MFTrace a un proceso existente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-DC** \] \[ **-es** \] \[ **-k** *Keywords* \] \[ **-l** *LEVEL* \] \[ **-o** *OutputFile*- \] \[ **v** \] \[ **-** ? \] \[ {*Comando* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argumentos de la línea de comandos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Identificador de proceso o nombre de proceso</em><br/></td>
<td>Asociar a un proceso en ejecución.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Archivo de configuración</em><br/></td>
<td>Lee la configuración del archivo de configuración especificado. Vea el <a href="mftrace-configuration-file.md">archivo de configuración MFTrace</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br/></td>
<td>Deshabilite el seguimiento de procesos secundarios. De forma predeterminada, la traza está habilitada para los procesos secundarios.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Habilitar símbolos públicos.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Palabras clave</em><br/></td>
<td>Lista separada por comas de palabras clave. Vea <a href="mftrace-keywords.md">palabras clave de MFTrace</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Nivel</em> de<br/></td>
<td>Nivel de seguimiento.<br/>
<ul>
<li>0: Ninguno</li>
<li>1: crítico</li>
<li>2: error</li>
<li>3: ADVERTENCIA</li>
<li>4: informativo</li>
<li>5: detallado</li>
<li>16: depuración</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Archivo de salida</em><br/></td>
<td>Escribir la salida del seguimiento en el archivo especificado. De forma predeterminada, la salida va a <strong>stdout</strong>.<br/> Si se especifica un archivo de salida, la extensión de nombre de archivo debe ser una de las siguientes:<br/>
<ul>
<li>. ETL: archivo de registro de seguimiento de eventos (ETL).</li>
<li>. log o. txt: archivo de texto.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Habilitar el modo detallado.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Muestra información de uso.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>COMMAND</em><br/></td>
<td>Argumentos de la línea de comandos para crear un nuevo proceso.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>Nombre de un archivo ETL existente. Si se proporciona este argumento, el archivo ETL se convierte en salida de texto.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Variables de entorno

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Para realizar un seguimiento de los componentes que utilizan el preprocesador de seguimiento de software (WPP) de Windows, establezca esta variable de entorno en la especificación de la ruta de acceso a los archivos de formato de mensaje de seguimiento (TMF) para el componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Si la búsqueda de símbolos está habilitada (**-es**), establezca esta variable de entorno para especificar la ruta de acceso de símbolos.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Cree un nuevo proceso y trace el proceso:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Adjunte MFTrace a un proceso existente:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Enviar la salida del seguimiento a un archivo de texto:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Seguimiento de eventos de ETW o WPP:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> En el primer ejemplo se genera un archivo de texto. En el segundo ejemplo se genera un archivo ETL.

 

Convertir un archivo ETL en un archivo de texto:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Observaciones

De forma predeterminada, MFTrace solo genera seguimientos de desvíos. Para generar seguimientos de ETW o WPP, debe proporcionar un archivo de configuración. El archivo de configuración proporciona los nombres de los proveedores de seguimiento. Para obtener más información, consulte [archivo de configuración de MFTrace](mftrace-configuration-file.md).

MFTrace puede enviar la salida a los destinos siguientes:

-   **stdout** (valor predeterminado).
-   Un archivo de texto.
-   Archivo ETL binario.

Si registra seguimientos de ETW/WPP, un archivo ETL es la opción más eficaz, ya que los datos de seguimiento se guardan como blobs binarios. Una vez completada la sesión de seguimiento, puede usar MFTrace para convertir el archivo ETL en un archivo de texto.

> [!Note]  
> En el seguimiento de desvíos, la salida de texto es tan eficaz como un archivo ETL. Por lo tanto, si solo registra los seguimientos de desvío (sin seguimientos de ETW/WPP), se recomienda la salida de texto.

 

Para el seguimiento de desvíos, debe adjuntar MFTrace a un proceso en ejecución (**-a**) o usar MFTrace para crear un nuevo proceso. En el caso de los seguimientos de ETW/WPP, MFTrace escucha en cualquier proveedor de eventos que se muestra en el archivo de configuración.

Puede filtrar los resultados de seguimiento especificando palabras clave de seguimiento, ya sea mediante la opción de línea de comandos **-k** o en el archivo de configuración. Sin embargo, el uso más habitual es registrar todos los seguimientos y, a continuación, usar un script o **grep** para buscar patrones de cadena concretos.

## <a name="interpreting-the-trace-results"></a>Interpretar los resultados de seguimiento

Puede usar MFTrace para responder a las preguntas sobre lo que ocurre dentro de la aplicación o el componente de Media Foundation. En la tabla siguiente se enumeran algunas preguntas típicas. La segunda columna proporciona la cadena de búsqueda que puede ayudar a responder a la pregunta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pregunta</th>
<th>Búsqueda en las cadenas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>¿Se produjo un error?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>¿La topología se resolvió correctamente?</td>
<td>&quot;CTopologyHelpers:: Trace&quot;</td>
</tr>
<tr class="odd">
<td>¿Se ha iniciado la sesión multimedia?</td>
<td>&quot;MESessionStarted&quot;</td>
</tr>
<tr class="even">
<td>¿Qué archivo se reprodujo?</td>
<td>&quot;CMFSourceResolverDetours&quot;</td>
</tr>
<tr class="odd">
<td>¿Cuáles son los tipos de medios de las secuencias de origen?</td>
<td>&quot;Nuevo flujo &quot; , &quot; MENewStream &quot; , &quot; CMFMediaSourceDetours:: TracePD&quot;</td>
</tr>
<tr class="even">
<td>¿Las secuencias de origen generan ejemplos?</td>
<td>&quot;CMFMediaStreamDetours:: HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>¿Llegó la reproducción hasta el final de los datos?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>¿Cambió el formato?</td>
<td>&quot;MEStreamFormatChanged &quot; (orígenes de medios), &quot; nuevo formato &quot; , &quot; MESessionStreamSinkFormatChanged &quot; (receptores de medios)</td>
</tr>
<tr class="odd">
<td>¿Qué objetos se crearon?</td>
<td>&quot;COle32ExportDetours:: CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>¿El Media Foundation transformaciones (MFTs) de la canalización procesa los datos?</td>
<td>&quot;CMFTransformDetours::P rocessOutput &quot; , &quot; CMFTransformDetours::P rocessinput&quot;</td>
</tr>
<tr class="odd">
<td>¿Qué Estados se establecieron en el MFTs?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>¿Una MFT solicita datos de entrada?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (MFT sincrónico), &quot; METRANSFORMNEEDINPUT &quot; (MFT asincrónico).</td>
</tr>
<tr class="odd">
<td>¿Un MFT asíncrono genera datos de salida?</td>
<td>&quot;ProcessOutputs disponible&quot;</td>
</tr>
<tr class="even">
<td>¿Un receptor de medios solicita ejemplos?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>¿Ha recibido un receptor de medios ejemplos?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: ¿Qué ejemplos se procesaron?</td>
<td>&quot;ejemplo &quot; , &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: ¿Qué gráfico de filtro se usó?</td>
<td>&quot;CGraphHelpers:: Trace&quot;</td>
</tr>
<tr class="even">
<td>¿Había varios procesos?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Busque también el identificador de proceso, que aparece al principio de cada línea de seguimiento.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




