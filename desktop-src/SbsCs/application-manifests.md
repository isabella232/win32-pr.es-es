---
description: Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifiestos de aplicación
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105653121"
---
# <a name="application-manifests"></a>Manifiestos de aplicación

Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución. Deben ser las mismas versiones de ensamblado utilizadas para probar la aplicación. Los manifiestos de aplicación también describen los metadatos para archivos privados de la aplicación.

Para obtener una lista completa del esquema XML, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).

Los manifiestos de aplicación tienen los siguientes elementos y atributos.

| Elemento                               | Atributos                | Obligatorio |
|---------------------------------------|---------------------------|----------|
| **assembl**                          |                           | Sí      |
|                                       | **manifestVersion**       | Sí      |
| **noInherit**                         |                           | No       |
| **assemblyIdentity**                  |                           | Sí      |
|                                       | **type**                  | Sí      |
|                                       | **name**                  | Sí      |
|                                       | **language**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Sí      |
|                                       | **publicKeyToken**        | No       |
| **compatibilidad**                     |                           | No       |
| **application**                       |                           | No       |
| **supportos**                       | **Id**                    | No       |
| **maxversiontested**                  | **Id**                    | No       |
| **pendiente**                        |                           | No       |
| **dependentAssembly**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **name**                  | No       |
|                                       | **hashalg**               | No       |
|                                       | **hash**                  | No       |
| **activeCodePage**                    |                           | No       |
| **Elevación de privilegios**                       |                           | No       |
| **disableTheming**                    |                           | No       |
| **disableWindowFiltering**            |                           | No       |
| **dpiAware**                          |                           | No       |
| **dpiAwareness**                      |                           | No       |
| **gdiScaling**                        |                           | No       |
| **highResolutionScrollingAware**      |                           | No       |
| **longPathAware**                     |                           | No       |
| **printerDriverIsolation**            |                           | No       |
| **ultraHighResolutionScrollingAware** |                           | No       |
| **msix**                              |                           | No       |
| **heapType**                          |                           | No       |

## <a name="file-location"></a>Ubicación del archivo

Los manifiestos de aplicación deben incluirse como un recurso en el archivo EXE o DLL de la aplicación.

Para obtener más información, vea [Instalar ensamblados en paralelo](installing-side-by-side-assemblies.md).

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de. manifest.

Por ejemplo, un manifiesto de aplicación que hace referencia a example.exe o example.dll utilizaría la siguiente sintaxis de nombre de archivo. Puede omitir el campo <ID. de *recurso*> si el identificador de recurso es 1.

**ID. de *recurso* deexample.exe. <>. manifest**

**ID. de *recurso* deexample.dll. <>. manifest**

## <a name="elements"></a>Elementos

Los nombres de los elementos y atributos distinguen mayúsculas de minúsculas. Los valores de los elementos y atributos no distinguen mayúsculas de minúsculas, excepto el valor del atributo type.

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>ensamblado

Elemento contenedor. Su primer subelemento debe ser un elemento **NoInherit** o **assemblyIdentity** . Obligatorio.

El elemento de **ensamblado** debe estar en el espacio de nombres "urn: schemas-microsoft-com: ASM. v1". Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o mediante el etiquetado.

El elemento **Assembly** tiene los atributos siguientes.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El atributo **manifestVersion** debe establecerse en 1,0. |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

Incluya este elemento en un manifiesto de aplicación para establecer los [contextos de activación](activation-contexts.md) generados a partir del manifiesto con la marca "no heredado". Cuando esta marca no se establece en un contexto de activación y el contexto de activación está activo, lo heredan los nuevos subprocesos en el mismo proceso, ventanas, procedimientos de ventana y [llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls). Al establecer esta marca, se evita que el nuevo objeto herede el contexto activo.

El elemento **NoInherit** es opcional y se suele omitir. La mayoría de los ensamblados no funcionan correctamente utilizando un contexto de activación no heredado porque el ensamblado debe diseñarse explícitamente para administrar la propagación de su propio contexto de activación. El uso del elemento **NoInherit** requiere que todos los ensamblados dependientes a los que hace referencia el manifiesto de aplicación tengan un elemento **NoInherit** en el [manifiesto del ensamblado](assembly-manifests.md).

