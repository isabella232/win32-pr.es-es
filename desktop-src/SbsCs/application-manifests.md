---
description: Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifiestos de aplicación
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230241"
---
# <a name="application-manifests"></a>Manifiestos de aplicación

Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución. Deben ser las mismas versiones de ensamblado utilizadas para probar la aplicación. Los manifiestos de aplicación también describen los metadatos para archivos privados de la aplicación.

Para obtener una lista completa del esquema XML, vea [Esquema de archivo de manifiesto.](manifest-file-schema.md)

Los manifiestos de aplicación tienen los siguientes elementos y atributos.

| Elemento                               | Atributos                | Requerido |
|---------------------------------------|---------------------------|----------|
| **ensamblado**                          |                           | Sí      |
|                                       | **manifestVersion**       | Sí      |
| **noInherit**                         |                           | No       |
| **Assemblyidentity**                  |                           | Sí      |
|                                       | **type**                  | Sí      |
|                                       | **name**                  | Sí      |
|                                       | **language**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Sí      |
|                                       | **Publickeytoken**        | No       |
| **Compatibilidad**                     |                           | No       |
| **application**                       |                           | No       |
| **supportedOS**                       | **Id**                    | No       |
| **maxversiontested**                  | **Id**                    | No       |
| **Dependencia**                        |                           | No       |
| **dependentAssembly**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **name**                  | No       |
|                                       | **hashalg**               | No       |
|                                       | **hash**                  | No       |
| **activeCodePage**                    |                           | No       |
| **autoElevate**                       |                           | No       |
| **disableTheming**                    |                           | No       |
| **disableWindowFiltering**            |                           | No       |
| **pppAware**                          |                           | No       |
| **pppAwareness**                      |                           | No       |
| **gdiScaling**                        |                           | No       |
| **highResolutionScrollingAware**      |                           | No       |
| **longPathAware**                     |                           | No       |
| **printerDriverIsolation**            |                           | No       |
| **ultraHighResolutionScrollingAware** |                           | No       |
| **msix**                              |                           | No       |
| **heapType**                          |                           | No       |

## <a name="file-location"></a>Ubicación del archivo

Los manifiestos de aplicación deben incluirse como un recurso en el archivo EXE o dll de la aplicación.

