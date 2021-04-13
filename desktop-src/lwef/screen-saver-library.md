---
title: Controlar los protectores de pantalla
description: La API de Microsoft Win32 admite aplicaciones especiales denominadas protectores de pantalla.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- protectores de pantalla
- Panel de control, protectores de pantalla
- ScreenSaverConfigureDialog
- archivos de definición de módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487671"
---
# <a name="handling-screen-savers"></a>Controlar los protectores de pantalla

La API de Microsoft Win32 admite aplicaciones especiales denominadas *protectores de pantalla*. Los protectores de pantalla se inician cuando el mouse y el teclado están inactivos durante un período de tiempo especificado. Se usan por estos dos motivos:

-   Para proteger una pantalla de la grabación de fósforo causada por imágenes estáticas.
-   Para ocultar la información confidencial que queda en una pantalla.

Este tema se divide en las secciones siguientes.

-   [Acerca de los protectores de pantalla](#about-screen-savers)
-   [Usar las funciones del protector de pantalla](#using-the-screen-saver-functions)
    -   [Crear un protector de pantalla](#creating-a-screen-saver)
    -   [Instalar nuevos protectores de pantalla](#installing-new-screen-savers)
    -   [Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Acerca de los protectores de pantalla

La aplicación de escritorio del panel de control de Windows permite a los usuarios seleccionar en una lista de protectores de pantalla, especificar cuánto tiempo debe transcurrir antes de que se inicie el protector de pantalla, configurar protectores de pantalla y obtener una vista previa de los protectores de pantalla. Los protectores de pantalla se cargan automáticamente cuando se inicia Windows o cuando un usuario activa el protector de pantalla a través del panel de control.

Una vez que se elige un protector de pantalla, Windows supervisa las pulsaciones de teclas y los movimientos del mouse y, a continuación, inicia el protector de pantalla después de un período de inactividad. Sin embargo, Windows no inicia el protector de pantalla si se cumple alguna de las condiciones siguientes:

-   La aplicación activa no es una aplicación basada en Windows.
-   Existe una ventana de aprendizaje basado en PC (CBT).
-   La aplicación activa recibe el mensaje de [ \_ SYSCOMMAND de WM](../menurc/wm-syscommand.md) con el parámetro *wParam* establecido en el \_ valor SC SCREENSAVE, pero no pasa el mensaje a la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

**Contexto de seguridad del protector de pantalla**

El contexto de seguridad del protector de pantalla depende de si un usuario ha iniciado sesión de forma interactiva. Si un usuario inicia sesión de forma interactiva cuando se invoca el protector de pantalla, el protector de pantalla se ejecuta en el contexto de seguridad del usuario interactivo. Si ningún usuario ha iniciado sesión, el contexto de seguridad del protector de pantalla depende de la versión de Windows que se esté usando.

-   Windows XP y Windows 2000: el protector de pantalla se ejecuta en el contexto de LocalSystem con cuentas restringidas.
-   Windows 2003-el protector de pantalla se ejecuta en el contexto de LocalService con todos los privilegios quitados y el grupo administradores está deshabilitado.
-   No se aplica a Windows NT4.

El contexto de seguridad determina el nivel de las operaciones con privilegios que se pueden realizar desde un protector de pantalla.

**Windows Vista y versiones posteriores:** Si la Directiva habilita la protección con contraseña, se inicia el protector de pantalla, independientemente de lo que hace una aplicación con la \_ notificación SC SCREENSAVE.

Los protectores de pantalla contienen funciones exportadas, definiciones de recursos y declaraciones de variables específicas. La biblioteca de protectores de pantalla contiene la función **principal** y otro código de inicio necesario para un protector de pantalla. Cuando se inicia un protector de pantalla, el código de inicio de la biblioteca de protector de pantalla crea una ventana de pantalla completa. La clase de ventana para esta ventana se declara de la siguiente manera:


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



Para crear un protector de pantalla, la mayoría de los desarrolladores crean un módulo de código fuente que contiene tres funciones necesarias y los vincula con la biblioteca del protector de pantalla. Un módulo de protector de pantalla solo es responsable de la configuración y de proporcionar efectos visuales.

Una de las tres funciones requeridas en un módulo de protector de pantalla es [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Esta función procesa mensajes específicos y pasa los mensajes no procesados de nuevo a la biblioteca del protector de pantalla. A continuación se muestran algunos de los mensajes típicos procesados por **ScreenSaverProc**.



| Mensaje        | Significado                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| creación de WM \_     | Recupere los datos de inicialización del archivo de Regedit.ini. Establezca un temporizador de ventana para la ventana del protector de pantalla. Realice cualquier otra inicialización requerida.                                     |
| ERASEBKGND de WM \_ | Borre la ventana del protector de pantalla y prepárese para las operaciones de dibujo posteriores.                                                                                                               |
| temporizador de WM \_      | Realizar operaciones de dibujo.                                                                                                                                                                |
| destrucción de WM \_    | Destruya los temporizadores creados cuando la aplicación haya procesado el mensaje de [ \_ creación de WM](../winmsg/wm-create.md) . Realice cualquier limpieza adicional requerida. |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) pasa los mensajes no procesados a la biblioteca del protector de pantalla mediante una llamada a la función [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . En la tabla siguiente se describe cómo procesa esta función varios mensajes.



| Message         | Acción                                                                    |
|-----------------|---------------------------------------------------------------------------|
| SETCURSOR de WM \_   | Establezca el cursor en el cursor nulo y quítelo de la pantalla.           |
| pintura de WM \_       | Pinte el fondo de la pantalla.                                              |
| LBUTTONDOWN de WM \_ | Finalice el protector de pantalla.                                               |
| MBUTTONDOWN de WM \_ | Finalice el protector de pantalla.                                               |
| RBUTTONDOWN de WM \_ | Finalice el protector de pantalla.                                               |
| KEYDOWN de WM \_     | Finalice el protector de pantalla.                                               |
| MOUSEMOVE de WM \_   | Finalice el protector de pantalla.                                               |
| activación de WM \_    | Finalice el protector de pantalla si el parámetro *wParam* está establecido en **false**. |



 

La segunda función necesaria en un módulo de protector de pantalla es [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Esta función muestra un cuadro de diálogo que permite al usuario configurar el protector de pantalla (una aplicación debe proporcionar una plantilla de cuadro de diálogo correspondiente). Windows muestra el cuadro de diálogo Configuración cuando el usuario selecciona el botón **configurar** en el cuadro de diálogo protector de pantalla del panel de control.

La tercera función necesaria en un módulo de protector de pantalla es [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Todas las aplicaciones de protector de pantalla deben llamar a esta función. Sin embargo, las aplicaciones que no requieren controles personalizados o de Windows especiales en el cuadro de diálogo de configuración pueden devolver simplemente **true**. Las aplicaciones que requieren Windows o controles personalizados especiales deben usar esta función para registrar las clases de ventana correspondientes.

Además de crear un módulo que admita las tres funciones que se acaban de describir, un protector de pantalla debe proporcionar un icono. Este icono solo está visible cuando el protector de pantalla se ejecuta como una aplicación independiente. (Para que lo ejecute el panel de control, un protector de pantalla debe tener la extensión de nombre de archivo. SCR; para ejecutarse como una aplicación independiente, debe tener la extensión de nombre de archivo. exe). El icono debe identificarse en el archivo de recursos del protector de pantalla por la aplicación de ID. de constante \_ , que se define en el archivo de encabezado Scrnsave. h.

Un requisito final es una cadena de Descripción del protector de pantalla. El archivo de recursos de un protector de pantalla debe contener una cadena que el panel de control muestre como el nombre del protector de pantalla. La cadena de descripción debe ser la primera cadena de la tabla de cadenas del archivo de recursos (identificada con el valor ordinal 1). Sin embargo, el panel de control omite la cadena de descripción si el protector de pantalla tiene un nombre de archivo largo. En tal caso, el nombre de archivo se utilizará como la cadena de descripción.

## <a name="using-the-screen-saver-functions"></a>Usar las funciones del protector de pantalla

En esta sección se usa el código de ejemplo tomado de una aplicación de protector de pantalla para mostrar las tareas siguientes:

-   [Crear un protector de pantalla](#creating-a-screen-saver)
-   [Instalar nuevos protectores de pantalla](#installing-new-screen-savers)
-   [Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Crear un protector de pantalla

En intervalos que oscilan entre 1 y 10 segundos, la aplicación de este ejemplo vuelve a dibujar la pantalla con uno de cuatro colores: blanco, gris claro, gris oscuro y negro. La aplicación pinta la pantalla cada vez que recibe un [mensaje \_ del temporizador de WM](../winmsg/wm-timer.md) . El usuario puede ajustar el intervalo en el que se envía este mensaje seleccionando el cuadro de diálogo de configuración de la aplicación y ajustando una sola barra de desplazamiento horizontal.

### <a name="screen-saver-library"></a>Biblioteca de protector de pantalla

Las funciones estáticas del protector de pantalla están contenidas en la biblioteca del protector de pantalla. Hay dos versiones de la biblioteca disponibles, Scrnsave. lib y Scrnsavw. lib. Debe vincular el proyecto con uno de estos. Scrnsave. lib se utiliza para los protectores de pantalla que usan caracteres ANSI, y Scrnsavw. lib se usa para los protectores de pantalla que usan caracteres Unicode. Un protector de pantalla que esté vinculado con Scrnsavw. lib solo se ejecutará en plataformas de Windows que admitan Unicode, mientras que un protector de pantalla vinculado con Scrnsave. lib se ejecutará en cualquier plataforma de Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Compatibilidad con el cuadro de diálogo de configuración

La mayoría de los protectores de pantalla proporcionan un cuadro de diálogo de configuración para permitir que el usuario especifique datos de personalización, como colores únicos, velocidades de dibujo, grosor de línea, fuentes, etc. Para admitir el cuadro de diálogo de configuración, la aplicación debe proporcionar una plantilla de cuadro de diálogo y también debe admitir la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) . A continuación se muestra la plantilla de cuadro de diálogo para la aplicación de ejemplo.


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



Debe definir la constante que se usa para identificar la plantilla de cuadro de diálogo mediante el valor decimal 2003, como en el ejemplo siguiente:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



En el ejemplo siguiente se muestra la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) que se encuentra en la aplicación de ejemplo.


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



Además de proporcionar la plantilla de cuadro de diálogo y la compatibilidad con la función [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , una aplicación también debe admitir la función [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . Esta función registra las clases de ventana no estándar que requiere el protector de pantalla. Dado que la aplicación de ejemplo solo usa clases de ventana estándar en el procedimiento del cuadro de diálogo, esta función simplemente devuelve **true**, como en el ejemplo siguiente:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Compatibilidad con el procedimiento de ventana protector de pantalla

Cada protector de pantalla debe admitir un procedimiento de ventana denominado [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Como la mayoría de los procedimientos de ventana, **ScreenSaverProc** procesa un conjunto de mensajes específicos y pasa los mensajes no procesados a un procedimiento predeterminado. Sin embargo, en lugar de pasarlos a la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** pasa los mensajes no procesados a la función [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Otra diferencia entre **ScreenSaverProc** y un procedimiento de ventana normal es que el identificador pasado a **ScreenSaverProc** identifica todo el escritorio en lugar de una ventana de cliente. En el ejemplo siguiente se muestra el procedimiento de ventana **ScreenSaverProc** para el protector de pantalla de ejemplo.


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>Crear un archivo de definición de módulo

Las funciones [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) y [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) se deben exportar en el archivo de definición de módulo de la aplicación; No obstante, no se debe exportar [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . En el ejemplo siguiente se muestra el archivo de definición de módulo para la aplicación de ejemplo.


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>Instalar nuevos protectores de pantalla

Al compilar la lista de protectores de pantalla disponibles, el panel de control busca archivos con la extensión. SCR en el directorio de inicio de Windows. Dado que los protectores de pantalla son archivos ejecutables estándar de Windows con extensiones. exe, debe cambiarles el nombre para que tengan extensiones. SCR y copiarlos en el directorio correcto.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Agregar ayuda al cuadro de diálogo Configuración del protector de pantalla

El cuadro de diálogo de configuración de un protector de pantalla incluye normalmente un botón **ayuda** . Las aplicaciones de protector de pantalla pueden buscar el identificador del botón ayuda y llamar a la función [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) de la misma forma que la ayuda se proporciona en otras aplicaciones basadas en Windows.

 

 