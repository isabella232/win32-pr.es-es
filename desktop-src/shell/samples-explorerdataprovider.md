---
description: Muestra cómo implementar una extensión de espacio de nombres de Shell, incluido el comportamiento del menú contextual y las tareas personalizadas en el explorador.
title: Ejemplo del proveedor de datos de Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278868"
---
# <a name="explorer-data-provider-sample"></a>Ejemplo del proveedor de datos de Explorer

Muestra cómo implementar una extensión de espacio de nombres de Shell, incluido el comportamiento del menú contextual y las tareas personalizadas en el explorador.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ExplorerDataProvider** .
2.  Escriba `msbuild ExplorerDataProvider.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **ExplorerDataProvider** .
2.  Haga doble clic en el icono del archivo ExplorerDataProvider. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**. El archivo DLL se generará en el \\ Directorio de depuración o \\ versión predeterminado.

> [!Note]  
> En la versión de este ejemplo incluida en el Windows SDK, la configuración de la compilación de la versión de 64 bits no incluye el archivo ExplorerDataProvider. def en la opción de **archivo de definición de módulo** del enlazador. Debe especificar ese archivo antes de compilar en un entorno de 64 bits. Agregue la línea `ModuleDefinitionFile="ExplorerDataProvider.def"` a la sección VCLinkerTool (comienza en la línea 329) del archivo ExplorerDataProvider. vcproj como se muestra aquí:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> La versión de este ejemplo descargable de la galería de código se ha corregido para este problema y no se requiere ninguna acción adicional por su parte.
>
>  
>
> ## <a name="running-the-sample"></a>Ejecutar el ejemplo
>
> 1.  Navegue hasta el directorio que contiene el nuevo archivo. dll y. propDesc, mediante el símbolo del sistema o el explorador de Windows.
> 2.  En la línea de comandos, escriba `regsvr32.exe` .
>     > [!Note]  
>     > Si ejecuta este comando desde un símbolo del sistema con privilegios elevados, el registro automático también registrará automáticamente el archivo. propDesc. Si se ejecuta desde un símbolo del sistema sin privilegios elevados, la extensión de espacio de nombres funcionará, pero sin la funcionalidad de propiedad personalizada.
>
>      
>
> 3.  Abra la carpeta **mi PC** y examine la nueva extensión de espacio de nombres presente allí.
>
>  
>
>  
>


