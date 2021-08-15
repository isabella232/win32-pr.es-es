---
description: MFTrace es una herramienta para generar registros de seguimiento para Microsoft Media Foundation aplicaciones.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Uso de MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03cb19f17978236b3e4edd8415f524913c90d99d7a7caf4183dd885d340cfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737328"
---
# <a name="using-mftrace"></a>Uso de MFTrace

MFTrace es una herramienta para generar registros de seguimiento para Microsoft Media Foundation aplicaciones.

MFTrace usa la biblioteca Detours para enlazarse a Media Foundation API y generar registros de seguimiento. MFTrace también puede registrar seguimientos de cualquier componente que use seguimiento de eventos para Windows (ETW) o el preprocesador de seguimiento de software (WPP) para generar seguimientos. Los registros de seguimiento se pueden generar iniciando un nuevo proceso desde MFTrace o adjuntando MFTrace a un proceso existente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]



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
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Id. de proceso o Nombre del proceso</em><br/></td>
<td>Asociar a un proceso en ejecución.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Archivo de configuración</em><br/></td>
<td>Lee la configuración del archivo de configuración especificado. Vea <a href="mftrace-configuration-file.md">Archivo de configuración de MFTrace</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br/></td>
<td>Deshabilite el seguimiento para los procesos secundarios. De forma predeterminada, el seguimiento está habilitado para los procesos secundarios.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Habilitar símbolos públicos.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Palabras clave</em><br/></td>
<td>Lista de palabras clave separadas por comas. Vea <a href="mftrace-keywords.md">Palabras clave de MFTrace</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Nivel</em><br/></td>
<td>Nivel de seguimiento.<br/>
<ul>
<li>0: Ninguno</li>
<li>1: Crítico</li>
<li>2: Error</li>
<li>3: Advertencia</li>
<li>4: Informativo</li>
<li>5: Detallado</li>
<li>16: Depuración</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Archivo de salida</em><br/></td>
<td>Escriba la salida de seguimiento en el archivo especificado. De forma predeterminada, la salida va <strong>a stdout</strong>.<br/> Si se especifica un archivo de salida, la extensión de nombre de archivo debe ser una de las siguientes:<br/>
<ul>
<li>.etl: archivo de registro de seguimiento de eventos (ETL).</li>
<li>.log o .txt: archivo de texto.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Habilite el modo detallado.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Muestra información de uso.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>Comando</em><br/></td>
<td>Argumentos de línea de comandos para crear un nuevo proceso.<br/></td>
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

Para hacer un seguimiento de los componentes que usan el preprocesador de seguimiento de software (WPP) de Windows, establezca esta variable de entorno en para especificar la ruta de acceso a los archivos de formato de mensaje de seguimiento (TMF) para el componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Si la búsqueda de símbolos está habilitada (**-es**), establezca esta variable de entorno para especificar la ruta de acceso del símbolo.

</dd> </dl>

## <a name="examples"></a>Ejemplos

Cree un nuevo proceso y haga un seguimiento de ese proceso:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Adjunte MFTrace a un proceso existente:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Enviar la salida de seguimiento a un archivo de texto:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Seguimiento de eventos ETW o WPP:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> El primer ejemplo genera un archivo de texto. El segundo ejemplo genera un archivo ETL.

 

Convertir un archivo ETL en un archivo de texto:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Observaciones

De forma predeterminada, MFTrace solo genera seguimientos de desviados. Para generar seguimientos ETW o WPP, debe proporcionar un archivo de configuración. El archivo de configuración proporciona los nombres de los proveedores de seguimiento. Para obtener más información, vea [Archivo de configuración de MFTrace](mftrace-configuration-file.md).

MFTrace puede enviar la salida a los siguientes destinos:

-   **stdout** (valor predeterminado).
-   Un archivo de texto.
-   Un archivo ETL binario.