Para obtener más información, vea [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de .manifest.

Por ejemplo, un manifiesto de aplicación que hace referencia a example.exe o example.dll usaría la siguiente sintaxis de nombre de archivo. Puede omitir el identificador <*de recurso>* campo si el identificador de recurso es 1.

**example.exe.<*id. de recurso*>.manifest**

**example.dll.<*id. de recurso*>.manifest**

## <a name="elements"></a>Elementos

Los nombres de elementos y atributos distinguen mayúsculas de minúsculas. Los valores de elementos y atributos no tienen en cuenta las mayúsculas y minúsculas, excepto el valor del atributo type.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>ensamblado

Elemento contenedor. Su primer subelemento debe ser **un elemento noInherit** **o assemblyIdentity.** Necesario.

El **elemento** de ensamblado debe estar en el espacio de nombres "urn:schemas-microsoft-com:asm.v1". Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, mediante herencia o etiquetado.

El **elemento** assembly tiene los siguientes atributos.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El **atributo manifestVersion** debe establecerse en 1.0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Incluya este elemento en un manifiesto de aplicación para establecer los contextos de activación [generados](activation-contexts.md) a partir del manifiesto con la marca "no inherit". Cuando esta marca no se establece en un contexto de activación y el contexto de activación está activo, lo heredan los nuevos subprocesos en el mismo proceso, ventanas, procedimientos de ventana y llamadas a [procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls). Establecer esta marca impide que el nuevo objeto herede el contexto activo.

El **elemento noInherit** es opcional y normalmente se omite. La mayoría de los ensamblados no funcionan correctamente mediante un contexto de activación que no hereda porque el ensamblado debe diseñarse explícitamente para administrar la propagación de su propio contexto de activación. El uso del **elemento noInherit** requiere que los ensamblados dependientes a los que hace referencia el manifiesto de aplicación tengan **un elemento noInherit** en su manifiesto [de ensamblado.](assembly-manifests.md)

Si **noInherit se** usa en un manifiesto, debe ser el primer subelemento del **elemento de** ensamblado. El **elemento assemblyIdentity** debe ir inmediatamente después del **elemento noInherit.** Si **no se usa noInherit,** **assemblyIdentity** debe ser el primer subelemento del **elemento de** ensamblado. El **elemento noInherit** no tiene elementos secundarios. No es un elemento válido en los [manifiestos de ensamblado.](assembly-manifests.md)

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como primer subelemento de un elemento **de** ensamblado, **assemblyIdentity** describe e identifica de forma única la aplicación propietaria de este manifiesto de aplicación. Como primer subelemento de un **elemento dependentAssembly,** **assemblyIdentity** describe un ensamblado en paralelo requerido por la aplicación. Tenga en cuenta que todos los ensamblados a los que se hace referencia en el manifiesto de aplicación requieren una **assemblyIdentity** que coincida exactamente con **assemblyIdentity** en el propio manifiesto de ensamblado del ensamblado al que se hace referencia.

El **elemento assemblyIdentity** tiene los atributos siguientes. No tiene subelementos.

| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de aplicación o ensamblado. El valor debe ser Win32 y todo en minúsculas. Necesario.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Nombra de forma única la aplicación o el ensamblado. Use el formato siguiente para el nombre: Organization.Division.Name. Por ejemplo, Microsoft.Windows.mysampleApp. Necesario.                                                                                                                                                                                                                                                               |
| **language**              | Identifica el idioma de la aplicación o ensamblado. Opcional. Si la aplicación o el ensamblado son específicos del lenguaje, especifique el código de lenguaje DHTML. En **assemblyIdentity de una** aplicación destinada a uso internacional (idioma neutro) omita el atributo language.<br/> En un **ensambladoIdentidad de** un ensamblado destinado a uso internacional (idioma neutro) establezca el valor de language en " \* ".<br/> |
| **processorArchitecture** | Especifica el procesador. Entre los valores válidos se incluyen `x86`, `amd64`, `arm` y `arm64`. Opcional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Especifica la versión de la aplicación o del ensamblado. Use el formato de versión de cuatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada una de las partes separadas por puntos puede ser de 0 a 65535, ambos incluidos. Para obtener más información, vea [Versiones de ensamblado.](assembly-versions.md) Necesario.                                                                                                                                                                        |
| **Publickeytoken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma la aplicación o el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Necesario para todos los ensamblados en paralelo compartidos.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilidad

Contiene al menos una **aplicación**. No tiene atributos. Opcional. Los manifiestos de aplicación sin un elemento de compatibilidad tienen como valor predeterminado la compatibilidad de Windows Vista en Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Contiene al menos un **elemento supportedOS.** A partir Windows 10, versión 1903, también puede contener un **elemento maxversiontested** opcional. No tiene atributos. Opcional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

El **elemento supportedOS** tiene el atributo siguiente. No tiene subelementos.

| Atributo | Descripción   |
|-----------|-----------------------|
| **Id**    | Establezca el atributo Id en **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para ejecutar la aplicación mediante la funcionalidad vista. Esto puede permitir que una aplicación diseñada para Windows Vista se ejecute en un sistema operativo posterior. <br/> Establezca el atributo Id en **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para ejecutar la aplicación con la funcionalidad de Windows 7.<br/> Las aplicaciones que admiten Windows Vista, Windows 7 y Windows 8 no requieren manifiestos independientes. En este caso, agregue los GUID para todos los sistemas operativos Windows.<br/> Para obtener información sobre el **comportamiento del** atributo Id en Windows, vea la guía Windows 8 y compatibilidad de Windows [Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Los siguientes GUID se corresponden con los sistemas operativos indicados:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 y Windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 y Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 y Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 y Windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista y Windows Server 2008<br/> Para probar esto en Windows 7 o Windows 8.x, ejecute Monitor de recursos (resmon), vaya a la pestaña CPU, haga clic con el botón derecho en las etiquetas de columna, "Seleccionar columna..." y active "Contexto del sistema operativo". En Windows 8.x, también puede encontrar esta columna disponible en el Administrador de tareas (taskmgr). El contenido de la columna muestra el valor más alto encontrado o "Windows Vista" como valor predeterminado. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

El **elemento maxversiontested** especifica las versiones de Windows con las que se ha probado la aplicación a partir de la versión mínima del sistema operativo que admite la aplicación hasta la versión máxima. El conjunto completo de versiones se puede encontrar [aquí.](https://developer.microsoft.com/windows/downloads/sdk-archive/) Esto está pensado para que lo usen las aplicaciones de escritorio que usan islas [XAML](/windows/apps/desktop/modernize/xaml-islands) y que no se implementan en un paquete MSIX. Este elemento se admite en Windows 10, versión 1903 y versiones posteriores.

El **elemento maxversiontested** tiene el atributo siguiente. No tiene subelementos.

| Atributo | Descripción    |
|-----------|----------------|
| **Id**    | Establezca el atributo Id en una cadena de versión de 4 partes que especifique la versión máxima de Windows con la que se probó la aplicación. Por ejemplo, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Contiene al menos un **dependentAssembly**. No tiene atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

El primer subelemento de **dependentAssembly** debe ser un **elemento assemblyIdentity** que describa un ensamblado en paralelo requerido por la aplicación. Cada **dependentAssembly debe** estar dentro de exactamente una **dependencia**. No tiene atributos.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>archivo

Especifica los archivos que son privados para la aplicación. Opcional.

El **elemento** file tiene los atributos que se muestran en la tabla siguiente.



| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nombre del archivo. Por ejemplo, Comctl32.dll.                                                            |
| **hashalg** | Algoritmo utilizado para crear un hash del archivo. Este valor debe ser SHA1.                                 |
| **hash**    | Hash del archivo al que se hace referencia por nombre. Cadena hexadecimal de longitud en función del algoritmo hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Forzar que un proceso use UTF-8 como página de códigos del proceso.

**activeCodePage se** agregó en la versión 1903 de Windows (actualización de mayo de 2019). Puede declarar esta propiedad y establecer como destino o ejecutar en compilaciones anteriores de Windows, pero debe controlar la detección y conversión de páginas de códigos heredadas como de costumbre. Consulte [Uso de la página de códigos UTF-8 para](/windows/uwp/design/globalizing/use-utf8-code-page) obtener más información.

Este elemento no tiene atributos. **UTF-8 solo** es un valor válido para **el elemento activeCodePage.**

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>autoElevate

Especifica si la elevación automática está habilitada. **TRUE** indica que está habilitado. No tiene atributos.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Especifica si se deshabilita la entrega de un tema a los elementos de la interfaz de usuario. **TRUE** indica deshabilitado. No tiene atributos.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Especifica si se va a deshabilitar el filtrado de ventanas. **TRUE** deshabilita el filtrado de ventanas para que pueda enumerar las ventanas inmersivas desde el escritorio. **disableWindowFiltering** se agregó en Windows 8 y no tiene atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>dpiAware

Especifica si el proceso actual es compatible con puntos por pulgada (ppp).

**Windows 10, versión 1607:** El **elemento dpiAware** se omite si **el elemento dpiAwareness** está presente. Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607 que para una versión anterior del sistema operativo.

En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del **elemento dpiAware** y el texto que contiene. El texto del elemento no distingue mayúsculas de minúsculas.

| Estado del **elemento dpiAware** | Descripción     |
|-----------------------------------|---------|
| Absent                            | El proceso actual no es consciente de ppp de forma predeterminada. Puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)                                                                                                                                                            |
| Contiene "true"                   | El proceso actual es compatible con ppp del sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contiene "false"                  | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual no es consciente de los valores de ppp y no se puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |
| Contiene "true/pm"                | **Windows Vista, Windows 7 y Windows 8:** El proceso actual es compatible con ppp del sistema.<br/> **Windows 8.1 y Windows 10:** El proceso actual es compatible con ppp por monitor.<br/>                                                                                                                                                                                                          |
| Contiene "por monitor"            | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual es compatible con ppp por monitor.<br/>                                                                                                                                                                                      |
| Contiene cualquier otra cadena         | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual no es consciente de los valores de ppp y no se puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)<br/> |

Para obtener más información sobre la configuración de reconocimiento de ppp, vea [Comparación de los niveles de reconocimiento de PPP.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

**pppAware** no tiene atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>pppAwareness

Especifica si el proceso actual es compatible con puntos por pulgada (ppp).

La versión mínima del sistema operativo que admite el **elemento dpiAwareness** Windows 10, versión 1607. Para las versiones que admiten **el elemento dpiAwareness,** **pppAwareness** invalida el **elemento dpiAware.** Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607 que para una versión anterior del sistema operativo.

El **elemento dpiAwareness** puede contener un solo elemento o una lista de elementos separados por comas. En el último caso, se usa el primer elemento (situado más a la izquierda) de la lista reconocido por el sistema operativo. De esta manera, puede especificar distintos comportamientos admitidos en futuras versiones del sistema operativo Windows.

En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAwareness** y el texto que contiene en su elemento reconocido situado más a la izquierda. El texto del elemento no distingue mayúsculas de minúsculas.

| **estado del elemento dpiAwareness:**        | Descripción                          |
|-----------------------------------------|-------------------------------------------|
| El elemento está ausente                       | El **elemento dpiAware** especifica si el proceso tiene en cuenta los valores de ppp.                                                                                                                                                                   |
| No contiene elementos reconocidos            | El proceso actual no es consciente de ppp de forma predeterminada. Puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) |
| El primer elemento reconocido es "system"       | El proceso actual es compatible con ppp del sistema.                                                                                                                                                                                               |
| El primer elemento reconocido es "permonitor".   | El proceso actual es compatible con ppp por monitor.                                                                                                                                                                                          |
| El primer elemento reconocido es "permonitorv2" | El proceso actual usa el contexto de reconocimiento de ppp por monitor-v2. Este elemento solo se reconocerá en Windows 10 versión 1703 o posterior.                                                                                              |
| El primer elemento reconocido es "no consciente"      | El proceso actual no es consciente de los valores de ppp. No **se** puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)      |

