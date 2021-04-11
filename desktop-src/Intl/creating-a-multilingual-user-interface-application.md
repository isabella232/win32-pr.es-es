---
description: En este tutorial se muestra cómo tomar una aplicación Monolingual y hacer que esté lista para el mundo. Esta aplicación está en forma de una solución completa que se compila en Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Agregar compatibilidad con la interfaz de usuario multilingüe a una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912562"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Agregar compatibilidad con la interfaz de usuario multilingüe a una aplicación

En este tutorial se muestra cómo tomar una aplicación Monolingual y hacer que esté lista para el mundo. Esta aplicación está en forma de una solución completa que se compila en Microsoft Visual Studio.

-   [Información general](#splitting-the-various-language-resource-modules-an-overview)
    -   [La idea detrás de Hello MUI](#the-idea-behind-hello-mui)
-   [Configuración de la solución Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Requisitos de la plataforma](#platform-requirements)
    -   [Requisitos previos](#prerequisites)
-   [Paso 0: creación del MUI de Hello codificado de forma rígida](#step-0-creating-the-hard-coded-hello-mui)
-   [Paso 1: implementar el módulo de recursos básico](#step-1-implementing-the-basic-resource-module)
-   [Paso 2: compilar el módulo de recursos básico](#step-2-building-the-basic-resource-module)
    -   [División de los distintos módulos de recursos de idioma: información general](#splitting-the-various-language-resource-modules-an-overview)
    -   [División de los distintos módulos de recursos de idioma: crear los archivos](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Paso 3: creación de un Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Paso 4: globalización de "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Paso 5: personalización de "Hello MUI"](#step-5-customizing-hello-mui)
-   [Consideraciones adicionales para MUI](#additional-considerations-for-mui)
    -   [Compatibilidad con aplicaciones de consola](#support-for-console-applications)
    -   [Determinación de los idiomas que se admiten en tiempo de ejecución](#determination-of-languages-to-support-at-run-time)
    -   [Compatibilidad con scripts complejos en versiones anteriores a Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Resumen](#summary)

## <a name="overview"></a>Información general

A partir de Windows Vista, el propio sistema operativo Windows se creó desde el principio para ser una plataforma multilingüe, con compatibilidad adicional que le permite crear aplicaciones multilingües que usan el modelo de recursos de Windows MUI.

En este tutorial se muestra esta nueva compatibilidad con aplicaciones multilingües, cubriendo los aspectos siguientes:

-   Usa la compatibilidad con la plataforma MUI mejorada para habilitar fácilmente aplicaciones multilingües.
-   Extiende las aplicaciones multilingües para que se ejecuten en versiones de Windows anteriores a Windows Vista.
-   Toca las consideraciones adicionales implicadas en el desarrollo de aplicaciones multilingües especializadas, como aplicaciones de consola.

Estos vínculos ayudan a proporcionar un actualizador rápido sobre los conceptos sobre internacionalización y MUI:

-   [Información general rápida de internacionalización](understanding-internationalization.md).
-   [Conceptos de MUI](understanding-mui.md).
-   [Usar MUI para desarrollar aplicaciones Win32](using-multilingual-user-interface.md).

### <a name="the-idea-behind-hello-mui"></a>La idea detrás de Hello MUI

Probablemente esté familiarizado con la aplicación Hola mundo clásica, que muestra los conceptos básicos de la programación. Este tutorial tiene un enfoque similar para ilustrar cómo usar el modelo de recursos de MUI para actualizar una aplicación de Monolingual para crear una versión multilingüe denominada Hola MUI.

> [!Note]  
> Las tareas de este tutorial se describen en pasos detallados debido a la precisión con la que se deben realizar estas actividades y la necesidad de explicar los detalles a los desarrolladores que tienen poca experiencia con estas tareas.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configuración de la solución Hello MUI

En estos pasos se describe cómo preparar la creación de la solución Hello MUI.

### <a name="platform-requirements"></a>Requisitos de la plataforma

Debe compilar los ejemplos de código de este tutorial con el kit de desarrollo de software (SDK) de Windows para Windows 7 y Visual Studio 2008. El SDK de Windows 7 se instalará en Windows XP, Windows Vista y Windows 7, y la solución de ejemplo se puede crear en cualquiera de estas versiones de sistema operativo.

Todos los ejemplos de código de este tutorial están diseñados para ejecutarse en las versiones x86 y x64 de Windows XP, Windows Vista y Windows 7. Las partes específicas que no funcionarán en Windows XP se indican donde corresponda.

### <a name="prerequisites"></a>Requisitos previos

1.  Instale Visual Studio 2008.

    Para obtener más información, vea el [Centro para desarrolladores de Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).

2.  Instale el Windows SDK para Windows 7.

    Puede instalarlo desde la página Windows SDK del centro para [desarrolladores de Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx). El SDK incluye utilidades para desarrollar aplicaciones para versiones del sistema operativo a partir de Windows XP a través del más reciente.

    > [!Note]  
    > Si no va a instalar el paquete en la ubicación predeterminada, o si no está instalando en la unidad del sistema, que normalmente es la unidad C, tome nota de la ruta de instalación.

     

3.  Configure los parámetros de línea de comandos de Visual Studio.

    1.  Abra una ventana de comandos de Visual Studio.
    2.  Escriba **set path**.
    3.  Confirme que la variable PATH incluye la ruta de acceso de la carpeta bin del SDK de Windows 7:... Microsoft SDK \\ Windows \\ v 7.0 \\ bin

4.  Instale el paquete del complemento Microsoft NLS Downlevel API.
    > [!Note]  
    > En el contexto de este tutorial, este paquete solo es necesario si va a personalizar la aplicación para que se ejecute en versiones de Windows anteriores a Windows Vista. Vea [STEP 5: customizating Hello mui](#step-5-customizing-hello-mui).

     

    1.  Descargue e instale el paquete desde su [sitio de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).
    2.  Al igual que con el Windows SDK, si no va a instalar el paquete en la ubicación predeterminada, o si no está instalando en la unidad del sistema, que normalmente es la unidad C, anote la ruta de instalación.
    3.  Si la plataforma de desarrollo es Windows XP o Windows Server 2003, confirme que Nlsdl.dll esté instalado y registrado correctamente.

        1.  Vaya a la carpeta "Redist" en la ubicación de la ruta de instalación.
        2.  Ejecute el nlsdl redistribuible adecuado \* . exe, como nlsdl.x86.exe. En este paso se instalan y registran Nlsdl.dll.

    > [!Note]  
    > Si desarrolla una aplicación que usa MUI y que se debe ejecutar en versiones de Windows anteriores a Windows Vista, Nlsdl.dll debe estar presente en la plataforma de Windows de destino. En la mayoría de los casos, esto significa que la aplicación debe llevar e instalar el instalador redistribuible de nlsdl (y no simplemente copiar Nlsdl.dll).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Paso 0: creación del MUI de Hello codificado de forma rígida

Este tutorial comienza con la versión Monolingual de la aplicación Hello MUI. La aplicación asume el uso del lenguaje de programación C++, las cadenas de caracteres anchos y la función [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) para la salida.

Empiece por crear la aplicación GuiStep \_ 0 inicial, así como la solución HelloMUI, que contiene todas las aplicaciones de este tutorial.

1.  En Visual Studio 2008, cree un nuevo proyecto. Use los valores y valores siguientes:

    1.  Tipo de proyecto: en Visual C++ Seleccione Win32 y, después, en plantillas instaladas de Visual Studio, seleccione proyecto Win32.
    2.  Nombre: GuiStep \_ 0.
    3.  Ubicación: *ProjectRootDirectory* (los pasos posteriores hacen referencia a este directorio).
    4.  Nombre de la solución: HelloMUI.
    5.  Seleccione Crear directorio para la solución.
    6.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.

2.  Configure el modelo de subprocesos del proyecto:

    1.  En el Explorador de soluciones, haga clic con el botón secundario en el proyecto GuiStep \_ 0 y, a continuación, seleccione Propiedades.
    2.  En el cuadro de diálogo páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.
        2.  En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 0. cpp por el código siguiente:
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

El código fuente sencillo anterior hace que la opción de diseño simplista de la codificación o la inserción se realice de forma rígida, todo el resultado que verá el usuario (en este caso, el texto "Hello MUI"). Esta opción limita la utilidad de la aplicación para los usuarios que no reconocen la palabra "Hola" en inglés. Dado que MUI es un acrónimo en inglés basado en la tecnología, en este tutorial se supone que la cadena sigue siendo "MUI" para todos los idiomas.

## <a name="step-1-implementing-the-basic-resource-module"></a>Paso 1: implementar el módulo de recursos básico

Microsoft Win32 ha expuesto la capacidad de los desarrolladores de aplicaciones para separar los datos de recursos de la interfaz de usuario del código fuente de la aplicación. Esta separación tiene el formato del modelo de recursos de Win32, en el que las cadenas, mapas de bits, iconos, mensajes y otros elementos que se muestran normalmente a un usuario se empaquetan en una sección distinta del archivo ejecutable, separadas del código ejecutable.

Para ilustrar esta separación entre el código ejecutable y el empaquetado de datos de recursos, en este paso, el tutorial coloca la cadena "Hello" codificada previamente (el recurso "en-US") en la sección de recursos de un módulo DLL del \_ proyecto HelloModule en \_ EE. UU.

Este archivo DLL de Win32 también puede contener la funcionalidad ejecutable de tipo de biblioteca (como cualquier otro archivo DLL). Pero para ayudar a centrarse en los aspectos relacionados con los recursos de Win32, dejamos en DllMain. cpp el código DLL en tiempo de ejecución. Las secciones siguientes de este tutorial hacen uso de los datos de recursos de HelloModule que se crean aquí y también presentan el código de tiempo de ejecución adecuado.

Para construir un módulo de recursos de Win32, empiece por crear un archivo DLL con una función DllMain de stub:

1.  Agregue un nuevo proyecto a la solución HelloMUI:

    1.  En el menú Archivo, seleccione Agregar y, a continuación, nuevo proyecto.
    2.  Tipo de proyecto: proyecto Win32.
    3.  Nombre: HelloModule \_ en \_ EE. UU.
    4.  Ubicación: *ProjectRootDirectory* \\ HelloMUI.
    5.  En el Asistente para aplicaciones Win32, seleccione tipo de aplicación: DLL.

2.  Configure el modelo de subprocesos de este proyecto:

    1.  En el Explorador de soluciones, haga clic con el botón derecho en el proyecto HelloModule \_ en \_ US y seleccione Propiedades.
    2.  En el cuadro de diálogo páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.
        2.  En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).

3.  Examine DllMain. cpp. (Puede que desee agregar el no REFERENCIAdo \_ Las macros de parámetros al código generado, como tenemos aquí, para permitir que se compile en el nivel de ADVERTENCIA 4).
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

    

4.  Agregue un archivo de definición de recursos HelloModule. rc al proyecto:

    1.  En el proyecto HelloModule \_ en \_ EE. UU., haga clic con el botón derecho en la carpeta archivos de recursos, seleccione Agregar y, a continuación, seleccione nuevo elemento.
    2.  En el cuadro de diálogo Agregar nuevo elemento, elija lo siguiente:

        1.  Categorías: en Visual C++ Seleccione recurso y, en "plantillas instaladas de Visual Studio", seleccione Archivo de recursos (. RC).
        2.  Nombre: HelloModule.
        3.  Ubicación: acepte el valor predeterminado.
        4.  Haga clic en Agregar.

    3.  Especifique que el nuevo archivo HelloModule. RC se va a guardar como Unicode:

        1.  En el Explorador de soluciones, haga clic con el botón secundario en HelloModule. RC y seleccione Ver código.
        2.  Si ve un mensaje que le indica que el archivo ya está abierto y pregunta si desea cerrarlo, haga clic en sí.
        3.  Con el archivo mostrado como texto, cree el archivo de selección de menú y, a continuación, opciones avanzadas para guardar.
        4.  En codificación, especifique Unicode-CodePage 1200.
        5.  Haga clic en Aceptar.
        6.  Guarde y cierre HelloModule. rc.

    4.  Agregue una tabla de cadenas que contenga la cadena "Hello":

        1.  En el Vista de recursos, haga clic con el botón secundario en HelloModule. RC y seleccione Agregar recurso.
        2.  Seleccione Tabla de cadenas.
        3.  Haga clic en Nuevo.
        4.  Agregue una cadena a la tabla de cadenas:

            1.  ID: HELLO \_ mui \_ Str Str \_ 0.
            2.  Valor: 0.
            3.  Título: Hola.

        Si ve HelloModule. RC como texto ahora, verá varias partes del código fuente específico del recurso. El mayor interés es la sección que describe la cadena "Hello":

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

        

        Esta cadena "Hello" es el recurso que debe localizarse (es decir, traducirse) en cada idioma que la aplicación espera que admita. Por ejemplo, el HelloModule \_ TA \_ en el proyecto (que creará en el paso siguiente) contendrá su propia versión localizada de HelloModule. RC para "TA-in":

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

        

    5.  Compile el \_ proyecto HelloModule en \_ US para asegurarse de que no hay errores.

5.  Cree seis proyectos más en la solución HelloMUI (o como muchos de los deseados) para crear seis dll de recursos más para otros idiomas. Use los valores de esta tabla:

    | Nombre de proyecto        | Nombre del archivo. RC | Identificador de cadena          | Valor de cadena | Título de cadena |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | Hallo          |
    | HelloModule \_ es \_ es | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | Bonjour        |
    | HelloModule \_ HI \_ en | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | नमस्           |
    | HelloModule \_ RU \_ RU | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ TA \_ | HelloModule      | HELLO \_ mui \_ Str Str \_ 0 | 0            | வணக்கம்        |

    

     

Para obtener más información sobre la sintaxis y la estructura del archivo. rc, consulte [acerca de los archivos de recursos](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Paso 2: compilar el módulo de recursos básico

Con los modelos de recursos anteriores, la creación de uno de los siete proyectos HelloModule daría como resultado siete dll independientes. Cada archivo DLL contiene una sección de recursos con una sola cadena localizada en el idioma adecuado. Aunque es adecuado para el modelo de recursos históricos de Win32, este diseño no aprovecha MUI.

En el SDK de Windows Vista y versiones posteriores, MUI proporciona la capacidad de dividir los ejecutables en módulos de contenido localizable y código fuente. Con la personalización adicional que se trata más adelante en el paso 5, las aplicaciones pueden estar habilitadas para que la compatibilidad con varios idiomas se ejecute en versiones anteriores a Windows Vista.

Los mecanismos principales disponibles para dividir los recursos del código ejecutable, a partir de Windows Vista, son los siguientes:

-   Usar rc.exe (el compilador de RC) con modificadores específicos, o
-   Usar una herramienta de división de estilo posterior a la compilación denominada muirct.exe.

Consulte [utilidades de recursos](resource-utilities.md) para obtener más información.

Por simplicidad, en este tutorial se usa muirct.exe para dividir el archivo ejecutable "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>División de los distintos módulos de recursos de idioma: información general

Un proceso de varias partes implica dividir los archivos dll en un HelloModule.dll ejecutable, además de un HelloModule.dll. MUI para cada uno de los siete idiomas admitidos en este tutorial. En esta información general se describen los pasos necesarios; en la sección siguiente se muestra un archivo de comandos que realiza esos pasos.

En primer lugar, divida el módulo de HelloModule.dll solo en inglés con el comando:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



La línea de comandos anterior usa el archivo de configuración DoReverseMuiLoc. rcconfig. Normalmente, muirct.exe usa este tipo de archivo de configuración para dividir los recursos entre el archivo DLL del lenguaje neutro (LN) y los archivos. mui dependientes del lenguaje. En este caso, el archivo XML DoReverseMuiLoc. rcconfig (que se muestra en la sección siguiente) indica muchos tipos de recursos, pero todos se encuentran en la categoría de archivos "localizedResources" o. mui y no hay ningún recurso en la categoría de idioma neutro. Para obtener más información sobre cómo preparar un archivo de configuración de recursos, vea [preparar un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).

Además de crear un archivo HelloModule.dll. mui que contiene la cadena en inglés "Hello", muirct.exe también inserta un recurso de MUI en el módulo de HelloModule.dll durante la división. Con el fin de cargar correctamente en tiempo de ejecución los recursos adecuados desde los módulos de HelloModule.dll. mui específicos del idioma, cada archivo. mui debe tener sus sumas de comprobación fijas para que coincidan con las sumas de comprobación en el módulo LN del lenguaje de línea de base. Esto se realiza mediante un comando como:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Del mismo modo, muirct.exe se invoca para crear un archivo HelloModule.dll. MUI para cada uno de los demás idiomas. Sin embargo, en esos casos se descarta el archivo DLL independiente del lenguaje, ya que solo se necesitará el primero que se cree. Los comandos que procesan los recursos español y francés tienen el siguiente aspecto:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Uno de los aspectos más importantes que se deben tener en cuenta en el muirct.exe las líneas de comandos anteriores es que la marca-x se usa para especificar un identificador de idioma de destino. El valor proporcionado para muirct.exe es diferente para cada módulo de HelloModule.dll específico del idioma. Este valor de idioma es central y lo usa muirct.exe para marcar correctamente el archivo. mui durante la división. Un valor incorrecto produce errores de carga de recursos para ese archivo. mui determinado en tiempo de ejecución. Consulte [constantes y cadenas de identificador de idioma](language-identifier-constants-and-strings.md) para obtener más detalles sobre cómo asignar el nombre del idioma a LCID.

Cada archivo Split. mui termina de colocarse en un directorio que se corresponde con su nombre de idioma, inmediatamente debajo del directorio en el que residirá el HelloModule.dll independiente del lenguaje. Para obtener más información sobre la ubicación de los archivos. MUI, vea [implementación de aplicaciones](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>División de los distintos módulos de recursos de idioma: crear los archivos

En este tutorial se crea un archivo de comandos que contiene los comandos para dividir los distintos archivos dll y se invoca manualmente. Tenga en cuenta que, en el trabajo de desarrollo real, puede reducir la posibilidad de que se produzcan errores de compilación al incluir estos comandos como eventos anteriores o posteriores a la compilación en la solución HelloMUI, pero eso está fuera del ámbito de este tutorial.

Cree los archivos para la compilación de depuración:

1.  Cree un archivo de comandos DoReverseMuiLoc. cmd que contenga los siguientes comandos:
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

    

2.  Cree un archivo XML DoReverseMuiLoc. rcconfig que contenga las líneas siguientes:
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

    

3.  Copie DoReverseMuiLoc. cmd y DoReverseMuiLoc. rcconfig en *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  Abra el símbolo del sistema de Visual Studio 2008 y navegue hasta el directorio de depuración.
5.  Ejecute DoReverseMuiLoc. cmd.

Al crear una compilación de versión, copie los mismos archivos DoReverseMuiLoc. cmd y DoReverseMuiLoc. rcconfig en el directorio de versión y ejecute el archivo de comandos allí.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Paso 3: creación de un Resource-Savvy "Hello MUI"

Al basarse en el \_ ejemplo de GuiStep0.exe codificado de forma rígida anterior, podría ampliar el alcance de la aplicación a varios usuarios de lenguajes si opta por incorporar el modelo de recursos de Win32. El nuevo código en tiempo de ejecución presentado en este paso incluye la lógica de carga de módulos ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) y de recuperación de cadenas ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:

    1.  Tipo de proyecto: proyecto Win32.
    2.  Nombre: GuiStep \_ 1.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.

2.  Establezca este proyecto para que se ejecute desde dentro de Visual Studio y configure su modelo de subprocesos:

    1.  En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 1 y seleccione establecer como proyecto de inicio.
    2.  Vuelva a hacer clic con el botón secundario y seleccione Propiedades.
    3.  En el cuadro de diálogo páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.
        2.  En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 1. cpp por el código siguiente:
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

    

4.  Compile y ejecute la aplicación. El resultado se mostrará en el idioma establecido actualmente como el idioma de visualización del equipo (siempre que sea uno de los siete idiomas que hemos creado).

## <a name="step-4-globalizing-hello-mui"></a>Paso 4: globalización de "Hello MUI"

Aunque el ejemplo anterior es capaz de mostrar su salida en distintos idiomas, es breve en varias áreas. Quizás lo más notable es que la aplicación solo está disponible en un pequeño subconjunto de idiomas en comparación con el propio sistema operativo Windows. Si, por ejemplo, la \_ aplicación GuiStep 1 del paso anterior se instalaba en una compilación en japonés de Windows, es probable que se produzcan errores de ubicación de recursos.

Para solucionar esta situación, tiene dos opciones principales:

-   Asegúrese de que se incluyen los recursos de un idioma de reserva Ultimate predeterminados.
-   Proporcionar una manera para que el usuario final Configure sus preferencias de idioma entre el subconjunto de idiomas admitidos específicamente por la aplicación.

De estas opciones, el que proporciona un lenguaje de reserva final es muy aconsejable y se implementa en este tutorial pasando la marca-g a muirct.exe, como se ha mencionado anteriormente. Esta marca indica muirct.exe para convertir un idioma específico (de-DE/0x0407) en el idioma de reserva final asociado con el módulo DLL independiente del lenguaje (HelloModule.dll). En tiempo de ejecución, este parámetro se utiliza como último recurso para generar el texto que se va a mostrar al usuario. En caso de que no se encuentre un idioma de reserva final y no haya ningún recurso adecuado disponible en el binario independiente del lenguaje, se producirá un error al cargar el recurso. Por lo tanto, debe determinar cuidadosamente los escenarios en los que puede encontrarse la aplicación y planear el lenguaje de reserva final en consecuencia.

La otra opción de permitir las preferencias de idioma configurables y cargar recursos basados en esta jerarquía definida por el usuario puede aumentar considerablemente la satisfacción del cliente. Desafortunadamente, también complica la funcionalidad necesaria dentro de la aplicación.

Este paso del tutorial usa un mecanismo de archivo de texto simplificado para habilitar la configuración de idioma del usuario personalizado. La aplicación analiza el archivo de texto en tiempo de ejecución, y la lista de idiomas analizados y validados se usa para establecer una lista de reserva personalizada. Una vez establecida la lista de reserva personalizada, las API de Windows cargarán los recursos según la prioridad de idioma establecida en esta lista. El resto del código es similar al que se encontró en el paso anterior.

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:

    1.  Tipo de proyecto: proyecto Win32.
    2.  Nombre: GuiStep \_ 2.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.

2.  Establezca este proyecto para que se ejecute desde dentro de Visual Studio y configure su modelo de subprocesos:

    1.  En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 2 y seleccione establecer como proyecto de inicio.
    2.  Vuelva a hacer clic con el botón secundario y seleccione Propiedades.
    3.  En el cuadro de diálogo páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.
        2.  En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).

3.  Reemplace el contenido de GuiStep \_ 2. cpp por el código siguiente:
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

    -   Si se ejecuta desde dentro de Visual Studio, cópielo en *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Si se ejecuta desde el explorador de Windows, cópielo en el mismo directorio que GuiStep \_2.exe.

5.  Compile y ejecute el proyecto. Intente editar langs.txt para que aparezcan distintos idiomas al principio de la lista.

## <a name="step-5-customizing-hello-mui"></a>Paso 5: personalización de "Hello MUI"

Una serie de las características en tiempo de ejecución que se mencionan hasta ahora en este tutorial solo están disponibles en Windows Vista y versiones posteriores. Es posible que desee volver a usar el esfuerzo invertido en la localización y la división de recursos haciendo que la aplicación funcione en versiones anteriores del sistema operativo Windows, como Windows XP. Este proceso implica ajustar el ejemplo anterior en dos áreas clave:

-   Las funciones de carga de recursos anteriores a Windows Vista (como [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**loadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)y otras) no reconocen MUI. Las aplicaciones que se distribuyen con recursos divididos (archivos LN y. MUI) deben cargar los módulos de recursos mediante una de estas dos funciones:

    -   Si la aplicación solo se va a ejecutar en Windows Vista y versiones posteriores, debe cargar los módulos de recursos con [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   Si la aplicación se va a ejecutar en versiones anteriores a Windows Vista, así como en Windows Vista o posterior, debe usar [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), que es una función de nivel inferior específica que se proporciona en el SDK de Windows 7.

-   La compatibilidad con la administración de idiomas y el orden de reserva de idioma que se ofrece en las versiones anteriores a Windows Vista del sistema operativo Windows difiere significativamente de la de Windows Vista y versiones posteriores. Por este motivo, las aplicaciones que permiten la reserva de idiomas configurados por el usuario deben ajustar sus prácticas de administración de idioma:

    -   Si la aplicación solo se va a ejecutar en Windows Vista y versiones posteriores, basta con establecer la lista de idiomas con [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .
    -   Si la aplicación se va a ejecutar en todas las versiones de Windows, se debe construir código que se ejecutará en plataformas de nivel inferior para recorrer en iteración la lista de idiomas configurados por el usuario y sondear el módulo de recursos deseado. Esto se puede observar en las secciones 1C y 2 del código que se proporciona más adelante en este paso.

Cree un proyecto que pueda usar los módulos de recursos localizados en cualquier versión de Windows:

1.  Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:

    1.  Tipo de proyecto: proyecto Win32.
    2.  Nombre: GuiStep \_ 3.
    3.  Ubicación: acepte el valor predeterminado.
    4.  En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.

2.  Establezca este proyecto para que se ejecute desde Visual Studio y configure su modelo de subprocesos. Además, configúrelo para agregar los encabezados y las bibliotecas necesarios.

    > [!Note]  
    > Las rutas de acceso que se usan en este tutorial suponen que el SDK de Windows 7 y el paquete de las API de Microsoft NLS Downlevel se instalaron en sus directorios predeterminados. Si no es así, modifique las rutas de acceso de forma adecuada.

     

    1.  En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 3 y seleccione establecer como proyecto de inicio.
    2.  Vuelva a hacer clic con el botón secundario y seleccione Propiedades.
    3.  En el cuadro de diálogo páginas de propiedades del proyecto:

        1.  En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.
        2.  En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).
        3.  Seleccione general y agregar a directorios de inclusión adicionales:

            -   "C: las \\ API de Microsoft NLS Downlevel \\ incluyen".

        4.  Seleccione idioma y establezca tratar WCHAR \_ t como tipo integrado: no (/ZC: WCHAR \_ t-).
        5.  Seleccione avanzadas y establezca Convención de llamada: \_ Stdcall (/gz).
        6.  En propiedades de configuración, expanda enlazador, seleccione entrada y agregue a dependencias adicionales:

            -   "C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib".
            -   "C: \\ Microsoft NLS Downlevel API \\ lib \\ x86 \\ nlsdl. lib".

3.  Reemplace el contenido de GuiStep \_ 3. cpp por el código siguiente:
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

    

4.  Cree o copie langs.txt en el directorio adecuado, tal y como se describe anteriormente en el [paso 4: globalizar "Hello mui"](#step-4-globalizing-hello-mui).
5.  Compile y ejecute el proyecto.

> [!Note]  
> Si la aplicación se debe ejecutar en versiones de Windows anteriores a Windows Vista, asegúrese de leer los documentos que se incluían con el paquete de las [API de Microsoft NLS de nivel inferior](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) sobre cómo redistribuir Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Consideraciones adicionales para MUI

### <a name="support-for-console-applications"></a>Compatibilidad con aplicaciones de consola

Las técnicas que se describen en este tutorial también se pueden usar en aplicaciones de consola. Sin embargo, a diferencia de la mayoría de los controles estándar de la interfaz gráfica de usuario, la ventana comandos de Windows no puede mostrar caracteres para todos los idiomas. Por este motivo, las aplicaciones de consola multilingüe requieren atención especial.

La llamada a las API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con marcas de filtrado específicas hace que las funciones de carga de recursos quiten los sondeos de recursos de idioma para los idiomas específicos que normalmente no se muestran en una ventana de comandos. Cuando se establecen estas marcas, los algoritmos de configuración de lenguaje solo permiten que los idiomas que se mostrarán correctamente en la ventana de comandos estén en la lista de reserva.

Para obtener más información sobre el uso de estas API para compilar una aplicación de consola multilingüe, vea las secciones comentarios de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) y [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Determinación de los idiomas que se admiten en Run-Time

Puede adoptar una de las siguientes sugerencias de diseño para determinar qué idiomas debe admitir la aplicación en tiempo de ejecución:

-   **Durante la instalación, permita que el usuario final Seleccione el idioma preferido en la lista de idiomas admitidos.**

-   **Leer una lista de idiomas de un archivo de configuración**

    Algunos de los proyectos de este tutorial contienen una función que se usa para analizar un archivo de configuración de langs.txt, que contiene una lista de idiomas.

    Dado que esta función toma una entrada externa, valide los idiomas que se proporcionan como entrada. Vea las funciones [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) para obtener más información sobre cómo realizar esa validación.

-   **Consultar el sistema operativo para determinar qué idiomas están instalados**

    Este enfoque ayuda a la aplicación a usar el mismo idioma que el sistema operativo. Aunque esto no requiere la solicitud del usuario, si elige esta opción, tenga en cuenta que los idiomas del sistema operativo se pueden agregar o quitar en cualquier momento y pueden cambiar después de que el usuario instale la aplicación. Además, tenga en cuenta que, en algunos casos, el sistema operativo se instala con compatibilidad de idioma limitado y la aplicación ofrece más valor si es compatible con los idiomas que el sistema operativo no admite.

    Para obtener más información sobre cómo determinar los idiomas instalados actualmente en el sistema operativo, consulte la función [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Compatibilidad con scripts complejos en versiones anteriores a Windows Vista

Cuando una aplicación que admite determinados scripts complejos se ejecuta en una versión de Windows anterior a Windows Vista, es posible que el texto de ese script no se muestre correctamente en los componentes de la GUI. Por ejemplo, en el proyecto de nivel inferior de este tutorial, es posible que no se muestren los scripts de alta y escritura en el cuadro de mensaje debido a problemas con el procesamiento de scripts complejos y la falta de fuentes relacionadas. Normalmente, los problemas de esta naturaleza aparecen como cuadros cuadrados en el componente GUI.

Puede encontrar más información sobre cómo habilitar el procesamiento complejo de scripts en [compatibilidad con scripts y fuentes en Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Resumen

En este tutorial se ha globalizado una aplicación Monolingual y se han mostrado las siguientes prácticas recomendadas.

-   Diseñe la aplicación para aprovechar las ventajas del modelo de recursos de Win32.
-   Use la división de los recursos de MUI en binarios satélite (archivos. MUI).
-   Asegúrese de que el proceso de localización actualiza los recursos de los archivos. MUI para que sean adecuados para el idioma de destino.
-   Asegúrese de que el empaquetado y la implementación de la aplicación, los archivos. mui asociados y el contenido de configuración se realizan correctamente para permitir que las API de carga de recursos encuentren el contenido localizado.
-   Proporcionar al usuario final un mecanismo para ajustar la configuración de idioma de la aplicación.
-   Ajuste el código en tiempo de ejecución para aprovechar las ventajas de la configuración de idioma para que la aplicación responda mejor a las necesidades de los usuarios finales.

 

 
