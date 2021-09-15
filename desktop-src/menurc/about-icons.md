---
title: Acerca de los iconos
description: En este tema se de abordan los iconos.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- resources,icons
- iconos, zonas de acceso
- icons,standard
- iconos estándar
- icons,custom
- iconos personalizados
- iconos, tamaños
- crear iconos
- iconos, mostrar
- iconos, destruir
- iconos, duplicación
- iconos, crear
- mostrar iconos
- destruir iconos
- duplicar iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359727"
---
# <a name="about-icons"></a>Acerca de los iconos

El sistema usa iconos en toda la interfaz de usuario para representar objetos como archivos, carpetas, accesos directos, aplicaciones y documentos. Las funciones de icono permiten a las aplicaciones crear, cargar, mostrar, organizar, animar y destruir iconos. Para obtener información sobre cómo especificar iconos para tipos de archivo, vea [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

Esta información general proporciona información sobre los temas siguientes:

-   [Icono de zona de acceso](#icon-hot-spot)
-   [Tipos de icono](#icon-types)
-   [Tamaños de icono](#icon-sizes)
    -   [Para cambiar el tamaño del icono pequeño del sistema](#to-change-the-size-of-the-system-small-icon)
    -   [Para recuperar el tamaño del icono pequeño del sistema](#to-retrieve-the-size-of-the-system-small-icon)
    -   [Para recuperar el tamaño del icono grande del sistema](#to-retrieve-the-size-of-the-system-large-icon)
    -   [Para recuperar el tamaño del icono pequeño del shell](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [Para cambiar el tamaño del icono grande](#to-change-the-size-of-the-large-icon)
    -   [Para recuperar el tamaño del icono grande del shell](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Creación de iconos](#icon-creation)
-   [Presentación del icono](#icon-display)
-   [Destrucción de iconos](#icon-destruction)
-   [Duplicación de iconos](#icon-duplication)

## <a name="icon-hot-spot"></a>Icono de zona de acceso

Uno de los píxeles de un icono se designa como el punto de acceso [rápido,](#icon-hot-spot)que es el punto al que el sistema realiza un seguimiento y reconoce como la posición del icono. La zona activa de un icono suele ser el píxel situado en el centro del icono. Si usa la [**función CreateIconIndirect para**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) crear un icono, puede especificar cualquier píxel para que sea la zona activa.

## <a name="icon-types"></a>Tipos de icono

El sistema operativo proporciona un conjunto de *iconos estándar* que están disponibles para que cualquier aplicación la use en cualquier momento. Los archivos de encabezado del Kit de desarrollo de software (SDK) contienen identificadores para los iconos estándar: los identificadores comienzan con el **prefijo IDI. \_**

Cada icono estándar tiene asociada una imagen predeterminada correspondiente. El usuario puede reemplazar la imagen predeterminada asociada con cualquier cursor estándar en cualquier momento.

*Los iconos personalizados* están diseñados para su uso en una aplicación determinada y pueden ser cualquier diseño. A continuación se muestran varios iconos personalizados.

![varios iconos personalizados](images/csicn-02.png)

## <a name="icon-sizes"></a>Tamaños de icono

El sistema usa cuatro tamaños de icono:

-   Sistema pequeño
-   Sistema grande
-   Shell pequeño
-   Shell grande

El *icono pequeño del sistema* se muestra en el título de la ventana.

### <a name="to-change-the-size-of-the-system-small-icon"></a>Para cambiar el tamaño del icono pequeño del sistema

1.  En Panel de control, haga clic **en Mostrar** y, a continuación, haga clic en **la pestaña** Apariencia.
2.  Seleccione **Botones de título** en la **lista** Elemento y, a continuación, establezca **el campo** Tamaño.

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>Para recuperar el tamaño del icono pequeño del sistema

-   Llame a [**la función GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) **con SM \_ CXSMICON** **y SM \_ CYSMICON.**

Las *aplicaciones usan* principalmente el icono grande del sistema, pero también se muestra en el cuadro de diálogo Alt+Tab. Las [**funciones CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon,**](/windows/desktop/api/Winuser/nf-winuser-drawicon) [**ExtractAssociatedIcon,**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona) [**ExtractIcon,**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona) [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)y [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) usan iconos grandes del sistema. El controlador de vídeo define el tamaño del icono grande del sistema, por lo que no se puede cambiar.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>Para recuperar el tamaño del icono grande del sistema

-   Llame [**a GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ CXICON** **y SM \_ CYICON.**

Las [**funciones CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx,**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)y [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) se pueden usar para trabajar con iconos en tamaños distintos de los grandes del sistema.

El *icono pequeño del shell* se usa en el explorador Windows y en los cuadros de diálogo comunes. Actualmente, el valor predeterminado es el tamaño pequeño del sistema.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>Para recuperar el tamaño del icono pequeño del shell

1.  Use la [función SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` para recuperar un identificador en la lista de imágenes del sistema.
2.  A continuación, [**llame a la función \_ ImageList GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obtener el tamaño del icono.

El icono grande del shell se usa en el escritorio.

### <a name="to-change-the-size-of-the-large-icon"></a>Para cambiar el tamaño del icono grande

1.  En Panel de control , haga clic **en Mostrar** y, a continuación, haga clic en **la pestaña** Apariencia.
2.  Seleccione **Icono en** la lista  Elemento y, a continuación, establezca el campo Tamaño (este tamaño se almacena en el Registro, en **HKEY \_ CURRENT USER \_ \\ Panel de control, Desktop \\ WindowMetrics \\ Shell Icon Size**). 
3.  Haga clic en **el signo Más.** y, a continuación, active **la casilla Usar iconos** grandes.

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>Para recuperar el tamaño del icono grande del shell

1.  Use la [**función SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con **SHGFI \_ SHELLICONSIZE** para recuperar un identificador en la lista de imágenes del sistema.
2.  A continuación, [**llame a la función \_ ImageList GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obtener el tamaño del icono.

El menú Inicio usa iconos pequeños de shell o iconos grandes de shell, dependiendo de si la casilla Usar **iconos** grandes está activada.

La aplicación debe proporcionar grupos de imágenes de icono en los tamaños siguientes:

-   48 x 48, color 256
-   32 x 32, 16 colores
-   16 x 16 píxeles, 16 colores

Al rellenar la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) que se va a usar para registrar la clase de ventana, establezca el miembro **hIcon** en el icono de 32x32 y el miembro **hIconSm** en el icono de 16x16. Para obtener más información sobre los iconos de clase, vea [Iconos de clase](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Creación de iconos

Los iconos estándar están predefinidos, por lo que no es necesario crearlos. Para usar un icono estándar, una aplicación puede obtener su identificador mediante la [**función LoadImage.**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) Un *identificador de* icono es un valor único del tipo **HICON** que identifica un icono estándar o personalizado.

Para crear un icono personalizado para una aplicación, normalmente usaría una aplicación de gráficos e incluiría el recurso [ICON](./icon-resource.md) en el archivo de definición de recursos de la aplicación. En tiempo de ejecución, puede llamar a [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) para recuperar un identificador en el icono. Un recurso de icono puede contener un grupo de imágenes para varios dispositivos de visualización diferentes. **LoadIcon** **y LoadImage** seleccionan automáticamente el icono más adecuado del grupo para el dispositivo de visualización actual.

Una aplicación también puede crear un icono personalizado en tiempo de ejecución mediante la función [**CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) que crea un icono basado en el contenido de una [**estructura ICONINFO.**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) La [**función GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) rellena la estructura con las coordenadas de punto de acceso y la información sobre el mapa de bits de máscara de bits y el mapa de bits de color del icono.

Las aplicaciones deben implementar iconos personalizados como recursos y deben usar [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) [**o LoadImage,**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)en lugar de crear el icono en tiempo de ejecución. El uso de recursos de icono evita la dependencia del dispositivo, simplifica la localización y permite que las aplicaciones compartan formas de icono.

La [**función CreateIconFromResourceEx permite**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) a una aplicación examinar los recursos del sistema y crear iconos y cursores basados en datos de recursos. **CreateIconFromResourceEx crea** un icono basado en datos de recursos binarios de otros archivos ejecutables o DLL. Una aplicación debe preceder a esta función con llamadas a [**la función LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) y a varias de las funciones de recurso. **LookupIconIdFromDirectoryEx** devuelve el identificador de los datos de icono más adecuados para el dispositivo de visualización actual.

## <a name="icon-display"></a>Presentación del icono

Puede recuperar la imagen de un icono mediante la función [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) y dibujarla mediante la [**función DrawIconEx.**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) Para dibujar la imagen predeterminada de un icono, especifique la marca **\_ DI COMPAT** en la llamada a **DrawIconEx.** Si no especifica la marca **\_ COMPAT de DI,** **DrawIconEx** dibuja el icono con la imagen especificada por el usuario.

Cuando el sistema muestra un icono, debe extraer la imagen de icono adecuada del .exe o .dll archivo. El sistema usa los pasos siguientes para seleccionar la imagen de icono:

1.  Seleccione el **recurso ICONO DE GRUPO \_ \_ RT.** Si existe más de uno de estos recursos, el sistema usa el primer recurso enumerado en el scrip de recursos.
2.  Seleccione la imagen **RT \_ ICON adecuada** en el recurso RT GROUP **\_ \_ ICON.** Si existe más de una imagen, el sistema usa los criterios siguientes para elegir una imagen:
    -   -   Se elige la imagen más cercana al tamaño solicitado.
        -   Si hay dos o más imágenes de ese tamaño, se elige la que coincide con la profundidad de color de la pantalla.
        -   Si ninguna imagen coincide exactamente con la profundidad de color de la pantalla, se elige la imagen con la mayor profundidad de color que no supere la profundidad de color de la pantalla. Si todas superan la profundidad de color, se elige la que tiene la profundidad de color más baja.

> [!Note]  
> El sistema trata todas las profundidades de color de 8 o más bpp como iguales. Por lo tanto, no hay ninguna ventaja de incluir una imagen de 16x16 de 256 colores y una imagen de 16x16 de 16 colores en el mismo recurso: el sistema simplemente elegirá la primera que encuentre. Cuando la pantalla está en modo 8 bpp, el sistema elegirá un icono de 16 colores sobre un icono de 256 colores y mostrará todos los iconos mediante la paleta predeterminada del sistema.

 

Para mostrar un icono animado, use un control estático como se muestra en el fragmento de código siguiente.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Destrucción de iconos

Cuando una aplicación ya no necesita un icono que creó mediante la [**función CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) debe destruir el icono. La [**función DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destruye el identificador del icono y libera la memoria que usa el icono. Las aplicaciones solo deben usar esta función para los iconos creados **con CreateIconIndirect**; no es necesario destruir otros iconos.

## <a name="icon-duplication"></a>Duplicación de iconos

La [**función CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) copia un identificador de icono. Esto permite que una aplicación o dll obtenga su propio identificador a un icono propiedad de otro módulo. A continuación, si se libera el otro módulo, la aplicación que copió el icono podrá seguir utilizando el icono.

La [**función CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) crea un nuevo icono basado en el icono de origen especificado. El nuevo icono puede ser mayor o menor que el icono de origen.

Para obtener información sobre cómo agregar, quitar o reemplazar recursos de icono en archivos ejecutables (.exe), vea [Recursos](resources.md).

La [**función DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) realiza una copia real del icono.

 

 