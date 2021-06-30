---
title: Habilitar los estilos visuales
description: En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102174"
---
# <a name="enabling-visual-styles"></a>Habilitar los estilos visuales

En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.

En este tema se incluyen las secciones siguientes.

-   [Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Usar ComCtl32 versión 6 en Panel de control o un archivo DLL que ejecuta RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Agregar compatibilidad con el estilo visual a una extensión, un complemento, un complemento MMC o un archivo DLL que se incorpora a un proceso](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Desactivar estilos visuales](#turning-off-visual-styles)
-   [Usar estilos visuales con contenido HTML](#using-visual-styles-with-html-content)
-   [Cuando no se aplican estilos visuales](#when-visual-styles-are-not-applied)
-   [Hacer que la aplicación sea compatible con versiones anteriores de Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Temas relacionados](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones

Para permitir que la aplicación use estilos visuales, debe usar ComCtl32.dll versión 6 o posterior. Dado que la versión 6 no es redistribuible, solo está disponible cuando la aplicación se ejecuta en una versión de Windows que la contiene. Windows se suministra con las versiones 5 y 6. ComCtl32.dll versión 6 contiene los controles de usuario y los controles comunes. De forma predeterminada, las aplicaciones usan los controles de usuario definidos en User32.dll y los controles comunes definidos en ComCtl32.dll versión 5. Para obtener una lista de las versiones de DLL y sus plataformas de distribución, vea [Versiones de control comunes](common-control-versions.md).

Si desea que la aplicación use estilos visuales, debe agregar un manifiesto de aplicación o una directiva del compilador que indique que se debe usar ComCtl32.dll versión 6 si está disponible.

Un manifiesto de aplicación permite a una aplicación especificar qué versiones de un ensamblado requiere. En Microsoft Win32, un ensamblado es un conjunto de archivos DLL y una lista de objetos con control de versiones que se encuentran dentro de esos archivos DLL.

Los manifiestos se escriben en XML. El nombre del archivo de manifiesto de aplicación es el nombre del ejecutable seguido de la extensión de nombre de archivo .manifest; por ejemplo, MyApp.exe.manifest. En el siguiente manifiesto de ejemplo se muestra que la primera sección describe el propio manifiesto. En la tabla siguiente se muestran los atributos establecidos por el **elemento assemblyIdentity** en la sección de descripción del manifiesto.



| Atributo             | Descripción                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versión del manifiesto. La versión debe tener el formato major.minor.revision.build (es decir, n.n.n.n, donde n <=65535). |
| processorArchitecture | Procesador para el que se desarrolla la aplicación.                                                                          |
| name                  | Incluye el nombre de la empresa, el nombre del producto y el nombre de la aplicación.                                                                   |
| type                  | Tipo de aplicación, como Win32.                                                                                    |



 

El manifiesto de ejemplo también proporciona una descripción de la aplicación y especifica las dependencias de la aplicación. En la tabla siguiente se muestran los atributos establecidos por el **elemento assemblyIdentity** en la sección de dependencia.



| Atributo             | Descripción                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo del componente de dependencia, como Win32. |
| name                  | Nombre del componente.                           |
| version               | Versión del componente.                        |
| processorArchitecture | Procesador para el que está diseñado el componente.    |
| Publickeytoken        | Token de clave usado con este componente.              |
| language              | Idioma del componente.                       |



 

A continuación se muestra un ejemplo de un archivo de manifiesto.

> [!IMPORTANT]
> Establezca la entrada **processorArchitecture** en **"X86"** si la aplicación tiene como destino la plataforma Windows de 32 bits o **en "amd64"** si la aplicación tiene como destino la plataforma windows de 64 bits. También puede especificar **\* "",** lo que garantiza que todas las plataformas están destinadas, como se muestra en los ejemplos siguientes.

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



Si usa Microsoft Visual C++ 2005 o posterior, puede agregar la siguiente directiva del compilador al código fuente en lugar de crear manualmente un manifiesto. Para mejorar la legibilidad, la directiva se divide en varias líneas aquí.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



En los temas siguientes se describen los pasos para aplicar estilos visuales a diferentes tipos de aplicaciones. Observe que el formato del manifiesto es el mismo en cada caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar

A continuación se muestran ejemplos de aplicaciones que no usan extensiones de terceros.

-   Calculadora
-   FreeCell (en Windows Vista y Windows 7)
-   Minesweeper (en Windows Vista y Windows 7)
-   Bloc de notas
-   Porrón (en Windows Vista y Windows 7)

**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**

1.  Vincule a ComCtl32.lib y llame a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Agregue un archivo denominado YourApp.exe.manifest al árbol de origen que tenga el formato de manifiesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Agregue el manifiesto al archivo de recursos de la aplicación como se muestra a continuación:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Al agregar la entrada anterior al recurso, debe formatearla en una línea. Como alternativa, puede colocar el archivo de manifiesto XML en el mismo directorio que el archivo ejecutable de la aplicación. El sistema operativo cargará primero el manifiesto desde el sistema de archivos y, a continuación, comprobará la sección de recursos del ejecutable. La versión del sistema de archivos tiene prioridad.

     

Al compilar la aplicación, el manifiesto se agregará como un recurso binario.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Usar ComCtl32 versión 6 en Panel de control o un archivo DLL ejecutado por RunDll32.exe

**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**

1.  Vincule a ComCtl32.lib y llame a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Agregue un archivo denominado YourApp.cpl.manifest al árbol de origen que tenga el formato de manifiesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Agregue el manifiesto al archivo de recursos de la aplicación como id. de recurso 123.

> [!Note]  
> Al crear una aplicación Panel de control, coló hay que colocarla en la categoría adecuada. Panel de control ahora admite la categorización de Panel de control aplicaciones. Esto significa que Panel de control a las aplicaciones se les pueden asignar identificadores y separarse en áreas de tareas, como Agregar o quitar programas, Apariencia y temas, o Fecha, Hora, Idioma y Opciones regionales.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Agregar compatibilidad de estilo visual a una extensión, un complemento, un complemento MMC o un archivo DLL que se incorpora a un proceso

Se puede agregar compatibilidad con estilos visuales a una extensión, un complemento, un complemento MMC o un archivo DLL que se lleva a un proceso. Por ejemplo, siga estos pasos para agregar compatibilidad con estilos visuales para un complemento Microsoft Management Console (MMC).

1.  Compile el complemento con la marca -DISOLATION AWARE ENABLED o inserte la siguiente instrucción antes de \_ \_ incluir la instrucción \# "windows.h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Para obtener más información sobre ISOLATION \_ AWARE \_ ENABLED, vea [Aislar componentes](/windows/desktop/SbsCs/isolating-components).

2.  Incluya el archivo de encabezado de control común en el origen del complemento.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Agregue un archivo denominado YourApp.manifest al árbol de origen que use el formato de manifiesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  Agregue el manifiesto al archivo de recursos del complemento. Consulte [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins,](/previous-versions//ms649781(v=vs.85)) or a DLL That Is Brought into a Process (Uso de ComCtl32 versión 6 en una aplicación que usa extensiones, complementos o un archivo DLL que se incorpora a un proceso) para obtener más información sobre cómo agregar un manifiesto a un archivo de recursos.

## <a name="turning-off-visual-styles"></a>Desactivar estilos visuales

Puede desactivar los estilos visuales de un control o de todos los controles de una ventana llamando a la [**función SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) como se muestra a continuación:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



En el ejemplo anterior, *hwnd* es el identificador de la ventana en la que se deshabilitan los estilos visuales. Después de la llamada, el control se representa sin estilos visuales.

## <a name="using-visual-styles-with-html-content"></a>Usar estilos visuales con contenido HTML

Las páginas HTML que modifican Hojas de estilo CSS (CSS) como el fondo o el borde no tienen estilos visuales aplicados. Muestran el atributo CSS especificado. Cuando se especifica como parte del contenido, la mayoría de las propiedades CSS se aplican a los elementos que tienen estilos visuales aplicados.

De forma predeterminada, los estilos visuales se aplican a controles HTML intrínsecos en las páginas mostradas en Microsoft Internet Explorer 6 y versiones posteriores. Para desactivar los estilos visuales de una página HTML, agregue una etiqueta META a <head> . Esta técnica también se aplica al contenido empaquetado como aplicaciones HTML (HTA). Para desactivar los estilos visuales, la etiqueta META debe ser la siguiente:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Si la configuración del explorador y la configuración de etiqueta no están de acuerdo, la página no aplicará estilos visuales. Por ejemplo, si la etiqueta META se establece en "no" y el explorador está establecido para habilitar estilos visuales, los estilos visuales no se aplicarán a la página. Sin embargo, si el explorador o la etiqueta META se establecen en "sí" y no se especifica el otro elemento, se aplicarán estilos visuales.

 

Los estilos visuales pueden cambiar el diseño del contenido. Además, si establece determinados atributos en controles HTML intrínsecos, como el ancho de un botón, es posible que la etiqueta del botón sea ilegible en determinados estilos visuales.

Debe probar exhaustivamente el contenido mediante estilos visuales para determinar si la aplicación de estilos visuales tiene un efecto adverso en el contenido y el diseño.

## <a name="when-visual-styles-are-not-applied"></a>Cuando no se aplican estilos visuales

Para evitar aplicar estilos visuales a una ventana de nivel superior, dé a la ventana una región que no sea NULL (**SetWindowRgn**). El sistema supone que una ventana con una región que no es NULL es una ventana especializada que no usa estilos visuales. Una ventana secundaria asociada a una ventana de nivel superior que no sea de estilos visuales puede seguir aplicando estilos visuales aunque la ventana primaria no lo haga.

Si desea deshabilitar el uso de estilos visuales para todas las ventanas de la aplicación, llame a [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) y no pase la marca STAP \_ ALLOW \_ NONCLIENT. Si una aplicación no llama a **SetThemeAppProperties,** los valores de marca asumidos son STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT. Los valores asumidos hacen que se aplique un estilo visual al área no cliente, los controles y el contenido web.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Hacer que la aplicación sea compatible con versiones anteriores de Windows

Gran parte de la arquitectura de estilo visual está diseñada para facilitar el envío del producto en versiones anteriores de Windows que no admiten cambiar la apariencia de los controles. Al enviar una aplicación para más de un sistema operativo, tenga en cuenta lo siguiente:

-   En las versiones de Windows anteriores a Windows 8, los estilos visuales están desactivados cuando el contraste alto está on. Para admitir el contraste alto, una aplicación heredada que admite estilos visuales debe proporcionar una ruta de acceso de código independiente para dibujar correctamente los elementos de la interfaz de usuario en contraste alto. En Windows 8, el contraste alto forma parte de los estilos visuales; sin embargo, una aplicación de Windows 8 (una que incluya el GUID de Windows 8 en la sección de compatibilidad de su manifiesto de aplicación) todavía necesita proporcionar una ruta de acceso de código independiente para representarse correctamente en contraste alto en Windows 7 una vez anterior.
-   Si usa las características de ComCtl32.dll versión 6, como la vista de icono o el control de vínculo, debe controlar el caso en el que esos controles no están disponibles en el equipo del usuario. ComCtl32.dll versión 6 no es redistribuible.
-   Pruebe la aplicación para asegurarse de que no se basa en las características de ComCtl32.dll versión 6 sin comprobar primero la versión actual.
-   No vincule a UxTheme.lib.
-   Escribir código de control de errores para instancias de cuando los estilos visuales no funcionan según lo previsto.
-   La instalación del manifiesto de la aplicación en versiones anteriores no afectará a la representación de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 