Si se utiliza **NoInherit** en un manifiesto, debe ser el primer subelemento del elemento **Assembly** . El elemento **assemblyIdentity** debe aparecer inmediatamente después del elemento **NoInherit** . Si no se utiliza **NoInherit** , **assemblyIdentity** debe ser el primer subelemento del elemento **Assembly** . El elemento **NoInherit** no tiene elementos secundarios. No es un elemento válido en los [manifiestos de ensamblado](assembly-manifests.md).

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como primer subelemento de un elemento **Assembly** , **assemblyIdentity** describe e identifica de forma única la aplicación que posee este manifiesto de aplicación. Como primer subelemento de un elemento **dependentAssembly** , **assemblyIdentity** describe un ensamblado en paralelo requerido por la aplicación. Tenga en cuenta que cada ensamblado al que se hace referencia en el manifiesto de aplicación requiere **assemblyIdentity** que coincida exactamente con el **assemblyIdentity** en el manifiesto del ensamblado del ensamblado al que se hace referencia.

El elemento **assemblyIdentity** tiene los atributos siguientes. No tiene subelementos.

| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de aplicación o ensamblado. El valor debe ser Win32 y todo en minúsculas. Obligatorio.                                                                                                                                                                                                                                                                                                                              |
| **name**                  | Designa de forma exclusiva la aplicación o el ensamblado. Use el siguiente formato para el nombre: Organization.Division.Name. Por ejemplo, Microsoft. Windows. mysampleApp. Obligatorio.                                                                                                                                                                                                                                                               |
| **language**              | Identifica el idioma de la aplicación o del ensamblado. Opcional. Si la aplicación o el ensamblado son específicos del idioma, especifique el código de lenguaje DHTML. En el **assemblyIdentity** de una aplicación diseñada para uso internacional (idioma neutro), omita el atributo de idioma.<br/> En un **assemblyIdentity** de un ensamblado diseñado para uso internacional (idioma neutro) establezca el valor de Language en " \* ".<br/> |
| **processorArchitecture** | Especifica el procesador. Entre los valores válidos se incluyen `x86`, `amd64`, `arm` y `arm64`. Opcional.                                                                                                                                                                                                                                                                                                                       |
| **version**               | Especifica la versión de la aplicación o del ensamblado. Use el formato de versión de cuatro partes: mmmmm. nnnnn. ooooo. ppppp. Cada una de las partes separadas por puntos puede ser 0-65535, ambos inclusive. Para obtener más información, vea [versiones de ensamblado](assembly-versions.md). Obligatorio.                                                                                                                                                                        |
| **publicKeyToken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma la aplicación o el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Se requiere para todos los ensamblados en paralelo compartidos.                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>compatibilidad

Contiene al menos una **aplicación**. No tiene atributos. Opcional. Los manifiestos de aplicación sin un elemento de compatibilidad tienen como valor predeterminado la compatibilidad con Windows Vista en Windows 7.

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>application

Contiene al menos un elemento **admitido** . A partir de Windows 10, versión 1903, también puede contener un elemento **maxversiontested** opcional. No tiene atributos. Opcional.

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportos

El elemento **supportos** tiene el siguiente atributo. No tiene subelementos.

| Atributo | Descripción   |
|-----------|-----------------------|
| **Id**    | Establezca el atributo ID en **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para ejecutar la aplicación mediante la funcionalidad de vista. Esto puede permitir que una aplicación diseñada para Windows Vista se ejecute en un sistema operativo posterior. <br/> Establezca el atributo ID en **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para ejecutar la aplicación mediante la funcionalidad de Windows 7.<br/> Las aplicaciones que admiten la funcionalidad de Windows Vista, Windows 7 y Windows 8 no requieren manifiestos independientes. En este caso, agregue los GUID para todos los sistemas operativos Windows.<br/> Para obtener información sobre el comportamiento del atributo **ID** en Windows, vea la guía de compatibilidad de Windows [8 y Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).<br/> Los siguientes GUID corresponden a los sistemas operativos indicados:<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, windows Server 2016 y windows Server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 y Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 y windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 y windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista y windows Server 2008<br/> Para probarlo en Windows 7 o Windows 8. x, ejecute Monitor de recursos (resmon), vaya a la pestaña CPU, haga clic con el botón derecho en las etiquetas de columna, "Seleccionar columna..." y seleccione "contexto del sistema operativo". En Windows 8. x, también puede encontrar esta columna disponible en el administrador de tareas (taskmgr). El contenido de la columna muestra el valor más alto encontrado o "Windows Vista" como valor predeterminado. <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

El elemento **maxversiontested** especifica la versión máxima de Windows con la que se probó la aplicación. Esto está pensado para que lo usen las aplicaciones de escritorio que usan [islas XAML](/windows/apps/desktop/modernize/xaml-islands) y que no se implementan en un paquete MSIX. Este elemento es compatible con Windows 10, la versión 1903 y versiones posteriores.

El elemento **maxversiontested** tiene el siguiente atributo. No tiene subelementos.

