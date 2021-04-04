---
description: 'WsdCodeGen tiene dos funciones: generar archivos de configuración y generar código fuente para las aplicaciones de cliente y host de WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Sintaxis de la línea de comandos WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908541"
---
# <a name="wsdcodegen-command-line-syntax"></a>Sintaxis de la línea de comandos WsdCodeGen

WsdCodeGen tiene dos funciones: generar archivos de configuración y generar código fuente para las aplicaciones de cliente y host de WSDAPI. En este tema se proporciona la sintaxis de línea de comandos que se usa para realizar cada tarea.

## <a name="generating-a-configuration-file"></a>Generar un archivo de configuración

### <a name="syntax"></a>Sintaxis

**WSDCODEGEN.EXE** **/generateconfig:**{**cliente** \| **host** \| **All**} **\[ /OutputFile:**_nombrearchivoconfig_ *_\]_* *WSDLFileNameList*

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {cliente \| host \| todos}**
</dt> <dd>

El tipo de código que generará el archivo de configuración de salida. **/generateconfig: el cliente** se usa para generar un archivo de configuración para generar el código de cliente, **/generateconfig: host** se usa para generar un archivo de configuración para generar el código de host y **/generateconfig: ALL** se usa para generar un archivo de configuración para generar el cliente y el código del host.

</dd> <dt>

<span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_nombrearchivoconfig_
</dt> <dd>

Este parámetro opcional se usa para especificar el nombre de archivo del archivo de configuración de salida. Si se excluye este parámetro, se codegen.config el nombre del archivo de configuración de salida.

</dd> <dt>

<span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*
</dt> <dd>

Incluya una plantilla PnP-X en el archivo de configuración.

</dd> <dt>

<span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*
</dt> <dd>

Una lista delimitada por espacios de los archivos WSDL que va a procesar WsdCodeGen.

</dd> </dl>

## <a name="generating-source-code"></a>Generar código fuente

### <a name="syntax"></a>Sintaxis

**WSDCODEGEN.EXE** **/GenerateCode** **\[ /download \]** **\[ /GBC \]** **\[ outputroot:**_ruta de acceso_ *_\]_* **\[ /writeaccess:**_comando_ *_\]_* *nombrearchivoconfig*

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**
</dt> <dd>

Indica a WsdCodeGen que genere código fuente. Este es el modo predeterminado si no se especifica ningún modo.

</dd> <dt>

<span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**
</dt> <dd>

Descarga los documentos importados a los que hace referencia el archivo de configuración. Este parámetro es opcional.

</dd> <dt>

<span id="_gbc"></span><span id="_GBC"></span>**/gbc**
</dt> <dd>

Agrega comentarios al código fuente que indica que se ha generado el código. Estos comentarios llevan como prefijo la frase "generada por". Este parámetro es opcional.

</dd> <dt>

<span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_ruta de acceso_
</dt> <dd>

La ubicación de salida para los archivos generados. la *ruta de acceso* puede ser una ruta de acceso absoluta o relativa. Este parámetro es opcional.

</dd> <dt>

<span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_comando_
</dt> <dd>

Indica a WsdCodeGen que ejecute el comando especificado antes de modificar los archivos existentes en el disco. Los archivos de salida que sean idénticos a los del disco no recibirán este comando ni se escribirán en él. Si el comando contiene la secuencia " {0} ", esta secuencia se reemplazará por el nombre del archivo que se va a modificar. De lo contrario, el nombre de archivo se anexará al comando.

Ejemplos:

**/writeaccess: "attrib-r"**

**/writeaccess: "attrib-r {0} "**

**/writeaccess: "Copy {0} .. \\ copia de seguridad \\ "**

</dd> <dt>

<span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nombrearchivoconfig*
</dt> <dd>

Nombre del archivo de configuración que se va a procesar antes de generar el código.

</dd> </dl>

## <a name="formatting-legend"></a>Leyenda de formato



| Formato                                                                    | Significado                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| *Cursiva*                                                                  | Información que el usuario debe proporcionar                  |
| **Negrita**                                                                  | Elementos que el usuario debe escribir exactamente como se indica       |
| Entre corchetes ( \[ \] )                                                   | Elementos opcionales                                          |
| Entre llaves ( {} ); opciones separadas por canalización ( \| ). Ejemplo: { \| impares} | Conjunto de opciones de las que el usuario debe elegir sólo una. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración WsdCodeGen](wsdcodegen-configuration-file.md)
</dt> <dt>

[Usar WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 




