---
description: El compilador de Managed Object Format (MOF) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: MOFCOMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908328"
---
# <a name="mofcomp"></a>MOFCOMP

El compilador de [*Managed Object Format (MOF)*](gloss-m.md) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI. Normalmente, los archivos MOF se compilan automáticamente durante la instalación de los sistemas con los que se proporcionan, pero también puede compilar archivos MOF con esta herramienta.

Para obtener más información acerca de la búsqueda y el uso de mofcomp.exe, consulte [uso de las herramientas de administración de WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .

En el ejemplo de código siguiente se muestra cómo ejecutar el compilador MOF en un archivo.

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>Conmutadores

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-Autorrecuperación**
</dt> <dd>

Agrega el archivo MOF con nombre a la lista de archivos compilados durante la recuperación del repositorio. La lista de archivos MOF de Autorrecuperación se almacena en la clave del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

Los archivos MOF que aparecen en esta entrada del registro deben residir en el equipo local, ya que los archivos MOF que utilizan el comando **Autorrecuperación** no pueden recuperar archivos MOF ubicados en un equipo remoto.

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el [*repositorio WMI*](gloss-w.md) si WMI tiene un error y se reinician, use la instrucción de preprocesador [**\# pragma autocover**](pragma-autorecover.md) en el archivo [*Managed Object Format*](gloss-m.md) (MOF).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-comprobar**
</dt> <dd>

Solicita que el compilador realice una comprobación de sintaxis únicamente e imprima los mensajes de error correspondientes. No se puede usar ningún otro conmutador con este modificador. Cuando se utiliza este modificador, no se establece ninguna conexión a Instrumental de administración de Windows (WMI) y no se realiza ninguna modificación en el repositorio WMI.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _namespacepath_*_>_*
</dt> <dd>Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*. El MOF compilado se carga en el espacio de nombres de MOFCOMP predeterminado, raíz \\ predeterminado, a menos que se use este modificador. También puede insertar el comando de preprocesador **\# pragma ("**_ruta de acceso de espacio de nombres_*_")_* en el archivo MOF para lograr el mismo efecto. Si se usan el modificador **-N:** y el comando de \# <a href="pragma-namespace.md">espacio de nombres pragma</a> , la Autorrecuperación del \# **espacio de nombres de pragma**  tiene prioridad. En este caso, la única manera de compilar el MOF en otro espacio de nombres es editar el archivo MOF y cambiar el \# comando **pragma namespace** . Se puede especificar un equipo remoto mediante el \\ \\ valor predeterminado de MachineName \\ raíz \\ .</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-clase: createonly**
</dt> <dd>

Solicita que el compilador no realice ningún cambio en las clases existentes. Cuando se utiliza este modificador, la operación de compilación finaliza si ya existe una clase especificada en el archivo MOF.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class: ForceUpdate**
</dt> <dd>

Fuerza la actualización de las clases cuando existen clases secundarias en conflicto. Por ejemplo, supongamos que se define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador. En el modo de **clase: ForceUpdate** , el compilador MOF resuelve este conflicto eliminando el calificador en conflicto de la clase secundaria. Si la clase secundaria tiene instancias, se produce un error en la actualización forzada.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-clase: safeupdate**
</dt> <dd>

Permite actualizaciones de clases aunque haya clases secundarias, siempre y cuando el cambio no cause conflictos con las clases secundarias. Por ejemplo, esta marca permite agregar una nueva propiedad a la clase base que no se mencionó anteriormente en las clases secundarias. Si las clases secundarias tienen instancias, se produce un error en la actualización.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-clase: updateonly**
</dt> <dd>

Solicita que el compilador no cree nuevas clases. Cuando se utiliza este modificador, la operación de compilación finaliza si no existe una clase especificada en el archivo MOF.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instancia: updateonly**
</dt> <dd>

Solicita que el compilador no cree instancias nuevas. Cuando se utiliza este modificador, la operación de compilación finaliza si no existe una instancia especificada en el archivo MOF.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instancia: createonly**
</dt> <dd>

Solicita que el compilador no realice ningún cambio en las instancias existentes. Cuando se utiliza este modificador, la operación de compilación finaliza si ya existe una instancia especificada en el archivo MOF.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _nombre de archivo_*_>_*
</dt> <dd>

Solicita que el compilador cree una versión binaria del archivo MOF con el nombre *filename* sin realizar ninguna modificación en el repositorio WMI.

Si usa la opción **-B: <** _nombre_ de *_>_* archivo para crear un archivo MOF binario, solo se almacenan los tipos de calificador predeterminados en el repositorio WMI.

El formato MOF binario es el formato intermedio para combinar un controlador WDM con el MOF como un recurso. MOF binario representa las clases y las instancias de la misma forma que un archivo MOF de texto y se comprimen antes de almacenarse en el disco.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Solicita que el compilador realice una comprobación de la sintaxis de WMI. El modificador **-B:** debe usarse con este modificador. El modificador **-WMI** solo se usa para compilar archivos MOF binarios para su uso por parte de controladores de dispositivos WDM. Este modificador invoca un comprobador de archivos MOF binario independiente, que se ejecuta después de crear el archivo MOF binario.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: contraseña de <** *_>_*
</dt> <dd>

Especifica la *contraseña* que el usuario del equipo debe especificar al iniciar sesión.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _nombre de usuario_*_>_*
</dt> <dd>

Especifica *username* como el nombre del usuario que inicia sesión.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: entidad de <** *_>_*
</dt> <dd>

Especifica la *autoridad* como la entidad (nombre de dominio) que se va a usar al iniciar sesión en WMI.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: <** _ruta de acceso_*_>_*
</dt> <dd>

Nombre de la salida independiente del idioma. Se usa con el modificador **-enmiendas** para especificar el nombre del archivo MOF independiente del idioma que se generará.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: ruta de acceso de <** *_>_*
</dt> <dd>

Nombre de la salida específica del idioma. Se usa con el modificador **-enmiendas** para especificar el nombre del archivo MOF específico del idioma que se generará.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Enmienda:** _configuración regional_ de <*_>_*
</dt> <dd>

Divide el archivo MOF en versiones independientes del lenguaje y específicas. El compilador MOF crea una forma independiente del idioma del archivo MOF que tiene todos los calificadores modificados que se han quitado. También se crea una versión localizada del archivo MOF con una extensión de nombre de archivo MFL. El parámetro *locale* especifica el nombre del espacio de nombres secundario que contiene las definiciones de clase localizadas. El formato del parámetro de *configuración regional* es ms \_ xxx, donde xxx es el valor hexadecimal del LCID de Windows. Por ejemplo, la configuración regional de inglés americano es MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _ResourceName_*_>_*
</dt> <dd>

Extrae MOF binario de un recurso con nombre. Este modificador obtiene el MOF binario de la clase en el repositorio WMI, mientras que el modificador-B crea el formato MOF binario a partir de un archivo MOF.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*
</dt> <dd>

Opcional. Extrae las descripciones de MOF localizadas del MOF binario cuando se usa con el modificador-ER.

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

Nombre del archivo que se va a analizar.

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Como primera operación, el compilador MOF realiza una comprobación de sintaxis en el archivo MOF. Si el compilador encuentra algún error, imprime un mensaje de error y finaliza el proceso.

El compilador MOF puede devolver los valores siguientes:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Operación de compilación de MOF realizada correctamente.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

El compilador MOF no se pudo conectar con el servidor WMI. Esto se debe a un error semántico, como una incompatibilidad con el repositorio WMI existente o un error real, como el error del servidor WMI en iniciarse.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Uno o varios modificadores de la línea de comandos no son válidos.

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Error de sintaxis de MOF.

</dd> </dl>

Si el archivo MOF se analiza correctamente, pero se realiza un intento de realizar una operación prohibida por un modificador de la línea de comandos, el compilador devuelve un código de error generado por WMI en lugar de cualquiera de los códigos de retorno que aparecen en la lista anterior. Por ejemplo, se devuelve un código de error de WMI cuando se especifica el modificador **-Instance: updateonly** y el archivo MOF intenta crear una instancia.

Si la instrucción [**\# pragma autorecover**](pragma-autorecover.md) preprocesser no está en el archivo, se devuelve la siguiente ADVERTENCIA:

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Observaciones

El compilador MOF está disponible en el directorio% WINDIR% \\ system32 \\ WBEM. Debe especificar el archivo MOF como el parámetro del compilador MOF. También puede especificar un modificador de Autorrecuperación si desea que el archivo MOF se vuelva a compilar automáticamente si alguna vez el repositorio CIM tiene que recuperarse automáticamente. Para obtener más información, escriba **MOFCOMP/?** en el símbolo del sistema.

Un archivo MOF que utiliza el juego de caracteres Unicode contiene una firma como los dos primeros bytes del archivo. Esta firma es U + FFFE o U + FEFF, dependiendo del orden de bytes del archivo.

Cuando no se producen errores en el proceso de análisis, el compilador MOF se conecta al servidor WMI que se ejecuta en el equipo local, a menos que se especifique el modificador **-check** . Las clases e instancias definidas en el archivo MOF se agregan al repositorio WMI.

Cuando se produce un error al actualizar el repositorio WMI, el compilador no intenta devolver el repositorio a su estado anterior a que el compilador comenzó el procesamiento.

**Windows 8:** Al instalar un proveedor, MOFCOMP trata los \[ \] calificadores de clave y \[ estáticos \] como true si están presentes, independientemente de sus valores reales. Otros calificadores se tratan como false si están presentes pero no se establecen explícitamente en true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**pragma (espacio de nombres)**](pragma-namespace.md)
</dt> <dt>

[Compilar archivos MOF](compiling-mof-files.md)
</dt> <dt>

[Compilar archivos MOF localizados](compiling-localized-mof-files.md)
</dt> <dt>

[Registrar un proveedor](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler::CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

