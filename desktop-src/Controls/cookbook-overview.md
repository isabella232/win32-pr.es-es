---
title: Habilitar los estilos visuales
description: En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995694"
---
# <a name="enabling-visual-styles"></a>Habilitar los estilos visuales

En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.

En este tema se incluyen las secciones siguientes.

-   [Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Usar la versión 6 de ComCtl32 en el panel de control o un archivo DLL ejecutado por RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Agregar compatibilidad con el estilo visual a una extensión, complemento, complemento MMC o archivo DLL que se incorpora a un proceso](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Desactivación de los estilos visuales](#turning-off-visual-styles)
-   [Usar estilos visuales con contenido HTML](#using-visual-styles-with-html-content)
-   [Cuando no se aplican estilos visuales](#when-visual-styles-are-not-applied)
-   [Conseguir que la aplicación sea compatible con versiones anteriores de Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Temas relacionados](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones

Para permitir que la aplicación use estilos visuales, debe usar ComCtl32.dll versión 6 o posterior. Dado que la versión 6 no es redistribuible, solo está disponible cuando la aplicación se ejecuta en una versión de Windows que la contiene. Windows se incluye con las versiones 5 y 6. ComCtl32.dll versión 6 contiene los controles de usuario y los controles comunes. De forma predeterminada, las aplicaciones usan los controles de usuario definidos en User32.dll y los controles comunes definidos en ComCtl32.dll versión 5. Para obtener una lista de las versiones de DLL y sus plataformas de distribución, vea [versiones de control comunes](common-control-versions.md).

Si desea que la aplicación use estilos visuales, debe agregar un manifiesto de aplicación o una directiva de compilador que indique que se debe usar ComCtl32.dll versión 6 Si está disponible.

Un manifiesto de aplicación permite a una aplicación especificar qué versiones de un ensamblado requiere. En Microsoft Win32, un ensamblado es un conjunto de archivos dll y una lista de objetos con versión que están incluidos en esos archivos dll.

Los manifiestos se escriben en XML. El nombre del archivo de manifiesto de aplicación es el nombre del ejecutable seguido de la extensión de nombre de archivo. manifest; por ejemplo, MyApp.exe. manifest. En el siguiente manifiesto de ejemplo se muestra que la primera sección describe el manifiesto. En la tabla siguiente se muestran los atributos establecidos por el elemento **assemblyIdentity** en la sección de Descripción del manifiesto.



| Atributo             | Descripción                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versión del manifiesto. La versión debe tener el formato principal. secundaria. revisión. compilación (es decir, n. n. n, donde n <= 65535). |
| processorArchitecture | Procesador para el que se desarrolla la aplicación.                                                                          |
| name                  | Incluye el nombre de la compañía, el nombre del producto y el nombre de la aplicación.                                                                   |
| type                  | Tipo de la aplicación, como Win32.                                                                                    |



 

El manifiesto de ejemplo también proporciona una descripción de la aplicación y especifica las dependencias de la aplicación. En la tabla siguiente se muestran los atributos establecidos por el elemento **assemblyIdentity** en la sección de dependencia.



| Atributo             | Descripción                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo del componente de dependencia, como Win32. |
| name                  | Nombre del componente.                           |
| version               | Versión del componente.                        |
| processorArchitecture | Procesador para el que está diseñado el componente.    |
| publicKeyToken        | Token de clave usado con este componente.              |
| language              | Lenguaje del componente.                       |



 

A continuación se encuentra un ejemplo de un archivo de manifiesto.

> [!IMPORTANT]
> Establezca la entrada de **processorArchitecture** en **"x86"** si su aplicación tiene como destino la plataforma de Windows de 32 bits o en **"AMD64"** si su aplicación tiene como destino la plataforma de Windows de 64 bits. También puede especificar **" \* "**, lo que garantiza que todas las plataformas están destinadas, tal y como se muestra en los ejemplos siguientes.

 


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



Si usa Microsoft Visual C++ 2005 o una versión posterior, puede Agregar la siguiente directiva de compilador al código fuente en lugar de crear manualmente un manifiesto. Para mejorar la legibilidad, la Directiva se divide aquí en varias líneas.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



En los temas siguientes se describen los pasos para aplicar estilos visuales a diferentes tipos de aplicaciones. Observe que el formato del manifiesto es el mismo en cada caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar

A continuación se muestran ejemplos de aplicaciones que no usan extensiones de terceros.

-   Calculadora
-   Carta blanca
-   Buscaminas
-   Bloc de notas
-   Solitario

**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**

1.  Vincular a ComCtl32. lib y llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Agregue un archivo llamado YourApp.exe. manifest al árbol de origen que tiene el formato de manifiesto XML.
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

    

3.  Agregue el manifiesto al archivo de recursos de la aplicación de la siguiente manera:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Al agregar la entrada anterior al recurso, debe darle formato en una línea. Como alternativa, puede colocar el archivo de manifiesto XML en el mismo directorio que el archivo ejecutable de la aplicación. El sistema operativo cargará primero el manifiesto del sistema de archivos y, a continuación, comprobará la sección de recursos del archivo ejecutable. La versión del sistema de archivos tiene prioridad.

     

Al compilar la aplicación, el manifiesto se agregará como un recurso binario.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Usar la versión 6 de ComCtl32 en el panel de control o un archivo DLL ejecutado por RunDll32.exe

**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**

1.  Vincular a ComCtl32. lib y llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Agregue un archivo llamado YourApp.cpl. manifest al árbol de origen que tiene el formato de manifiesto XML.
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

    

3.  Agregue el manifiesto al archivo de recursos de la aplicación como identificador de recurso 123.

> [!Note]  
> Cuando cree una aplicación del panel de control, colóquela en la categoría correspondiente. El panel de control admite ahora la categorización de aplicaciones del panel de control. Esto significa que las aplicaciones del panel de control pueden tener identificadores y separarse en áreas de tareas como agregar o quitar programas, apariencia y temas, o fecha, hora, idioma y opciones regionales.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Agregar compatibilidad con el estilo visual a una extensión, complemento, complemento MMC o archivo DLL que se incorpora a un proceso

Se puede Agregar compatibilidad con estilos visuales a una extensión, complemento, complemento MMC o a un archivo DLL que se incluye en un proceso. Por ejemplo, use los pasos siguientes para agregar compatibilidad con estilos visuales para un complemento de Microsoft Management Console (MMC).

1.  Compile el complemento con la marca-DISOLATION \_ compatible \_ habilitada o inserte la siguiente instrucción antes de la \# instrucción include "Windows. h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Para obtener más información sobre el reconocimiento de aislamiento \_ \_ habilitado, vea [aislar componentes](/windows/desktop/SbsCs/isolating-components).

2.  Incluya el archivo de encabezado de control común en el origen del complemento.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Agregue un archivo denominado sufiles. manifest al árbol de origen que utiliza el formato de manifiesto XML.
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

    

4.  Agregue el manifiesto al archivo de recursos del complemento. Vea [usar la versión 6 de comctl32 en una aplicación que usa extensiones, complementos o un archivo DLL que se incluye en un proceso](/previous-versions//ms649781(v=vs.85)) para obtener más información sobre cómo agregar un manifiesto a un archivo de recursos.

## <a name="turning-off-visual-styles"></a>Desactivación de los estilos visuales

Puede desactivar los estilos visuales para un control o para todos los controles de una ventana mediante una llamada a la función [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) como se indica a continuación:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



En el ejemplo anterior, *hWnd* es el identificador de la ventana en la que se deshabilitan los estilos visuales. Después de la llamada, el control se representa sin estilos visuales.

## <a name="using-visual-styles-with-html-content"></a>Usar estilos visuales con contenido HTML

En las páginas HTML que modifican las propiedades de Hojas de estilo CSS (CSS), como fondo o borde, no se les aplican estilos visuales. Muestran el atributo CSS especificado. Cuando se especifica como parte del contenido, la mayoría de las propiedades de CSS se aplican a los elementos que tienen estilos visuales aplicados.

De forma predeterminada, los estilos visuales se aplican a los controles HTML intrínsecos en las páginas que se muestran en Microsoft Internet Explorer 6 y versiones posteriores. Para desactivar los estilos visuales de una página HTML, agregue una etiqueta META al <head> . Esta técnica también se aplica al contenido empaquetado como aplicaciones HTML (HTA). Para desactivar los estilos visuales, la etiqueta META debe ser como se indica a continuación:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Si el valor del explorador y la configuración de la etiqueta no coinciden, la página no aplicará los estilos visuales. Por ejemplo, si la etiqueta META está establecida en "no" y el explorador está establecido para habilitar estilos visuales, los estilos visuales no se aplicarán a la página. Sin embargo, si el explorador o la etiqueta META está establecida en "sí" y no se especifica el otro elemento, se aplicarán los estilos visuales.

 

Los estilos visuales pueden cambiar el diseño del contenido. Además, si establece ciertos atributos en controles HTML intrínsecos, como el ancho de un botón, es posible que la etiqueta del botón sea ilegible en determinados estilos visuales.

Debe probar exhaustivamente el contenido mediante estilos visuales para determinar si la aplicación de estilos visuales tiene un efecto adverso en el contenido y el diseño.

## <a name="when-visual-styles-are-not-applied"></a>Cuando no se aplican estilos visuales

Para evitar la aplicación de estilos visuales en una ventana de nivel superior, asigne a la ventana una región que no sea NULL (**SetWindowRgn**). El sistema supone que una ventana con una región que no es NULL es una ventana especializada que no usa estilos visuales. Una ventana secundaria asociada a una ventana de nivel superior que no sea de estilos visuales puede seguir aplicando estilos visuales aunque la ventana primaria no lo sea.

Si desea deshabilitar el uso de estilos visuales para todas las ventanas de la aplicación, llame a [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) y no pase la \_ marca STAP allow \_ nonclient. Si una aplicación no llama a **SetThemeAppProperties**, los valores de marca asumidos son STAP permitir que los controles STAP no sean de \_ \_ cliente \| \_ \_ \| STAP \_ permitir el contenido de \_ WebContent. Los valores asumidos hacen que el área no cliente, los controles y el contenido web tengan aplicado un estilo visual.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Conseguir que la aplicación sea compatible con versiones anteriores de Windows

Gran parte de la arquitectura de estilo visual está diseñada para simplificar la entrega del producto en versiones anteriores de Windows que no admiten el cambio de la apariencia de los controles. Al enviar una aplicación para más de un sistema operativo, tenga en cuenta lo siguiente:

-   En las versiones de Windows anteriores a Windows 8, los estilos visuales se desactivan cuando el contraste alto está activado. Para admitir el contraste alto, una aplicación heredada que admite estilos visuales debe proporcionar una ruta de acceso de código independiente para dibujar correctamente los elementos de la interfaz de usuario en contraste alto. En Windows 8, el contraste alto forma parte de los estilos visuales; sin embargo, una aplicación de Windows 8 (una que incluye el GUID de Windows 8 en la sección de compatibilidad de su manifiesto de aplicación) todavía debe proporcionar una ruta de acceso de código independiente para representar correctamente en contraste alto en Windows 7.
-   Si usa las características de ComCtl32.dll versión 6, como la vista en mosaico o el control de vínculo, debe controlar el caso en el que los controles no están disponibles en el equipo del usuario. ComCtl32.dll versión 6 no es redistribuible.
-   Pruebe la aplicación para asegurarse de que no se basa en las características de ComCtl32.dll versión 6 sin comprobar primero la versión actual.
-   No vincule a UxTheme. lib.
-   Escriba el código de control de errores para las instancias cuando los estilos visuales no funcionen según lo esperado.
-   La instalación del manifiesto de la aplicación en versiones anteriores no afectará a la representación de los controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 