Para obtener más información sobre la configuración de reconocimiento de ppp compatible con este elemento, vea [RECONOCIMIENTO \_ de PPP](/windows/desktop/api/windef/ne-windef-dpi_awareness) y [CONTEXTO DE RECONOCIMIENTO DE \_ \_ PPP](/windows/desktop/hidpi/dpi-awareness-context).

**pppAwareness** no tiene atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

Especifica si el escalado de GDI está habilitado. La versión mínima del sistema operativo que admite el **elemento gdiScaling** Windows 10 versión 1703.

El marco GDI (interfaz de dispositivo gráfico) puede aplicar el escalado de PPP a primitivos y texto por monitor sin actualizaciones en la propia aplicación. Esto puede ser útil para las aplicaciones GDI que ya no se actualizan activamente.

Este elemento no puede escalar gráficos no vectoriales (como mapas de bits, iconos o barras de herramientas). Además, los gráficos y el texto que aparecen dentro de los mapas de bits creados dinámicamente por las aplicaciones tampoco se pueden escalar mediante este elemento.

**TRUE** indica que este elemento está habilitado. No tiene atributos.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

Especifica si está habilitado el desplazamiento de alta resolución. **TRUE** indica que está habilitado. No tiene atributos.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Habilita rutas de acceso largas **que superan MAX_PATH** longitud. Este elemento se admite en Windows 10, versión 1607 y posteriores. Para obtener más información, consulte [este artículo](../fileio/maximum-file-path-limitation.md).

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

