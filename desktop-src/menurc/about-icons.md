---
title: Acerca de los iconos
description: En este tema se describen los iconos.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- recursos, iconos
- iconos, zonas activas
- iconos, estándar
- iconos estándar
- iconos, personalizado
- iconos personalizados
- iconos, tamaños
- crear iconos
- iconos, Mostrar
- iconos, destruir
- iconos, duplicación
- iconos, crear
- mostrar iconos
- destruir iconos
- duplicar iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358930"
---
# <a name="about-icons"></a>Acerca de los iconos

El sistema utiliza iconos en la interfaz de usuario para representar objetos como archivos, carpetas, accesos directos, aplicaciones y documentos. Las funciones de icono permiten a las aplicaciones crear, cargar, mostrar, organizar, animar y destruir iconos. Para obtener información sobre cómo especificar iconos para tipos de archivo, vea [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

En esta información general se proporciona información sobre los temas siguientes:

-   [Icono de zona activa](#icon-hot-spot)
-   [Tipos de icono](#icon-types)
-   [Tamaños de icono](#icon-sizes)
    -   [Para cambiar el tamaño del icono pequeño del sistema](#to-change-the-size-of-the-system-small-icon)
    -   [Para recuperar el tamaño del icono pequeño del sistema](#to-retrieve-the-size-of-the-system-small-icon)
    -   [Para recuperar el tamaño del icono grande del sistema](#to-retrieve-the-size-of-the-system-large-icon)
    -   [Para recuperar el tamaño del icono pequeño de Shell](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [Para cambiar el tamaño del icono grande](#to-change-the-size-of-the-large-icon)
    -   [Para recuperar el tamaño del icono de Shell grande](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Creación de iconos](#icon-creation)
-   [Visualización de iconos](#icon-display)
-   [Destrucción de iconos](#icon-destruction)
-   [Duplicación de iconos](#icon-duplication)

## <a name="icon-hot-spot"></a>Icono de zona activa

Uno de los píxeles de un icono se designa como la [zona activa](#icon-hot-spot), que es el punto en el que el sistema realiza un seguimiento y lo reconoce como la posición del icono. La zona activa de un icono suele ser el píxel situado en el centro del icono. Si usa la función [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) para crear un icono, puede especificar que cualquier píxel sea la zona activa.

## <a name="icon-types"></a>Tipos de icono

El sistema operativo proporciona un conjunto de *iconos estándar* que se pueden usar en cualquier aplicación en cualquier momento. Los archivos de encabezado del kit de desarrollo de software (SDK) contienen identificadores para los iconos estándar: los identificadores comienzan por el prefijo **IDI \_** .

Cada icono estándar tiene asociada una imagen predeterminada correspondiente. El usuario puede reemplazar la imagen predeterminada asociada con cualquier cursor estándar en cualquier momento.

Los *iconos personalizados* están diseñados para su uso en una aplicación determinada y pueden ser cualquier diseño. A continuación se muestran varios iconos personalizados.

![varios iconos personalizados](images/csicn-02.png)

## <a name="icon-sizes"></a>Tamaños de icono

El sistema utiliza cuatro tamaños de icono:

-   Sistema pequeño
-   Gran sistema
-   Shell pequeño
-   Shell grande

El *icono pequeño del sistema* se muestra en el título de la ventana.

### <a name="to-change-the-size-of-the-system-small-icon"></a>Para cambiar el tamaño del icono pequeño del sistema

1.  En el panel de control, haga clic en **pantalla** y, a continuación, en la ficha **apariencia** .
2.  Seleccione los **botones de título** de la lista de **elementos** y, a continuación, establezca el campo **tamaño** .

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>Para recuperar el tamaño del icono pequeño del sistema

-   Llame a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ CXSMICON** y **SM \_ CYSMICON**.

Las aplicaciones usan principalmente el *icono grande del sistema* , pero también se muestra en el cuadro de diálogo Alt + Tab. Las funciones [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona), [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona), [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)y [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) usan iconos grandes del sistema. El controlador de vídeo define el tamaño del icono grande del sistema, por lo que no se puede cambiar.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>Para recuperar el tamaño del icono grande del sistema

-   Llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ CXICON** y **SM \_ CYICON**.

Las funciones [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)y [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) se pueden usar para trabajar con iconos en tamaños distintos de System Large.

El *icono pequeño de Shell* se usa en el explorador de Windows y en los cuadros de diálogo comunes. Actualmente, este valor predeterminado es el tamaño pequeño del sistema.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>Para recuperar el tamaño del icono pequeño de Shell

1.  Utilice la función [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` para recuperar un identificador de la lista de imágenes del sistema.
2.  Después, llame a la función [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obtener el tamaño del icono.

El icono de Shell grande se usa en el escritorio.

### <a name="to-change-the-size-of-the-large-icon"></a>Para cambiar el tamaño del icono grande

1.  En el panel de control, haga clic en **pantalla** y, a continuación, en la ficha **apariencia** .
2.  Seleccione **icono** en la lista de **elementos** y, a continuación, establezca el campo **tamaño** (este tamaño se almacena en el registro, en **HKEY \_ Current \_ User \\ control panel, Desktop \\ WindowMetrics \\ Shell Icon size**).
3.  Haga clic en **Plus!** y, a continuación, active la casilla **usar iconos grandes** .

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>Para recuperar el tamaño del icono de Shell grande

1.  Use la función [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con **SHGFI \_ SHELLICONSIZE** para recuperar un identificador de la lista de imágenes del sistema.
2.  Después, llame a la función [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obtener el tamaño del icono.

El menú Inicio usa iconos pequeños de shell o iconos grandes de Shell, dependiendo de si la casilla **usar iconos grandes** está activada.

La aplicación debe proporcionar grupos de imágenes de iconos en los tamaños siguientes:

-   48x48, color 256
-   32x32, 16 colores
-   16x16 píxeles, 16 colores

Al rellenar la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) que se va a usar para registrar la clase de ventana, establezca el miembro **hIcon** en el icono 32X32 y el miembro **hIconSm** en el icono 16x16. Para obtener más información sobre los iconos de clase, vea [iconos de clase](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Creación de iconos

Los iconos estándar están predefinidos, por lo que no es necesario crearlos. Para usar un icono estándar, una aplicación puede obtener su identificador mediante la función [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *identificador de icono* es un valor único del tipo **HICON** que identifica un icono estándar o personalizado.

Para crear un icono personalizado para una aplicación, normalmente usaría una aplicación de gráficos e incluiría el [recurso de icono](./icon-resource.md) en el archivo de definición de recursos de la aplicación. En tiempo de ejecución, puede llamar a [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) para recuperar un identificador del icono. Un recurso de icono puede contener un grupo de imágenes para varios dispositivos de pantalla diferentes. **LoadIcon** y **LoadImage** seleccionan automáticamente el icono más apropiado del grupo para el dispositivo de pantalla actual.

Una aplicación también puede crear un icono personalizado en tiempo de ejecución mediante la función [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , que crea un icono basado en el contenido de una estructura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La función [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) llena la estructura con las coordenadas de la zona activa e información sobre el mapa de bits de la máscara de bits y el mapa de bits de color para el icono.

Las aplicaciones deben implementar iconos personalizados como recursos y deben usar [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea), en lugar de crear el icono en tiempo de ejecución. El uso de recursos de icono evita la dependencia del dispositivo, simplifica la localización y permite que las aplicaciones compartan formas de icono.

La función [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permite a una aplicación examinar los recursos del sistema y crear iconos y cursores basados en los datos de recursos. **CreateIconFromResourceEx** crea un icono basado en datos de recursos binarios de otros archivos ejecutables o dll. Una aplicación debe preceder a esta función con llamadas a la función [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) y a varias de las funciones de recursos. **LookupIconIdFromDirectoryEx** devuelve el identificador de los datos de icono más adecuados para el dispositivo de pantalla actual.

## <a name="icon-display"></a>Visualización de iconos

Puede recuperar la imagen de un icono mediante la función [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) y puede dibujarla mediante la función [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Para dibujar la imagen predeterminada de un icono, especifique la marca de la **\_ compatibilidad con di** en la llamada a **DrawIconEx**. Si no especifica la marca de **la \_ compatibilidad con di** , **DrawIconEx** dibuja el icono con la imagen especificada por el usuario.

Cuando el sistema muestra un icono, debe extraer la imagen de icono correspondiente del archivo. exe o. dll. El sistema usa los pasos siguientes para seleccionar la imagen de icono:

1.  Seleccione el **recurso \_ \_ icono de grupo RT** . Si existe más de un recurso de este tipo, el sistema usa el primer recurso que aparece en el scripts de recursos.
2.  Seleccione la imagen **de \_ icono RT** adecuada en el recurso **\_ \_ icono de grupo RT** . Si existe más de una imagen, el sistema usa los siguientes criterios para elegir una imagen:
    -   -   Se elige la imagen más cercana al tamaño solicitado.
        -   Si hay dos o más imágenes de ese tamaño, se elige la que coincida con la profundidad de color de la pantalla.
        -   Si ninguna imagen coincide exactamente con la profundidad de color de la pantalla, se elige la imagen con la mayor profundidad de color que no supere la profundidad de color de la pantalla. Si todo supera la profundidad de color, se elige la que tenga la menor profundidad de color.

> [!Note]  
> El sistema trata todas las profundidades de color de 8 o más BPP como iguales. Por lo tanto, no hay ninguna ventaja de incluir una imagen de color 16x16 256 y una imagen de 16 colores de 16x16 en el mismo recurso; el sistema simplemente elegirá el primero que encuentra. Cuando la pantalla está en modo 8-BPP, el sistema elegirá un icono de 16 colores sobre un icono de color 256 y mostrará todos los iconos mediante la paleta predeterminada del sistema.

 

Para mostrar un Icono animado, use un control estático tal y como se muestra en el siguiente fragmento de código.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Destrucción de iconos

Cuando una aplicación ya no necesita un icono que creó mediante la función [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , debe destruir el icono. La función [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destruye el identificador del icono y libera cualquier memoria utilizada por el icono. Las aplicaciones deben usar esta función solo para los iconos creados con **CreateIconIndirect**; no es necesario destruir otros iconos.

## <a name="icon-duplication"></a>Duplicación de iconos

La función [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) copia un identificador de icono. Esto permite a una aplicación o DLL obtener su propio identificador de un icono que pertenece a otro módulo. Después, si se libera el otro módulo, la aplicación que copió el icono seguirá pudiendo usar el icono.

La función [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) crea un nuevo icono basado en el icono de origen especificado. El nuevo icono puede ser mayor o menor que el icono de origen.

Para obtener información sobre cómo agregar, quitar o reemplazar recursos de iconos en archivos ejecutables (. exe), vea [recursos](resources.md).

La función [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) crea una copia real del icono.

 

 