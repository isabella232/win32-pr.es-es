---
description: MFTrace es una herramienta para generar registros de seguimiento para Microsoft Media Foundation aplicaciones.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Uso de MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579796"
---
# <a name="using-mftrace"></a>Uso de MFTrace

MFTrace es una herramienta para generar registros de seguimiento para Microsoft Media Foundation aplicaciones.

MFTrace usa la biblioteca Detours para enlazarse a las Media Foundation API y generar registros de seguimiento. MFTrace también puede registrar seguimientos de cualquier componente que use seguimiento de eventos para Windows (ETW) o el preprocesador de seguimiento de software (WPP) para generar seguimientos. Los registros de seguimiento se pueden generar iniciando un nuevo proceso desde MFTrace o adjuntando MFTrace a un proceso existente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]




| Argumentos de la línea de comandos | Descripción | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Id. de proceso o Nombre del proceso</em><br /> | Asociar a un proceso en ejecución.<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Archivo de configuración</em><br /> | Lee la configuración del archivo de configuración especificado. Vea <a href="mftrace-configuration-file.md">Archivo de configuración de MFTrace</a>.<br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br /> | Deshabilite el seguimiento para los procesos secundarios. De forma predeterminada, el seguimiento está habilitado para los procesos secundarios.<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | Habilitar símbolos públicos.<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Palabras clave</em><br /> | Lista de palabras clave separadas por comas. Vea <a href="mftrace-keywords.md">Palabras clave de MFTrace</a>.<br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Nivel</em><br /> | Nivel de seguimiento.<br /><ul><li>0: Ninguno</li><li>1: Crítico</li><li>2: Error</li><li>3: Advertencia</li><li>4: Informativo</li><li>5: Detallado</li><li>16: Depuración</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Archivo de salida</em><br /> | Escriba la salida de seguimiento en el archivo especificado. De forma predeterminada, la salida va <strong>a stdout</strong>.<br /> Si se especifica un archivo de salida, la extensión de nombre de archivo debe ser una de las siguientes:<br /><ul><li>.etl: archivo de registro de seguimiento de eventos (ETL).</li><li>.log o .txt: archivo de texto.</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | Habilite el modo detallado.<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | Muestra información de uso.<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>COMANDO</em><br /> | Argumentos de línea de comandos para crear un nuevo proceso.<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | Nombre de un archivo ETL existente. Si se proporciona este argumento, el archivo ETL se convierte en salida de texto.<br /> | 




 

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




| Pregunta | Búsqueda en las cadenas | 
|----------|----------------|
| ¿Se ha producido un error? | "0xc00d" | 
| ¿Se ha resuelto correctamente la topología? | "CTopologyHelpers::Trace" | 
| ¿Se ha empezado la sesión multimedia? | "MESessionStarted" | 
| ¿Qué archivo se ha reproducdo? | "CMFSourceResolverDetours" | 
| ¿Cuáles son los tipos de medios para las secuencias de origen? | "New stream", "MENewStream", "CMFMediaSourceDetours::TracePD" | 
| ¿Generaron los flujos de origen ejemplos? | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| ¿Llegó la reproducción al final de los datos? | "MEEndOfStream", "MEEndOfPresentation" | 
| ¿Ha cambiado el formato? | "MEStreamFormatChanged" (orígenes multimedia), "Nuevo formato", "MESessionStreamSinkFormatChanged" (receptores multimedia) | 
| ¿Qué objetos se crearon? | "COle32ExportDetours::CoCreateInstance" | 
| ¿Procesó Media Foundation transformación de datos (MTA) en la canalización? | "CMFTransformDetours::P rocessOutput", "CMFTransformDetours::P rocessInput" | 
| ¿Qué estados se han establecido en las MTA? | "CMFTransformDetours::P rocessMessage" | 
| ¿Ha solicitado un MFT datos de entrada? | "MF_E_TRANSFORM_NEED_MORE_INPUT" (MFT sincrónico), "METransformNeedInput" (MFT asincrónico). | 
| ¿Produjo un MFT asincrónico datos de salida? | "ProcessOutputs available" | 
| ¿Ha solicitado un receptor multimedia ejemplos? | "MEStreamSinkRequestSample" | 
| ¿Recibió un receptor multimedia ejemplos? | "CMFStreamSinkDetours::P rocessSample" | 
| DirectShow: ¿Qué muestras se han procesado? | "sample", "CMemInputPinDetours" | 
| DirectShow: ¿Qué gráfico de filtro se usó? | "CGraphHelpers::Trace" | 
| ¿Hubo varios procesos? | "CreateProcess"<blockquote>[!Note]<br />Busque también el identificador del proceso, que aparece al principio de cada línea de seguimiento.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




