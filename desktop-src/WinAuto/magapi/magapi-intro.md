---
title: Introducción a la API de ampliación
description: En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Aumento
- aplicaciones de ampliación de pantalla
- Aumento
- procesamiento de imágenes personalizadas
- Magnification.dll
- crear controles del ampliador
- Ampliación selectiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720156"
---
# <a name="magnification-api-overview"></a>Introducción a la API de ampliación

La API de ampliación permite a los proveedores de tecnología de asistencia desarrollar aplicaciones de ampliación de pantalla que se ejecutan en Microsoft Windows. En este tema se describe la API de ampliación y se explica cómo utilizarla en una aplicación. Contiene las secciones siguientes:

- [Introducción](#getting-started)
- [Conceptos básicos](#basic-concepts)
  - [Tipos de ampliadores](#types-of-magnifiers)
  - [Factor de ampliación](#magnification-factor)
  - [Efectos de color](#color-effects)
  - [Rectángulo de origen](#source-rectangle)
  - [Lista de filtros](#filter-list)
  - [Transformación de entrada](#input-transform)
  - [Cursor del sistema](#system-cursor)
- [Inicializar la biblioteca en tiempo de ejecución del ampliador](#initializing-the-magnifier-run-time-library)
- [Uso del ampliador de Full-Screen](#using-the-full-screen-magnifier)
- [Usar el control Magnifier](#using-the-magnifier-control)
  - [Crear el control ampliador](#creating-the-magnifier-control)
  - [Inicializar el control](#initializing-the-control)
  - [Establecer el rectángulo de origen](#setting-the-source-rectangle)
  - [Aplicar efectos de color](#applying-color-effects)
  - [Ampliación selectiva](#selective-magnification)
- [Temas relacionados](#related-topics)

## <a name="getting-started"></a>Introducción

La versión original de la API de ampliación es compatible con Windows Vista y sistemas operativos posteriores. En Windows 8 y versiones posteriores, la API admite características adicionales, incluida la ampliación a pantalla completa y el establecimiento de la visibilidad del cursor del sistema ampliado.

Magnification.dll proporciona compatibilidad con la API de ampliación. Para compilar la aplicación, incluya proprof. h y vincule a Amplification. lib.

> [!Note]  
> La API de ampliación no se admite en WOW64; es decir, una aplicación del ampliador de 32 bits no se ejecutará correctamente en Windows de 64 bits.

## <a name="basic-concepts"></a>Conceptos básicos

En esta sección se describen los conceptos fundamentales en los que se basa la API de ampliación. Contiene las siguientes partes:

- [Tipos de ampliadores](#types-of-magnifiers)
- [Factor de ampliación](#magnification-factor)
- [Efectos de color](#color-effects)
- [Rectángulo de origen](#source-rectangle)
- [Lista de filtros](#filter-list)
- [Transformación de entrada](#input-transform)
- [Cursor del sistema](#system-cursor)

### <a name="types-of-magnifiers"></a>Tipos de ampliadores

La API admite dos tipos de ampliadores, el *ampliador de pantalla completa* y el *control ampliador*. El ampliador de pantalla completa amplía el contenido de toda la pantalla, mientras que el control ampliador amplía el contenido de un área determinada de la pantalla y muestra el contenido en una ventana. En el caso de los ampliadores, las imágenes y el texto se amplían y ambos le permiten controlar la cantidad de ampliación. También puede aplicar efectos de color al contenido de la pantalla ampliada, lo que facilita la visualización de las personas que tienen deficiencias de color o necesitan colores con mayor o menor contraste.

> [!Important]  
> La API del control Magnifier está disponible en Windows Vista y sistemas operativos posteriores, mientras que la API del ampliador de pantalla completa solo está disponible en los sistemas operativos Windows 8 y versiones posteriores.

### <a name="magnification-factor"></a>Factor de ampliación

Tanto el ampliador de pantalla completa como el control ampliador aplican una transformación de escala al contenido de la pantalla. La cantidad de ampliación aplicada por la transformación de escala se denomina *factor de ampliación*. Se expresa como un valor de punto flotante, en el que 1,0 corresponde a ninguna ampliación y los valores más grandes dan como resultado una cantidad de ampliación correspondiente. Por ejemplo, un valor de 1,5 hace que el contenido de la pantalla sea 50 por ciento más grande. Un factor de ampliación inferior a 1,0 no es válido.

### <a name="color-effects"></a>Efectos de color

Los efectos de color se logran aplicando una matriz de transformación de color 5 por 5 a los colores del contenido de la pantalla ampliada. La matriz determina las intensidades de los componentes rojo, azul, verde y alfa del contenido. Para obtener más información, vea [usar una matriz de colores para transformar un solo color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) en la documentación de Windows GDI+.

### <a name="source-rectangle"></a>Rectángulo de origen

El ampliador de pantalla completa aplica la transformación de escala y la transformación de color a toda la pantalla. Por otro lado, el control ampliador copia un área de la pantalla, denominada *rectángulo de origen*, en un mapa de bits fuera de la pantalla. Después, el control aplica la transformación de escala y la transformación de color, si existe, al mapa de bits fuera de la pantalla. Por último, el control muestra el mapa de bits escalado y transformado por colores en la ventana de control del ampliador.

### <a name="filter-list"></a>Lista de filtros

De forma predeterminada, el control Magnifier amplía todas las ventanas del rectángulo de origen especificado. Sin embargo, al proporcionar una *lista de filtros* de identificadores de ventana, puede controlar qué ventanas se incluyen en el contenido ampliado y cuáles no. Para obtener más información, vea el apartado sobre el [aumento selectivo](#selective-magnification).

El ampliador de pantalla completa no es compatible con una lista de filtros; siempre amplía todas las ventanas de la pantalla.

### <a name="input-transform"></a>Transformación de entrada

Normalmente, el contenido de la pantalla ampliada es "invisible" para el lápiz de usuario o la entrada táctil. Por ejemplo, si el usuario pulsa la imagen ampliada de un control, el sistema no pasa necesariamente la entrada al control. En su lugar, el sistema pasa la entrada a cualquier elemento (si existe) que se encuentra en las coordenadas de la pantalla punteada en el escritorio sin ampliar. La función [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) permite especificar una transformación de *entrada* que asigna el espacio de coordenadas del contenido de la pantalla ampliada al espacio de coordenadas de pantalla real (no ampliado). Esto permite al sistema pasar la entrada táctil o manuscrita que se escribe en el contenido de la pantalla ampliada, al elemento de la interfaz de usuario correcto en la pantalla.

> [!Note]  
> El proceso de llamada debe tener privilegios UIAccess para establecer la transformación de entrada. Para obtener más información, vea [consideraciones de seguridad de UI Automation](../uiauto-securityoverview.md) y [/manifestuac (insertar información de UAC en el manifiesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

### <a name="system-cursor"></a>Cursor del sistema

La función [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) permite mostrar u ocultar el cursor del sistema. Si se muestra el cursor del sistema cuando el ampliador de pantalla completa está activo, el cursor del sistema siempre se amplía junto con el resto del contenido de la pantalla. Si oculta el cursor del sistema cuando el ampliador de pantalla completa está activo, el cursor del sistema no es visible en absoluto.

Con el control Magnifier, la función [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) muestra u oculta el cursor del sistema no ampliado, pero no tiene ningún efecto en el cursor del sistema ampliado. La visibilidad del cursor del sistema ampliado depende de si el control de la lupa tiene el estilo [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) . Si tiene este estilo, el control ampliador muestra el cursor del sistema ampliado, junto con el contenido de la pantalla ampliada, siempre que el cursor del sistema entre en el rectángulo de origen.

## <a name="initializing-the-magnifier-run-time-library"></a>Inicializar la biblioteca en tiempo de ejecución del ampliador

Antes de poder llamar a cualquier otra función de API del ampliador, debe crear e inicializar los objetos de tiempo de ejecución del ampliador mediante una llamada a la función [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) . Del mismo modo, después de terminar de usar la API del ampliador, llame a la función [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) para destruir los objetos de tiempo de ejecución del ampliador y liberar los recursos del sistema asociados.

## <a name="using-the-full-screen-magnifier"></a>Uso del ampliador de Full-Screen

Para usar el ampliador de pantalla completa, llame a la función [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) . El parámetro *magLevel* especifica el factor de ampliación. Los parámetros *xoffset* y *YOFFSET* especifican cómo se coloca el contenido de la pantalla ampliada en relación con la pantalla.

Cuando se amplía el contenido de la pantalla, se vuelve más grande que la propia pantalla. Parte del contenido se extiende más allá de los bordes de la pantalla y se convierte en invisible para el usuario. Los parámetros *xoffset* y *YOFFSET* de la función [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinan qué parte del contenido de la pantalla ampliada aparece en la pantalla. Juntos, los parámetros especifican las coordenadas de un punto en el contenido de pantalla no ampliada. Cuando se amplía el contenido, se coloca con el punto especificado en la esquina superior izquierda de la pantalla.

En el ejemplo siguiente se establece el factor de ampliación para el ampliador de pantalla completa y se coloca el centro del contenido de la pantalla ampliada en el centro de la pantalla.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Utilice la función [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) para aplicar efectos de color al contenido de pantalla completa mediante el establecimiento de una matriz de transformación de color definida por la aplicación. Por ejemplo, en el ejemplo siguiente se establece una matriz de transformación de color que convierte los colores a escala de grises.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

Puede recuperar el factor de ampliación actual y los valores de desplazamiento mediante una llamada a la función [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) . Puede recuperar la matriz de transformación de color actual llamando a la función [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .

## <a name="using-the-magnifier-control"></a>Usar el control Magnifier

El control ampliador amplía el contenido de un área determinada de la pantalla y muestra el contenido en una ventana. En esta sección se describe cómo usar el control ampliador. Contiene las siguientes partes:

- [Crear el control ampliador](#creating-the-magnifier-control)
- [Inicializar el control](#initializing-the-control)
- [Establecer el rectángulo de origen](#setting-the-source-rectangle)
- [Aplicar efectos de color](#applying-color-effects)
- [Ampliación selectiva](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Crear el control ampliador

El control ampliador debe estar hospedado en una ventana creada con el estilo extendido [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) . Después de crear la ventana host, llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) para establecer la opacidad de la ventana host. La ventana host normalmente se establece en opacidad completa para evitar que se muestre el contenido de la pantalla subyacente. En el ejemplo siguiente se muestra cómo establecer la ventana host en la opacidad completa:

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Si aplica el estilo [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) a la ventana host, los clics del mouse se pasan a cualquier objeto situado detrás de la ventana host en la ubicación del cursor del mouse. Tenga en cuenta que, dado que la ventana host no procesa los clics del mouse, el usuario no podrá moverse ni cambiar el tamaño de la ventana de ampliación mediante el mouse.

La clase de ventana de la ventana de control del ampliador debe estar **WC_MAGNIFIER**. Si aplica el estilo [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , el control ampliador incluye el cursor del sistema en el contenido de la pantalla ampliada y el cursor se amplía junto con el contenido de la pantalla.

Después de crear el control ampliador, mantenga el identificador de ventana para que pueda pasarlo a otras funciones.

En el ejemplo siguiente se muestra cómo crear el control ampliador.

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Inicializar el control

Después de crear el control Magnifier, debe llamar a la función [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) para especificar el factor de ampliación. Esto es simplemente una cuestión de especificar una matriz de

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

donde *n* es el factor de ampliación.

En el ejemplo siguiente se muestra cómo establecer el factor de ampliación para el control ampliador.

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Establecer el rectángulo de origen

A medida que el usuario mueve el cursor del mouse alrededor de la pantalla, la aplicación llama a la función [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) para especificar la parte de la pantalla subyacente que se va a ampliar.

La función de ejemplo siguiente calcula la posición y las dimensiones del rectángulo de origen (en función de la posición del mouse y las dimensiones de la ventana del ampliador dividido por el factor de ampliación) y establece el rectángulo de origen en consecuencia. La función también centra el área cliente de la ventana host en la posición del mouse. Esta función se llamaría a intervalos para actualizar la ventana de ampliación.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Aplicar efectos de color

Un control ampliador que tiene el estilo [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) aplica una matriz de transformación de color integrada que invierte los colores del contenido de la pantalla ampliada. En la ilustración siguiente se muestra el contenido de la pantalla en un control ampliador que tiene el estilo **MS_INVERTCOLORS** .

![captura de pantalla del contenido ampliado con colores invertidos](images/color-inversion.png)

La función [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) permite aplicar otros efectos de color estableciendo una matriz de transformación de color definida por la aplicación. Por ejemplo, la función siguiente establece una matriz de transformación de color que convierte los colores a escala de grises.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

Para obtener más información sobre cómo funcionan las transformaciones de color, vea [usar una matriz de colores para transformar un color único](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) en la documentación de GDI+.

### <a name="selective-magnification"></a>Ampliación selectiva

De forma predeterminada, la ampliación se aplica a todas las ventanas que no sean la propia ventana de ampliación. Para especificar qué ventanas se van a ampliar, llame a la función [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) . Este método toma una lista de ventanas para aumentar o una lista de ventanas que se van a excluir de la ampliación.

## <a name="related-topics"></a>Temas relacionados

[API de ampliación](entry-magapi-sdk.md)