Especifica si el aislamiento del controlador de impresora está habilitado. **TRUE** indica que está habilitado. No tiene atributos. El aislamiento del controlador de impresora mejora la confiabilidad del servicio de impresión de Windows al permitir que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión. Compatibilidad con el aislamiento del controlador de impresora iniciado en Windows 7 y Windows Server 2008 R2. Una aplicación puede declarar el aislamiento del controlador de impresora en su manifiesto de aplicación para aislarse del controlador de impresora y mejorar su confiabilidad. Es decir, la aplicación no se bloqueará si el controlador de impresora tiene un error.


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

Especifica si está habilitado el desplazamiento de resolución ultra alta. **TRUE** indica que está habilitado. No tiene atributos.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Especifica la información de identidad de un [paquete MSIX disperso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para la aplicación actual. Este elemento se admite en Windows 10, versión 2004 y versiones posteriores.

El **elemento msix** debe estar en el espacio de nombres `urn:schemas-microsoft-com:msix.v1` . Tiene los atributos que se muestran en la tabla siguiente.

| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Describe la información del publicador. Este valor debe coincidir con el **atributo Publisher** del [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifiesto de paquete disperso. |
| **packageName** | Describe el contenido del paquete. Este valor debe coincidir con **el atributo Name** del elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifiesto de paquete disperso.    |
| **applicationId**    | Identificador único de la aplicación. Este valor debe coincidir con el **atributo Id** del [elemento Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) del manifiesto del paquete disperso.  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

Invalida la implementación predeterminada del montón para que las API de montón de [Win32](../Memory/heap-functions.md) las usen.

* El valor **SegmentHeap** indica que se usará el montón de segmentos. El montón de segmentos es una implementación moderna del montón que generalmente reducirá el uso general de memoria. Este elemento se admite en Windows 10, versión 2004 (compilación 19041) y versiones posteriores.
* Se omiten todos los demás valores.

Este elemento no tiene atributos.

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo de un manifiesto de aplicación para una aplicación denominada MySampleApp.exe. La aplicación consume el ensamblado SampleAssembly en paralelo.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