| Atributo | Descripción    |
|-----------|----------------|
| **Id**    | Establezca el atributo ID en una cadena de versión de cuatro partes que especifique la versión máxima de Windows con la que se probó la aplicación. Por ejemplo, "10.0.18226.0". |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency

Contiene al menos un **dependentAssembly**. No tiene atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

El primer subelemento de **dependentAssembly** debe ser un elemento **assemblyIdentity** que describe un ensamblado en paralelo requerido por la aplicación. Cada **dependentAssembly** debe estar dentro de una **dependencia** exactamente. No tiene atributos.

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>archivo

Especifica los archivos que son privados para la aplicación. Opcional.

El elemento **File** tiene los atributos que se muestran en la tabla siguiente.



| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nombre del archivo. Por ejemplo, Comctl32.dll.                                                            |
| **hashalg** | Algoritmo usado para crear un hash del archivo. Este valor debe ser SHA1.                                 |
| **hash**    | Un hash del archivo al que se hace referencia por nombre. Cadena hexadecimal de longitud según el algoritmo hash. |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

Fuerce que un proceso use UTF-8 como página de códigos del proceso.

**activeCodePage** se agregó en la versión 1903 de Windows (actualización 2019 de mayo). Puede declarar esta propiedad y destino o ejecutar en compilaciones anteriores de Windows, pero debe administrar la detección y conversión de páginas de códigos heredadas como de costumbre. Consulte [usar la página de códigos UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obtener más información.

Este elemento no tiene atributos. **UTF-8** es solo un valor válido para el elemento **activeCodePage** .

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

### <a name="autoelevate"></a>Elevación de privilegios

Especifica si la elevación automática está habilitada. **True** indica que está habilitada. No tiene atributos.

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

Especifica si los elementos de la interfaz de usuario que proporcionan un tema están deshabilitados. **True** indica deshabilitado. No tiene atributos.

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

Especifica si se va a deshabilitar el filtrado de ventanas. **True** deshabilita el filtrado de ventanas para que pueda enumerar las ventanas envolventes del escritorio. **disableWindowFiltering** se agregó en Windows 8 y no tiene atributos.

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

Especifica si el proceso actual tiene reconocimiento de puntos por pulgada (PPP).

**Windows 10, versión 1607:** El elemento **dpiAware** se omite si el elemento **dpiAwareness** está presente. Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607, que para una versión anterior del sistema operativo.

En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAware** y del texto que contiene. El texto dentro del elemento no distingue entre mayúsculas y minúsculas.

| Estado del elemento **dpiAware** | Descripción     |
|-----------------------------------|---------|
| Absent                            | El proceso actual no es compatible con PPP de forma predeterminada. Puede cambiar este valor mediante programación llamando a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .                                                                                                                                                            |
| Contiene "true"                   | El proceso actual es compatible con PPP del sistema.                                                                                                                                                                                                                                                                                                                                                          |
| Contiene "false"                  | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual no tiene en cuenta el valor de PPP y no se puede cambiar mediante programación con la llamada a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |
| Contiene "true/PM"                | **Windows Vista, Windows 7 y Windows 8:** El proceso actual es compatible con PPP del sistema.<br/> **Windows 8.1 y Windows 10:** El proceso actual es compatible con PPP por monitor.<br/>                                                                                                                                                                                                          |
| Contiene "por monitor"            | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual es compatible con PPP por monitor.<br/>                                                                                                                                                                                      |
| Contiene cualquier otra cadena         | **Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.<br/> **Windows 8.1 y Windows 10:** El proceso actual no tiene en cuenta el valor de PPP y no se puede cambiar mediante programación con la llamada a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .<br/> |

Para obtener más información sobre la configuración de reconocimiento de PPP, consulte [comparación de los niveles de reconocimiento de PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

**dpiAware** no tiene atributos.

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

### <a name="dpiawareness"></a>dpiAwareness

Especifica si el proceso actual tiene reconocimiento de puntos por pulgada (PPP).

La versión mínima del sistema operativo que admite el elemento **dpiAwareness** es Windows 10, versión 1607. En el caso de las versiones que admiten el elemento **dpiAwareness** , el **dpiAwareness** invalida el elemento **dpiAware** . Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607, que para una versión anterior del sistema operativo.

El elemento **dpiAwareness** puede contener un único elemento o una lista de elementos separados por comas. En el último caso, se usa el primer elemento (situado más a la izquierda) de la lista reconocido por el sistema operativo. De esta forma, puede especificar diferentes comportamientos que se admiten en versiones futuras del sistema operativo Windows.

En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAwareness** y el texto que contiene en el elemento reconocido más a la izquierda. El texto dentro del elemento no distingue entre mayúsculas y minúsculas.

| Estado del elemento **dpiAwareness** :        | Descripción                          |
|-----------------------------------------|-------------------------------------------|
| Falta el elemento                       | El elemento **dpiAware** especifica si el proceso es compatible con PPP.                                                                                                                                                                   |
| No contiene elementos reconocidos            | El proceso actual no es compatible con PPP de forma predeterminada. Puede cambiar este valor mediante programación llamando a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) . |
| El primer elemento reconocido es "System"       | El proceso actual es compatible con PPP del sistema.                                                                                                                                                                                               |
| El primer elemento reconocido es "permonitor"   | El proceso actual es compatible con PPP por monitor.                                                                                                                                                                                          |
| El primer elemento reconocido es "permonitorv2" | El proceso actual utiliza el contexto de reconocimiento de PPP por monitor-V2. Este elemento solo se reconocerá en la versión 1703 o posterior de Windows 10.                                                                                              |
| El primer elemento reconocido es "no compatible"      | El proceso actual no es compatible con PPP. **No se puede** cambiar este valor mediante programación si se llama a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .      |

Para obtener más información sobre la configuración de reconocimiento de PPP compatible con este elemento, consulte [ \_ reconocimiento de PPP](/windows/desktop/api/windef/ne-windef-dpi_awareness) y [contexto de \_ reconocimiento \_ de PPP](/windows/desktop/hidpi/dpi-awareness-context).

**dpiAwareness** no tiene atributos.

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

Especifica si está habilitado el escalado de GDI. La versión mínima del sistema operativo que admite el elemento **gdiScaling** es Windows 10, versión 1703.

El marco de trabajo GDI (interfaz de dispositivo gráfico) puede aplicar el ajuste de escala de PPP a primitivos y texto por monitor sin actualizaciones a la propia aplicación. Esto puede ser útil para las aplicaciones GDI que ya no se actualizan de forma activa.

Este elemento no puede escalar los gráficos no vectoriales (por ejemplo, mapas de bits, iconos o barras de herramientas). Además, este elemento no puede escalar los gráficos y el texto que aparecen en los mapas de bits construidos dinámicamente por las aplicaciones.

**True** indica que este elemento está habilitado. No tiene atributos.


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

Especifica si está habilitado el reconocimiento de alta resolución. **True** indica que está habilitada. No tiene atributos.

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

Habilita rutas de acceso largas que superan **MAX_PATH** de longitud. Este elemento es compatible con Windows 10, versión 1607 y versiones posteriores. Para obtener más información, consulte [este artículo](../fileio/maximum-file-path-limitation.md).

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

Especifica si está habilitado el aislamiento de controladores de impresora. **True** indica que está habilitada. No tiene atributos. El aislamiento de controladores de impresora mejora la confiabilidad del servicio de impresión de Windows al permitir que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión. Se ha iniciado la compatibilidad con el aislamiento de controladores de impresora en Windows 7 y Windows Server 2008 R2. Una aplicación puede declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislarse del controlador de la impresora y mejorar su confiabilidad. Es decir, la aplicación no se bloqueará si el controlador de impresora tiene un error.


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

Especifica si está habilitado el reconocimiento de la resolución ultra alta. **True** indica que está habilitada. No tiene atributos.

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

Especifica la información de identidad de un [paquete MSIX disperso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para la aplicación actual. Este elemento es compatible con Windows 10, la versión 2004 y versiones posteriores.

El elemento **msix** debe estar en el espacio de nombres `urn:schemas-microsoft-com:msix.v1` . Tiene los atributos que se muestran en la tabla siguiente.

| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | Describe la información del publicador. Este valor debe coincidir con el atributo **Publisher** en el elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) en el manifiesto del paquete disperso. |
| **packageName** | Describe el contenido del paquete. Este valor debe coincidir con el atributo **Name** del elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) en el manifiesto del paquete disperso.    |
| **applicationId**    | Identificador único de la aplicación. Este valor debe coincidir con el atributo **ID** del elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) en el manifiesto del paquete disperso.  |

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

Invalida la implementación de montón predeterminada para las [API del montón de Win32](../Memory/heap-functions.md) que se va a usar.

* El valor **SegmentHeap** indica que se usará el montón del segmento. El montón de segmentos es una implementación de montón moderna que normalmente reducirá el uso de memoria total. Este elemento es compatible con Windows 10, versión 2004 (compilación 19041) y versiones posteriores.
* Todos los demás valores se omiten.

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

El siguiente es un ejemplo de un manifiesto de aplicación para una aplicación denominada MySampleApp.exe. La aplicación consume el ensamblado en paralelo SampleAssembly.

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
