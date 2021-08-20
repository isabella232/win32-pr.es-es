---
description: El compilador Managed Object Format (MOF) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58821d99dfc816957684ad083710043502394b470548b2cf638a41ded850dc56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923540"
---
# <a name="mofcomp"></a>mofcomp

El [*compilador Managed Object Format (MOF)*](gloss-m.md) analiza un archivo que contiene instrucciones MOF y agrega las clases y las instancias de clase definidas en el archivo al repositorio WMI. Normalmente, los archivos MOF se compilan automáticamente durante la instalación de los sistemas con los que se proporcionan, pero también se pueden compilar archivos MOF mediante esta herramienta.

Para obtener más información sobre cómo buscar y usar mofcomp.exe, vea [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Para obtener información sobre cómo quitar clases e instancias del repositorio WMI, vea el comando [**pragma deleteclass**](pragma-deleteclass.md) de preprocesador.

En el ejemplo de código siguiente se muestra cómo ejecutar el compilador MOF en un archivo .

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

## <a name="switches"></a>Modificadores

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**
</dt> <dd>

Agrega el archivo MOF con nombre a la lista de archivos compilados durante la recuperación del repositorio. La lista de archivos MOF de autorrecuperación se almacena en la clave del Registro:

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

Los archivos MOF enumerados en esta entrada del Registro deben  residir en el equipo local porque los archivos MOF que usan el comando de recuperación automática no pueden recuperar archivos MOF ubicados en un equipo remoto.

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el repositorio [*WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) en el archivo [*Managed Object Format*](gloss-m.md) (MOF).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-check**
</dt> <dd>

Solicita que el compilador realice solo una comprobación de sintaxis e imprima los mensajes de error adecuados. No se puede usar ningún otro modificador con este modificador. Cuando se usa este modificador, no se establece ninguna conexión a Windows Management Instrumentation (WMI) y no se realiza ninguna modificación en el repositorio WMI.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<** _namespacepath_*_>_*
</dt> <dd>Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*. El MOF compilado se carga en el espacio de nombres Mofcomp predeterminado, el valor predeterminado raíz, a menos \\ que se utilice este modificador. También puede insertar el espacio de nombres **\# pragma** del comando de preprocesador (" ruta de acceso del espacio de nombres *_")_* en el archivo MOF para lograr el mismo efecto. Si se usan **el modificador -N:** y el comando \# <a href="pragma-namespace.md">pragma namespace,</a> la recuperación automática del espacio de nombres \# **pragma**  tiene prioridad. En este caso, la única manera de compilar el MOF en otro espacio de nombres es editar el archivo MOF y cambiar el \# **comando pragma namespace.** Se puede especificar un equipo remoto mediante el \\ \\ valor predeterminado raíz \\ machinename. \\</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**
</dt> <dd>

Solicita que el compilador no realice ningún cambio en las clases existentes. Cuando se usa este modificador, la operación de compilación finaliza si ya existe una clase especificada en el archivo MOF.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**
</dt> <dd>

Fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto. Por ejemplo, suponga que un calificador de clase está definido en una clase secundaria y la clase base intenta agregar el mismo calificador. En **el modo -class:forceupdate,** el compilador MOF resuelve este conflicto eliminando el calificador en conflicto en la clase secundaria. Si la clase secundaria tiene instancias, se produce un error en la actualización forzada.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**
</dt> <dd>

Permite actualizaciones de clases incluso si hay clases secundarias, siempre que el cambio no cause conflictos con las clases secundarias. Por ejemplo, esta marca permite agregar una nueva propiedad a la clase base que no se mencionó anteriormente en las clases secundarias. Si las clases secundarias tienen instancias, se produce un error en la actualización.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**
</dt> <dd>

Solicita que el compilador no cree clases nuevas. Cuando se usa este modificador, la operación de compilación finaliza si no existe una clase especificada en el archivo MOF.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**
</dt> <dd>

Solicita que el compilador no cree ninguna instancia nueva. Cuando se usa este modificador, la operación de compilación finaliza si no existe una instancia especificada en el archivo MOF.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**
</dt> <dd>

Solicita que el compilador no realice ningún cambio en las instancias existentes. Cuando se usa este modificador, la operación de compilación finaliza si ya existe una instancia especificada en el archivo MOF.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<** _nombre de archivo_*_>_*
</dt> <dd>

Solicita que el compilador cree una versión binaria del archivo MOF con el nombre *filename* sin realizar ninguna modificación en el repositorio WMI.

Si usa la **opción -B:<** _filename_ para crear un archivo MOF binario, solo se almacenan los tipos de calificador predeterminados en *_>_* el repositorio WMI.

El formato MOF binario es el formato intermedio para combinar un controlador WDM con el MOF como recurso. El MOF binario representa clases e instancias del mismo modo que lo hace un archivo MOF de texto y se comprime antes de almacenarse en el disco.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Solicita que el compilador realice una comprobación de sintaxis wmi. El **modificador -B:** debe usarse con este modificador. El **modificador -WMI** solo se usa para compilar archivos MOF binarios para que los usen los controladores de dispositivos WDM. Este modificador invoca un comprobación de archivos MOF binario independiente, que se ejecuta después de crear el archivo MOF binario.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<** _password_*_>_*
</dt> <dd>

Especifica Contraseña *como contraseña* para que el usuario del equipo escriba al iniciar sesión.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<** _UserName_*_>_*
</dt> <dd>

Especifica *UserName como* nombre del usuario que inicia sesión.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<** _Authority_*_>_*
</dt> <dd>

Especifica Autoridad *como autoridad* (nombre de dominio) que se usará al iniciar sesión en WMI.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<** _ruta de acceso_*_>_*
</dt> <dd>

Nombre de la salida neutra del idioma. Se usa con **el modificador -AMENDMENT** para especificar el nombre del archivo MOF neutral del lenguaje que se generará.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<** _ruta de acceso_*_>_*
</dt> <dd>

Nombre de la salida específica del idioma. Se usa con **el modificador -AMENDMENT** para especificar el nombre del archivo MOF específico del lenguaje que se generará.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<** _locale_*_>_*
</dt> <dd>

Divide el archivo MOF en versiones específicas y neutras del lenguaje. El compilador de MOF crea una forma neutra del lenguaje del archivo MOF que ha quitado todos los calificadores modificados. También se crea una versión localizada del archivo MOF con una extensión de nombre de archivo MFL. El *parámetro Locale* especifica el nombre del espacio de nombres secundario que contiene las definiciones de clase localizadas. El formato del parámetro *Locale* es MS xxx, donde xxx es el valor hexadecimal del Windows \_ LCID. Por ejemplo, la configuración regional del inglés estadounidense es MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _ResourceName_*_>_*
</dt> <dd>

Extrae el MOF binario de un recurso con nombre. Este modificador obtiene el MOF binario de la clase en el repositorio WMI, mientras que el modificador -B crea el formato MOF binario a partir de un archivo MOF.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<** _ResourceLocale_*_>_*
</dt> <dd>

Opcional. Extrae las descripciones de MOF localizadas del MOF binario cuando se usa con el modificador -ER.

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

Nombre del archivo que se analizará.

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Como primera operación, el compilador de MOF realiza una comprobación de sintaxis en el archivo MOF. Si el compilador encuentra algún error, imprime un mensaje de error y el proceso finaliza.

El compilador MOF puede devolver los valores siguientes:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

La operación de compilación de MOF se ha realizado correctamente.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

El compilador MOF no se pudo conectar con el servidor WMI. Esto se debe a un error semántico, como una incompatibilidad con el repositorio WMI existente o a un error real, como el error de inicio del servidor WMI.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Uno o varios modificadores de línea de comandos no eran válidos.

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Error de sintaxis de MOF.

</dd> </dl>

Si el archivo MOF se analiza correctamente, pero se intenta realizar una operación prohibida por un modificador de línea de comandos, el compilador devuelve un código de error generado por WMI en lugar de cualquiera de los códigos de retorno enumerados en la lista anterior. Por ejemplo, se devuelve un código de error wmi cuando se especifica el modificador **-instance:updateonly** y el archivo MOF intenta crear una instancia.

Si la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) no está en el archivo, se devuelve la siguiente advertencia:

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Comentarios