Si va a registrar seguimientos ETW/WPP, un archivo ETL es la opción más eficaz, ya que los datos de seguimiento se guardan como blobs binarios. Una vez completada la sesión de seguimiento, puede usar MFTrace para convertir el archivo ETL en un archivo de texto.

> [!Note]  
> Para el seguimiento de desvía, la salida de texto es tan eficaz como un archivo ETL. Por lo tanto, si solo registra seguimientos de desvía (sin seguimientos ETW/WPP), se recomienda la salida de texto.

 

Para el seguimiento de desviados, debe adjuntar MFTrace a un proceso en ejecución (**-a**) o usar MFTrace para crear un nuevo proceso. En el caso de los seguimientos ETW/WPP, MFTrace escucha a cualquier proveedor de eventos que se muestra en el archivo de configuración.

Puede filtrar los resultados del seguimiento especificando palabras clave de seguimiento, ya sea mediante la opción de línea de comandos **-k** o en el archivo de configuración. Sin embargo, el uso más típico es registrar todos los seguimientos y, a continuación, usar un script o **grep** para buscar patrones de cadena determinados.

## <a name="interpreting-the-trace-results"></a>Interpretación de los resultados de seguimiento

Puede usar MFTrace para responder preguntas sobre lo que sucede dentro de su Media Foundation aplicación o componente. En la tabla siguiente se enumeran algunas preguntas típicas. La segunda columna proporciona la cadena de búsqueda que puede ayudar a responder a la pregunta.



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
<td>¿Se ha producido un error?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>¿Se ha resuelto correctamente la topología?</td>
<td>&quot;CTopologyHelpers::Trace&quot;</td>
</tr>
<tr class="odd">
<td>¿Se ha empezado la sesión multimedia?</td>
<td>&quot;MESessionStarted&quot;</td>
</tr>
<tr class="even">
<td>¿Qué archivo se ha reproducdo?</td>
<td>&quot;CMFSourceResolverDetours&quot;</td>
</tr>
<tr class="odd">
<td>¿Cuáles son los tipos de medios para las secuencias de origen?</td>
<td>&quot;Nueva secuencia &quot; , &quot; MENewStream &quot; , &quot; CMFMediaSourceDetours::TracePD&quot;</td>
</tr>
<tr class="even">
<td>¿Generaron los flujos de origen ejemplos?</td>
<td>&quot;CMFMediaStreamDetours::HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>¿Llegó la reproducción al final de los datos?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>¿Ha cambiado el formato?</td>
<td>&quot;MEStreamFormatChanged &quot; (orígenes multimedia), &quot; Nuevo formato , &quot; &quot; MESessionStreamSinkFormatChanged &quot; (receptores multimedia)</td>
</tr>
<tr class="odd">
<td>¿Qué objetos se crearon?</td>
<td>&quot;COle32ExportDetours::CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>¿Procesó Media Foundation transformación de datos (MFT) en la canalización?</td>
<td>&quot;CMFTransformDetours::ProcessOutput &quot; , &quot; CMFTransformDetours::ProcessInput&quot;</td>
</tr>
<tr class="odd">
<td>¿Qué estados se han establecido en las MTA?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>¿Ha solicitado un MFT datos de entrada?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (MFT sincrónico), &quot; METransformNeedInput &quot; (MFT asincrónico).</td>
</tr>
<tr class="odd">
<td>¿Produjo un MFT asincrónico datos de salida?</td>
<td>&quot;ProcessOutputs disponible&quot;</td>
</tr>
<tr class="even">
<td>¿Ha solicitado un receptor multimedia ejemplos?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>¿Recibió un receptor multimedia ejemplos?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: ¿Qué muestras se han procesado?</td>
<td>&quot;sample &quot; , &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: ¿Qué gráfico de filtro se usó?</td>
<td>&quot;CGraphHelpers::Trace&quot;</td>
</tr>
<tr class="even">
<td>¿Hubo varios procesos?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Busque también el identificador del proceso, que aparece al principio de cada línea de seguimiento.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




