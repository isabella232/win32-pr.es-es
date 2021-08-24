---
description: En este tutorial se muestra cómo tomar una aplicación monolingüe y prepararla para todo el mundo. Esta aplicación tiene la forma de una solución completa que se basa en Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Agregar Interfaz de usuario multilingüe compatibilidad con aplicaciones a una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147698"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Agregar Interfaz de usuario multilingüe compatibilidad con aplicaciones a una aplicación

En este tutorial se muestra cómo tomar una aplicación monolingüe y prepararla para todo el mundo. Esta aplicación tiene la forma de una solución completa que se basa en Microsoft Visual Studio.

-   [Información general](#splitting-the-various-language-resource-modules-an-overview)
    -   [La idea detrás de Hello MUI](#the-idea-behind-hello-mui)
-   [Configuración de la solución Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Requisitos de la plataforma](#platform-requirements)
    -   [Requisitos previos](#prerequisites)
-   [Paso 0: Creación de Hello MUI codificado de forma hard-code](#step-0-creating-the-hard-coded-hello-mui)
-   [Paso 1: Implementar el módulo de recursos básicos](#step-1-implementing-the-basic-resource-module)
-   [Paso 2: Compilar el módulo de recursos básicos](#step-2-building-the-basic-resource-module)
    -   [Dividir los distintos módulos de recursos de lenguaje: Información general](#splitting-the-various-language-resource-modules-an-overview)
    -   [Dividir los distintos módulos de recursos de lenguaje: crear los archivos](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Paso 3: Crear un Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Paso 4: Globalizar "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Paso 5: Personalizar "Hello MUI"](#step-5-customizing-hello-mui)
-   [Consideraciones adicionales para MUI](#additional-considerations-for-mui)
    -   [Compatibilidad con aplicaciones de consola](#support-for-console-applications)
    -   [Determinación de los idiomas que se admitirán en tiempo de ejecución](#determination-of-languages-to-support-at-run-time)
    -   [Compatibilidad con scripts complejos en versiones anteriores a Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Resumen](#summary)

## <a name="overview"></a>Información general

A partir de Windows Vista, el propio sistema operativo Windows se creó desde el principio para ser una plataforma multilingüe, con compatibilidad adicional que le permite crear aplicaciones multilingües que usan el modelo de recursos Windows MUI.

En este tutorial se ilustra esta nueva compatibilidad con las aplicaciones multilingües mediante la cobertura de los siguientes aspectos:

-   Usa la compatibilidad mejorada con la plataforma DEME PARA habilitar fácilmente las aplicaciones multilingües.
-   Extiende las aplicaciones multilingües para que se ejecuten en versiones de Windows antes de Windows Vista.
-   Tiene en cuenta las consideraciones adicionales implicadas en el desarrollo de aplicaciones multilingües especializadas, como las aplicaciones de consola.

Estos vínculos ayudan a proporcionar un actualizador rápido sobre los conceptos de internacionalización e MUI:

-   [Introducción rápida a la internacionalización.](understanding-internationalization.md)
-   [Conceptos de MUI](understanding-mui.md).
-   [Uso de MUI para desarrollar aplicaciones Win32.](using-multilingual-user-interface.md)

### <a name="the-idea-behind-hello-mui"></a>La idea detrás de Hello MUI

Probablemente esté familiarizado con la aplicación de Hola mundo clásica, que ilustra los conceptos básicos de programación. Este tutorial adopta un enfoque similar para ilustrar cómo usar el modelo de recursos de MUI para actualizar una aplicación monolingüe con el fin de crear una versión multilingüe denominada Hello MUI.

> [!Note]  
> Las tareas de este tutorial se describen en pasos detallados debido a la precisión con la que se deben realizar estas actividades y a la necesidad de explicar los detalles a los desarrolladores que tienen poca experiencia con estas tareas.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configuración de la solución Hello MUI

En estos pasos se describe cómo prepararse para crear la solución Hello MUI.

### <a name="platform-requirements"></a>Requisitos de la plataforma

Debe compilar los ejemplos de código de este tutorial mediante el Kit de desarrollo de software (SDK) de Windows para Windows 7 y Visual Studio 2008. El SDK de Windows 7 se instalará en Windows XP, Windows Vista y Windows 7, y la solución de ejemplo se puede crear en cualquiera de estas versiones del sistema operativo.

Todos los ejemplos de código de este tutorial están diseñados para ejecutarse en versiones x86 y x64 de Windows XP, Windows Vista y Windows 7. Las partes específicas que no funcionarán en Windows XP se llaman cuando corresponda.

### <a name="prerequisites"></a>Requisitos previos

1.  Instale Visual Studio 2008.

    Para obtener más información, vea el [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).

2.  Instale el SDK Windows para Windows 7.

    Puede instalarlo desde la página Windows SDK del Centro [Windows desarrolladores](https://msdn.microsoft.com/windowsserver/bb980924.aspx)de . El SDK incluye utilidades para desarrollar aplicaciones para versiones del sistema operativo desde Windows XP hasta la más reciente.

    > [!Note]  
    > Si no va a instalar el paquete en la ubicación predeterminada, o si no va a instalar en la unidad del sistema, que suele ser la unidad C, tome nota de la ruta de instalación.

     

3.  Configure los parámetros Visual Studio línea de comandos.

    1.  Abra una ventana Visual Studio comandos.
    2.  Escriba la **ruta de acceso del conjunto.**
    3.  Confirme que la variable path incluye la ruta de acceso de la carpeta bin del SDK Windows 7: ... Sdk de Microsoft \\ Windows \\ bin v7.0 \\

4.  Instale el paquete de complementos de las API de nivel inferior de NLS de Microsoft.
    > [!Note]  
    > En el contexto de este tutorial, este paquete solo es necesario si va a personalizar la aplicación para que se ejecute en Windows versiones anteriores a Windows Vista. Vea [Paso 5: Personalización de Hello MUI.](#step-5-customizing-hello-mui)

     

    1.  Descargue e instale el paquete desde su [sitio de descarga.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)
    2.  Al igual que con el SDK de Windows, si no va a instalar el paquete en la ubicación predeterminada, o si no va a instalar en la unidad del sistema, que normalmente es la unidad C, tome nota de la ruta de instalación.
    3.  Si la plataforma de desarrollo Windows XP o Windows Server 2003, confirme que Nlsdl.dll está instalado y registrado correctamente.

        1.  Vaya a la carpeta "redist" en la ubicación de la ruta de acceso de instalación.
        2.  Ejecute el nlsdl redistribuible adecuado. \*.exe, como nlsdl.x86.exe. Este paso instala y registra Nlsdl.dll.

    > [!Note]  
    > Si desarrolla una aplicación que usa MUI y que debe ejecutarse en versiones de Windows anteriores a Windows Vista, Nlsdl.dll debe estar presente en la plataforma de Windows destino. En la mayoría de los casos, esto significa que la aplicación debe llevar e instalar el instalador nlsdl redistribuible (y no simplemente copiar Nlsdl.dll sí mismo).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Paso 0: Creación de Hello MUI codificado de forma hard-code

Este tutorial comienza con la versión monolingüe de la aplicación Hello MUI. La aplicación asume el uso del lenguaje de programación C++, las cadenas de caracteres anchos y la función [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) para la salida.

Comience por crear la aplicación Inicial GuiStep 0, así como la solución HelloMUI, que contiene todas las \_ aplicaciones de este tutorial.

1.  En Visual Studio 2008, cree un proyecto. Use los valores y la configuración siguientes:

    1.  Project tipo: en Visual C++ seleccione Win32 y, en Visual Studio plantillas instaladas, seleccione Win32 Project.
    2.  Nombre: GuiStep \_ 0.
    3.  Ubicación: *ProjectRootDirectory* (los pasos posteriores hacen referencia a este directorio).
    4.  Nombre de la solución: HelloMUI.
    5.  Seleccione Crear directorio para la solución.
    6.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: Windows aplicación.

2.  Configure el modelo de subprocesos de proyecto:

    1.  En la Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 0 y, a continuación, seleccione Propiedades.
    2.  En el cuadro de diálogo Páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca Configuración en Todas las configuraciones.
        2.  En Propiedades de configuración expanda C/C++, seleccione Generación de código y establezca Biblioteca en tiempo de ejecución: Depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 0.cpp por el código siguiente:
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Compile y ejecute la aplicación.

El código fuente sencillo anterior hace que la elección de diseño simplista de codificar de forma rígida, o incrustar, toda la salida que el usuario verá, en este caso el texto "Hello MUI". Esta opción limita la utilidad de la aplicación para los usuarios que no reconocen la palabra en inglés "Hello". Dado que MUI es un acrónimo en inglés basado en tecnología, se supone en este tutorial que la cadena sigue siendo "MUI" para todos los idiomas.

## <a name="step-1-implementing-the-basic-resource-module"></a>Paso 1: Implementar el módulo de recursos básicos

Microsoft Win32 ha expuesto durante mucho tiempo la capacidad para que los desarrolladores de aplicaciones separe sus datos de recursos de interfaz de usuario del código fuente de la aplicación. Esta separación tiene el formato del modelo de recursos Win32, en el que las cadenas, mapas de bits, iconos, mensajes y otros elementos que normalmente se muestran a un usuario se empaquetan en una sección distinta del ejecutable, separadas del código ejecutable.

Para ilustrar esta separación entre el código ejecutable y el empaquetado de datos de recursos, en este paso el tutorial coloca la cadena "Hello" codificada previamente (el recurso "en-US") en la sección de recursos de un módulo DLL del proyecto HelloModule \_ en \_ us.

Este archivo DLL de Win32 también podría contener funcionalidad ejecutable de tipo biblioteca (como cualquier otro archivo DLL). Pero para ayudar a centrarse en los aspectos relacionados con los recursos de Win32, se deja el código DLL en tiempo de ejecución como código auxiliar en dllmain.cpp. Las secciones posteriores de este tutorial usan los datos de recursos HelloModule que se están construyendo aquí y también presentan el código en tiempo de ejecución adecuado.

Para construir un módulo de recursos win32, empiece por crear un archivo DLL con un archivo dllmain con código auxiliar:

1.  Agregue un nuevo proyecto a la solución HelloMUI:

    1.  En el menú Archivo, seleccione Agregar y, a continuación, Nuevo Project.
    2.  Project tipo: Win32 Project.
    3.  Nombre: HelloModule \_ en \_ nosotros.
    4.  Ubicación: *ProjectRootDirectory* \\ HelloMUI.
    5.  En el Asistente para aplicaciones Win32, seleccione Tipo de aplicación: DLL.

2.  Configure el modelo de subprocesos de este proyecto:

    1.  En la Explorador de soluciones, haga clic con el botón derecho en el proyecto HelloModule \_ en us y seleccione \_ Propiedades.
    2.  En el cuadro de diálogo Páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca Configuración en Todas las configuraciones.
        2.  En Propiedades de configuración expanda C/C++, seleccione Generación de código y establezca Biblioteca en tiempo de ejecución: Depuración multiproceso (/MTd).

3.  Examine dllmain.cpp. (Es posible que desee agregar UNREFERENCED \_ Macros PARAMETER en el código generado, como se ha hecho aquí, para permitir que se compile en el nivel de advertencia 4).
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Agregue un archivo de definición de recursos HelloModule.rc al proyecto:

    1.  En el proyecto HelloModule en nosotros, haga clic con el botón derecho en la carpeta Archivos de recursos, seleccione Agregar y, a \_ continuación, seleccione Nuevo \_ elemento.
    2.  En el cuadro de diálogo Agregar nuevo elemento, elija lo siguiente:

        1.  Categorías: en Visual C++ seleccione Recurso y, a continuación, en "Visual Studio instaladas", seleccione Archivo de recursos (.rc).
        2.  Nombre: HelloModule.
        3.  Ubicación: acepte el valor predeterminado.
        4.  Haga clic en Agregar.

    3.  Especifique que el nuevo archivo HelloModule.rc se guardará como Unicode:

        1.  En la Explorador de soluciones, haga clic con el botón derecho en HelloModule.rc y seleccione Ver código.
        2.  Si ve un mensaje que le indica que el archivo ya está abierto y le pregunta si desea cerrarlo, haga clic en Sí.
        3.  Con el archivo mostrado como texto, haga que el menú seleccione Archivo y, a continuación, Opciones avanzadas de guardado.
        4.  En Codificación, especifique Unicode: página de códigos 1200.
        5.  Haga clic en Aceptar.
        6.  Guarde y cierre HelloModule.rc.

    4.  Agregue una tabla de cadenas que contenga la cadena "Hello":

        1.  En la Vista de recursos, haga clic con el botón derecho en HelloModule.rc y seleccione Agregar recurso.
        2.  Seleccione Tabla de cadenas.
        3.  Haga clic en Nuevo.
        4.  Agregue una cadena a la tabla de cadenas:

            1.  IDENTIFICADOR: HELLO \_ MUI \_ STR \_ 0.
            2.  Valor: 0.
            3.  Título: Hola.

        Si ahora ve HelloModule.rc como texto, verá varios fragmentos de código fuente específico del recurso. La de mayor interés es la sección que describe la cadena "Hello":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Esta cadena "Hello" es el recurso que se debe localizar (es decir, traducir) a todos los idiomas que la aplicación espera admitir. Por ejemplo, el archivo Ta de HelloModule en el proyecto (que creará en el paso siguiente) contendrá su propia versión localizada de \_ \_ HelloModule.rc para "ta-IN":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Compile el proyecto HelloModule \_ en us para asegurarse de que no hay \_ errores.

5.  Cree seis proyectos más en la solución HelloMUI (o tantos como desee) para crear seis archivos DLL de recursos más para lenguajes adicionales. Use los valores de esta tabla:

    | Nombre de proyecto        | Nombre del archivo .rc | Identificador de cadena          | Valor de cadena | Título de cadena |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ de | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Hola          |
    | HelloModule \_ es \_ | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Bonjour        |
    | HelloModule \_ hi \_ in | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | नमस्           |
    | HelloModule \_ ru \_ ru | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ in | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | வணக்கம்        |

    

     

Para obtener más información sobre la sintaxis y la estructura de archivos .rc, vea [Acerca de los archivos de recursos.](../menurc/about-resource-files.md)

## <a name="step-2-building-the-basic-resource-module"></a>Paso 2: Compilar el módulo de recursos básicos

Con los modelos de recursos anteriores, la creación de cualquiera de los siete proyectos HelloModule daría como resultado siete archivos DLL independientes. Cada archivo DLL contendrá una sección de recursos con una sola cadena localizada en el idioma adecuado. Aunque es adecuado para el modelo de recursos de Win32 histórico, este diseño no aprovecha las ventajas de MUI.

En el SDK Windows Vista y versiones posteriores, MUI proporciona la capacidad de dividir los ejecutables en código fuente y módulos de contenido localizables. Con la personalización adicional que se trata más adelante en el paso 5, las aplicaciones se pueden habilitar para que la compatibilidad con varios idiomas se ejecute en versiones anteriores a Windows Vista.

Los mecanismos principales disponibles para dividir los recursos del código ejecutable, empezando por Windows Vista, son:

-   Usar rc.exe (el compilador RC) con modificadores específicos o
-   Usar una herramienta de división de estilo posterior a la compilación denominada muirct.exe.

Consulte [Utilidades de recursos](resource-utilities.md) para obtener más información.

Por motivos de simplicidad, en este tutorial se muirct.exe para dividir el ejecutable "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Dividir los distintos módulos de recursos de lenguaje: Información general

Un proceso de varias partes está implicado en la división de los archivos DLL en un HelloModule.dll ejecutable, más un archivo HelloModule.dll.dl para cada uno de los siete idiomas admitidos en este tutorial. En esta introducción se describen los pasos necesarios. En la sección siguiente se presenta un archivo de comandos que realiza esos pasos.

En primer lugar, divida el módulo de HelloModule.dll inglés mediante el comando :


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



La línea de comandos anterior usa el archivo de configuración DoReverseMuiLoc.rcconfig. Este tipo de archivo de configuración lo usan normalmente los muirct.exe para dividir los recursos entre el archivo DLL de lenguaje neutro (LN) y los archivos .mui dependientes del idioma. En este caso, el archivo xml DoReverseMuiLoc.rcconfig (que se muestra en la sección siguiente) indica muchos tipos de recursos, pero todos ellos se encuentran en la categoría de archivos "localizedResources" o .mui, y no hay recursos en la categoría de idioma neutro. Para obtener más información sobre cómo preparar un archivo de configuración de recursos, vea [Preparar un archivo de configuración de recursos.](preparing-a-resource-configuration-file.md)

Además de crear un archivo HelloModule.dll.mui que contiene la cadena en inglés "Hello", muirct.exe también inserta un recurso de MUI en el módulo HelloModule.dll durante la división. Para cargar correctamente en tiempo de ejecución los recursos adecuados de los módulos HelloModule.dll.mui específicos del idioma, cada archivo .csv debe tener sus sumas de comprobación fijas para que coincidan con las sumas de comprobación del módulo LN neutro del lenguaje de línea de base. Esto se realiza mediante un comando como:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



De forma similar, muirct.exe se invoca para crear un archivo HelloModule.dll.csv para cada uno de los otros idiomas. Sin embargo, en esos casos se descarta el archivo DLL neutro del lenguaje, ya que solo será necesario el primero creado. Los comandos que procesan los recursos español y francés tienen el siguiente aspecto:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Una de las cosas más importantes que hay que tener en cuenta en muirct.exe líneas de comandos anteriores es que la marca -x se usa para especificar un identificador de idioma de destino. El valor proporcionado a muirct.exe es diferente para cada módulo de HelloModule.dll idioma específico. Este valor de lenguaje es central y lo usa muirct.exe para marcar correctamente el archivo .mui durante la división. Un valor incorrecto genera errores de carga de recursos para ese archivo .csv concreto en tiempo de ejecución. Consulte [Language Identifier Constants and Strings (Constantes](language-identifier-constants-and-strings.md) y cadenas de identificador de lenguaje) para obtener más información sobre cómo asignar el nombre de idioma a LCID.

Cada archivo .csv dividido termina en un directorio correspondiente a su nombre de idioma, inmediatamente debajo del directorio en el que residirá el HelloModule.dll independiente del idioma. Para obtener más información sobre la colocación de archivos .csv, vea [Implementación de aplicaciones.](application-deployment.md)

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Dividir los distintos módulos de recursos de lenguaje: crear los archivos

Para este tutorial, creará un archivo de comandos que contiene los comandos para dividir los distintos archivos DLL y lo invocará manualmente. Tenga en cuenta que, en el trabajo de desarrollo real, podría reducir la posibilidad de errores de compilación incluyendo estos comandos como eventos anteriores o posteriores a la compilación en la solución HelloMUI, pero eso está fuera del ámbito de este tutorial.

Cree los archivos para la compilación de depuración:

1.  Cree un archivo de comandos DoReverseMuiLoc.cmd que contenga los siguientes comandos:
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Cree un archivo xml DoReverseMuiLoc.rcconfig que contenga las líneas siguientes:
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Copie DoReverseMuiLoc.cmd y DoReverseMuiLoc.rcconfig en *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  Abra el Visual Studio de comandos de 2008 y vaya al directorio Depurar.
5.  Ejecute DoReverseMuiLoc.cmd.

Al crear una compilación de versión, copie los mismos archivos DoReverseMuiLoc.cmd y DoReverseMuiLoc.rcconfig en el directorio Release y ejecute allí el archivo de comandos.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Paso 3: Crear un Resource-Savvy "Hello MUI"

A partir del ejemplo inicial de GuiStep0.exe codificado de forma manual anterior, podría ampliar el alcance de la aplicación a varios usuarios del lenguaje si elige incorporar el modelo de recursos \_ win32. El nuevo código en tiempo de ejecución que se presenta en este paso incluye la lógica de carga del módulo [**(LoadLibraryEx)**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)y recuperación de cadenas [**(LoadString).**](/windows/win32/api/winuser/nf-winuser-loadstringa)

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante la selección de menú Archivo, Agregar y Nuevo Project) con los valores y valores siguientes:

    1.  Project tipo: Win32 Project.
    2.  Nombre: GuiStep \_ 1.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: Windows aplicación.

2.  Establezca este proyecto para que se ejecute desde dentro Visual Studio y configure su modelo de subprocesos:

    1.  En la Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep 1 y seleccione Establecer como inicio \_ Project.
    2.  Vuelva a hacer clic con el botón derecho en él y seleccione Propiedades.
    3.  En el cuadro de diálogo Páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca Configuración en Todas las configuraciones.
        2.  En Propiedades de configuración, expanda C/C++, seleccione Generación de código y establezca Biblioteca en tiempo de ejecución: Depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 1.cpp por el código siguiente:
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Compile y ejecute la aplicación. La salida se mostrará en el idioma establecido actualmente como idioma para mostrar del equipo (siempre que sea uno de los siete idiomas que hemos creado).

## <a name="step-4-globalizing-hello-mui"></a>Paso 4: Globalización de "Hello MUI"

Aunque el ejemplo anterior es capaz de mostrar su salida en distintos idiomas, se queda corto en una serie de áreas. Quizás lo más evidente es que la aplicación solo está disponible en un pequeño subconjunto de idiomas en comparación con el sistema operativo Windows sistema operativo. Si, por ejemplo, la aplicación GuiStep 1 del paso anterior se instalara en una compilación japonesa de Windows, los errores de ubicación de recursos \_ serían probables.

Para solucionar esta situación, tiene dos opciones principales:

-   Asegúrese de que se incluyen los recursos en un lenguaje de reserva final predeterminado.
-   Proporcione una manera de que el usuario final configure sus preferencias de idioma entre el subconjunto de idiomas admitidos específicamente por la aplicación.

De estas opciones, la que proporciona un lenguaje de reserva final es muy recomendable y se implementa en este tutorial pasando la marca -g a muirct.exe, como se ha visto anteriormente. Esta marca indica a muirct.exe que un idioma específico (de-DE/0x0407) sea el idioma de reserva final asociado al módulo dll neutral del idioma (HelloModule.dll). En tiempo de ejecución, este parámetro se usa como último recurso para generar texto que se mostrará al usuario. En caso de que no se encuentra un idioma de reserva final y no hay ningún recurso adecuado disponible en el binario neutral del idioma, se produce un error al cargar el recurso. Por lo tanto, debe determinar cuidadosamente los escenarios que la aplicación podría encontrar y planear el lenguaje de reserva final en consecuencia.

La otra opción de permitir preferencias de lenguaje configurables y cargar recursos basados en esta jerarquía definida por el usuario puede aumentar considerablemente la satisfacción del cliente. Desafortunadamente, también complica la funcionalidad necesaria dentro de la aplicación.

En este paso del tutorial se usa un mecanismo de archivo de texto simplificado para habilitar la configuración personalizada del lenguaje de usuario. La aplicación analiza el archivo de texto en tiempo de ejecución y la lista de idiomas analizada y validada se usa para establecer una lista de reserva personalizada. Una vez establecida la lista de reserva personalizada, las API de Windows cargarán los recursos según la prioridad de idioma establecida en esta lista. El resto del código es similar al que se encontró en el paso anterior.

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante la selección de menú Archivo, Agregar y Nuevo Project) con los valores y valores siguientes:

    1.  Project tipo: Win32 Project.
    2.  Nombre: GuiStep \_ 2.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: Windows aplicación.

2.  Establezca este proyecto para que se ejecute desde dentro Visual Studio y configure su modelo de subprocesos:

    1.  En la Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep 2 y seleccione Establecer como inicio \_ Project.
    2.  Vuelva a hacer clic con el botón derecho en él y seleccione Propiedades.
    3.  En el cuadro de diálogo Páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca Configuración en Todas las configuraciones.
        2.  En Propiedades de configuración, expanda C/C++, seleccione Generación de código y establezca Biblioteca en tiempo de ejecución: Depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 2.cpp por el código siguiente:
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Cree un archivo de texto Unicode langs.txt que contenga la línea siguiente:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Asegúrese de guardar el archivo como Unicode.

     

    Copie langs.txt en el directorio desde el que se ejecutará el programa:

    -   Si se ejecuta desde dentro Visual Studio, cópielo en *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Si se ejecuta Windows explorador, cópielo en el mismo directorio que GuiStep \_2.exe.

5.  Compile y ejecute el proyecto. Intente editar langs.txt para que aparezcan idiomas diferentes al frente de la lista.

## <a name="step-5-customizing-hello-mui"></a>Paso 5: Personalizar "Hello MUI"

Algunas de las características en tiempo de ejecución mencionadas hasta ahora en este tutorial solo están disponibles en Windows Vista y versiones posteriores. Es posible que desee volver a usar el esfuerzo invertido en localizar y dividir recursos haciendo que la aplicación funcione en versiones de sistema operativo de nivel inferior Windows, como Windows XP. Este proceso implica ajustar el ejemplo anterior en dos áreas clave:

-   Las funciones de carga de Windows vista previas (como [**LoadString,**](/windows/win32/api/winuser/nf-winuser-loadstringa) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadBitmap,**](/windows/win32/api/winuser/nf-winuser-loadbitmapa) [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)y otras) no son compatible con LAME. Las aplicaciones que se envían con recursos divididos (archivos LN y .mui) deben cargar módulos de recursos mediante una de estas dos funciones:

    -   Si la aplicación se va a ejecutar solo en Windows Vista y versiones posteriores, debe cargar módulos de recursos [**con LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   Si la aplicación se va a ejecutar en versiones anteriores a Windows Vista, así como en Windows Vista o posterior, debe usar [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), que es una función de nivel inferior específica proporcionada en el SDK de Windows 7.

-   La compatibilidad con la administración de idiomas y el orden de reserva de idioma que se ofrecen en versiones anteriores a Windows Vista del sistema operativo Windows difiere significativamente de la de Windows Vista y versiones posteriores. Por esta razón, las aplicaciones que permiten la reserva de idioma configurada por el usuario deben ajustar sus prácticas de administración de idiomas:

    -   Si la aplicación se va a ejecutar solo en Windows Vista y versiones posteriores, es suficiente establecer la lista de idiomas mediante [**SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)
    -   Si la aplicación se va a ejecutar en todas las versiones de Windows, se debe construir código que se ejecutará en plataformas de nivel inferior para recorrer en iteración la lista de idiomas configurada por el usuario y sondear el módulo de recursos deseado. Esto se puede ver en las secciones 1c y 2 del código proporcionado más adelante en este paso.

Cree un proyecto que pueda usar los módulos de recursos localizados en cualquier versión de Windows:

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante la selección de menú Archivo, Agregar y Nuevo Project) con los valores y valores siguientes:

    1.  Project tipo: Win32 Project.
    2.  Nombre: GuiStep \_ 3.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: Windows aplicación.

2.  Establezca este proyecto para que se ejecute desde dentro Visual Studio y configure su modelo de subprocesos. Además, configúrelo para agregar los encabezados y bibliotecas necesarios.

    > [!Note]  
    > Las rutas de acceso usadas en este tutorial suponen que el SDK de Windows 7 y el paquete de API de nivel inferior de Microsoft NLS se instalaron en sus directorios predeterminados. Si ese no es el caso, modifique las rutas de acceso correctamente.

     

    1.  En la Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep 3 y seleccione Establecer como inicio \_ Project.
    2.  Vuelva a hacer clic con el botón derecho en él y seleccione Propiedades.
    3.  En el cuadro de diálogo Páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca Configuración en Todas las configuraciones.
        2.  En Propiedades de configuración, expanda C/C++, seleccione Generación de código y establezca Biblioteca en tiempo de ejecución: Depuración multiproceso (/MTd).
        3.  Seleccione General y agregue a Directorios de incluir adicionales:

            -   "C: \\ Microsoft NLS Downlevel APIs \\ Include".

        4.  Seleccione Idioma y establezca Tratar wchar t como \_ Tipo integrado: No (/Zc:wchar \_ t-).
        5.  Seleccione Avanzadas y establezca Convención de llamada: \_ stdcall (/Gz).
        6.  En Propiedades de configuración, expanda Vinculador, seleccione Entrada y agregue a Dependencias adicionales:

            -   "C: \\ Archivos de programa sdk de Microsoft Windows \\ \\ \\ v7.0 \\ Lib \\ MUILoad.lib".
            -   "C: \\ Microsoft NLS Downlevel APIs \\ Lib \\ x86 \\ Nlsdl.lib".

3.  Reemplace el contenido de GuiStep \_ 3.cpp por el código siguiente:
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Cree o copie langs.txt en el directorio adecuado, como se describió anteriormente en [Paso 4: Globalizar "Hello MUI".](#step-4-globalizing-hello-mui)
5.  Compile y ejecute el proyecto.

> [!Note]  
> Si la aplicación debe ejecutarse en versiones de Windows anteriores a Windows Vista, asegúrese de leer los documentos que se incluyeron con el paquete de API de nivel inferior de [NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) de Microsoft sobre cómo redistribuir Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Consideraciones adicionales para MUI

### <a name="support-for-console-applications"></a>Compatibilidad con aplicaciones de consola

Las técnicas que se tratan en este tutorial también se pueden usar en aplicaciones de consola. Sin embargo, a diferencia de la mayoría de los controles de GUI estándar, Windows ventana de comandos no puede mostrar caracteres para todos los idiomas. Por este motivo, las aplicaciones de consola multilingües requieren una atención especial.

Llamar a las API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con marcas de filtrado específicas hace que las funciones de carga de recursos quiten sondeos de recursos de lenguaje para idiomas específicos que no se muestran normalmente en una ventana de comandos. Cuando se establecen estas marcas, los algoritmos de configuración de idioma solo permiten que los idiomas que se mostrarán correctamente en la ventana de comandos estén en la lista de reserva.

Para obtener más información sobre el uso de estas API para compilar una aplicación de consola multilingüe, vea las secciones comentarios de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) y [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Determinación de los idiomas que se admitirán en Run-Time

Puede adoptar una de las siguientes sugerencias de diseño para determinar qué idiomas debe admitir la aplicación en tiempo de ejecución:

-   **Durante la instalación, habilite al usuario final para seleccionar el idioma preferido de una lista de idiomas admitidos.**

-   **Lectura de una lista de idiomas de un archivo de configuración**

    Algunos de los proyectos de este tutorial contienen una función que se usa para analizar un langs.txt de configuración, que contiene una lista de idiomas.

    Dado que esta función toma una entrada externa, valide los idiomas que se proporcionan como entrada. Vea las [**funciones IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) para obtener más detalles sobre cómo realizar esa validación.

-   **Consultar el sistema operativo para determinar qué idiomas están instalados**

    Este enfoque ayuda a la aplicación a usar el mismo idioma que el sistema operativo. Aunque esto no requiere que el usuario le pida, si elige esta opción, tenga en cuenta que los idiomas del sistema operativo se pueden agregar o quitar en cualquier momento y pueden cambiar después de que el usuario instale la aplicación. Además, tenga en cuenta que, en algunos casos, el sistema operativo se instala con compatibilidad de idioma limitada y la aplicación ofrece más valor si admite idiomas que el sistema operativo no admite.

    Para obtener más información sobre cómo determinar los idiomas instalados actualmente en el sistema operativo, vea la [**función EnumUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Compatibilidad con scripts complejos en versiones anteriores a Windows Vista

Cuando una aplicación que admite determinados scripts complejos se ejecuta en una versión de Windows antes de Windows Vista, es posible que el texto de ese script no se muestre correctamente en los componentes de la GUI. Por ejemplo, en el proyecto de nivel inferior de este tutorial, es posible que los scripts hi-IN y ta-IN no se muestren en el cuadro de mensaje debido a problemas con el procesamiento de scripts complejos y la falta de fuentes relacionadas. Normalmente, los problemas de esta naturaleza se presentan como cuadros cuadrados en el componente gui.

Puede encontrar más información sobre cómo habilitar el procesamiento complejo de scripts en Compatibilidad con scripts y fuentes [en Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Resumen

En este tutorial se globalizó una aplicación monolingüe y se mostraron los siguientes procedimientos recomendados.

-   Diseñe la aplicación para aprovechar el modelo de recursos win32.
-   Utilice la división de LOS RECURSOS en archivos binarios satélite (archivos .mui).
-   Asegúrese de que el proceso de localización actualiza los recursos de los archivos .mui para que sean adecuados para el idioma de destino.
-   Asegúrese de que el empaquetado y la implementación de la aplicación, los archivos .mui asociados y el contenido de configuración se realizan correctamente para permitir que las API de carga de recursos encuentren el contenido localizado.
-   Proporcione al usuario final un mecanismo para ajustar la configuración de idioma de la aplicación.
-   Ajuste el código en tiempo de ejecución para aprovechar las ventajas de la configuración del lenguaje para que la aplicación responda mejor a las necesidades del usuario final.

 

 