El compilador MOF está disponible en el directorio wbem %Windir% \\ \\ System32. Debe especificar el archivo MOF como parámetro del compilador de MOF. También puede especificar un modificador de autorrecuperación si desea que el archivo MOF se vuelva a compilar automáticamente si alguna vez se tiene que recuperar automáticamente el repositorio CIM. Para obtener más información, escriba **Mofcomp /?** en el símbolo del sistema.

Un archivo MOF que usa el juego de caracteres Unicode contiene una firma como los dos primeros bytes del archivo. Esta firma es U+FFFE o U+FEFF, dependiendo de la ordenación de bytes del archivo.

Cuando no se produce ningún error en el proceso de análisis, el compilador de MOF se conecta al servidor WMI que se ejecuta en el equipo local a menos que se especifique el modificador **-check.** Las clases e instancias definidas en el archivo MOF se agregan al repositorio WMI.

Cuando se produce un error al actualizar el repositorio WMI, el compilador no intenta devolver el repositorio a su estado antes de que el compilador empezara a procesarse.

**Windows 8:** Al instalar un proveedor, mofcomp trata los calificadores Key y Static como true si están presentes, independientemente \[ de sus \] valores \[ \] reales. Otros calificadores se tratan como false si están presentes, pero no se establecen explícitamente en true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**pragma (espacio de nombres)**](pragma-namespace.md)
</dt> <dt>

[Compilación de archivos MOF](compiling-mof-files.md)
</dt> <dt>

[Compilación de archivos MOF localizados](compiling-localized-mof-files.md)
</dt> <dt>

[Registro de un proveedor](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler::CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

