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
ms.openlocfilehash: 31e1d42e4660e0e73830876cfdeb0a5c8a5957cd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471891"
---
# <a name="explorer-data-provider-sample"></a>Ejemplo del proveedor de datos de Explorer

Muestra cómo implementar una extensión de espacio de nombres de Shell, incluido el comportamiento del menú contextual y las tareas personalizadas en el explorador.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio **del proyecto ExplorerDataProvider.**
2.  Escriba `msbuild ExplorerDataProvider.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows Explorer y vaya al directorio del proyecto **ExplorerDataProvider.**
2.  Haga doble clic en el icono del archivo ExplorerDataProvider.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**. El archivo DLL se compilará en el directorio \\ debug o \\ release predeterminado.

> [!Note]  
> En la versión de este ejemplo incluida en el SDK de Windows, la configuración de la compilación de versión de 64 bits no incluye el archivo ExplorerDataProvider.def en la opción Archivo de definición de módulo del vinculador.  Debe especificar ese archivo usted mismo antes de compilarlo en un entorno de 64 bits. Agregue la línea a la sección VCLinkerTool (comienza en la línea `ModuleDefinitionFile="ExplorerDataProvider.def"` 329) del archivo ExplorerDataProvider.vcproj como se muestra aquí:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>LinkIncremental="1"&gt; AdditionalLibraryDirectories=""c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64""&gt; ModuleDefinitionFile="ExplorerDataProvider.def"&gt; GenerateDebugInformation="true"</code></pre> | 

>
> 
>
> La versión de este ejemplo descargable de la Galería de código se ha corregido para este problema y no se requiere ninguna acción adicional por su parte.
>
>  
>
> ## <a name="running-the-sample"></a>Ejecutar el ejemplo
>
> 1.  Vaya al directorio que contiene los nuevos archivos .dll y .propdesc, mediante el símbolo del sistema o Windows Explorer.
> 2.  En la línea de comandos, escriba `regsvr32.exe` .
>     > [!Note]  
>     > Si ejecuta este comando desde un símbolo del sistema con privilegios elevados, el registro automático también registrará automáticamente el archivo .propdesc. Si se ejecuta desde un símbolo del sistema sin privilegios elevados, la extensión de espacio de nombres funcionará, pero sin funcionalidad de propiedad personalizada.
>
>      
>
> 3.  Abra la carpeta **Mi PC** y examine la nueva extensión de espacio de nombres presente allí.
>
>  
>
>  
>


