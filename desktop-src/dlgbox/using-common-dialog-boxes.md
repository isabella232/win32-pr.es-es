---
title: Usar cuadros de diálogo comunes
description: En esta sección se tratan las tareas que invocan cuadros de diálogo comunes.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Biblioteca común de cuadros de diálogo, tareas
- cuadros de diálogo comunes, mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773382a34b048e812a3fb093da0492b0c628fb14
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590662"
---
# <a name="using-common-dialog-boxes"></a>Usar cuadros de diálogo comunes

En esta sección se tratan las tareas que invocan cuadros de diálogo comunes:

-   [Elegir un color](#choosing-a-color)
-   [Elección de una fuente](#choosing-a-font)
-   [Abrir un archivo](#opening-a-file)
-   [Mostrar el cuadro de diálogo Imprimir](#displaying-the-print-dialog-box)
-   [Usar la hoja de propiedades Imprimir](#using-the-print-property-sheet)
-   [Configuración de la página impresa](#setting-up-the-printed-page)
-   [Buscar texto](#finding-text)

## <a name="choosing-a-color"></a>Elegir un color

En este tema se describe el código de ejemplo que muestra un **cuadro de** diálogo Color para que un usuario pueda seleccionar un color. El código de ejemplo inicializa primero una [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) y, a continuación, llama a [**la función ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) para mostrar el cuadro de diálogo. Si la función devuelve **TRUE**, lo que indica que el usuario ha seleccionado un color, el código de ejemplo usa el color seleccionado para crear un nuevo pincel sólido.

En este ejemplo se usa [**la estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para inicializar el cuadro de diálogo de la siguiente manera:

-   Inicializa el miembro **lpCustColors** con un puntero a una matriz estática de valores. Los colores de la matriz son inicialmente de color negro, pero la matriz estática conserva los colores personalizados creados por el usuario para las llamadas [**a ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) posteriores.
-   Establece la **marca CC \_ RGBINIT** e inicializa el miembro **rgbResult** para especificar el color que se seleccionó inicialmente cuando se abre el cuadro de diálogo. Si no se especifica, la selección inicial es negra. En el ejemplo se usa la variable estática *rgbCurrent* para conservar el valor seleccionado entre las llamadas [**a ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))
-   Establece la **marca CC \_ FULLOPEN** para que siempre se muestre la extensión de colores personalizados del cuadro de diálogo.


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>Elegir una fuente

En este tema se describe el código de ejemplo que muestra un **cuadro de** diálogo Fuente para que un usuario pueda elegir los atributos de una fuente. El código de ejemplo inicializa primero una [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) y, a continuación, llama a la [**función ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para mostrar el cuadro de diálogo.

En este ejemplo se establece **la marca CF \_ SCREENFONTS** para especificar que el cuadro de diálogo solo debe mostrar fuentes de pantalla. Establece la marca **CF \_ EFFECTS para** mostrar los controles que permiten al usuario seleccionar opciones de tachado, subrayado y color.

Si [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **TRUE**, lo que  indica que el usuario hizo clic en el botón Aceptar, la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contiene información que describe los atributos de fuente y fuente seleccionados por el usuario, incluidos los miembros de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a los que apunta el **miembro lpLogFont.** El **miembro rgbColors** contiene el color de texto seleccionado. El código de ejemplo usa esta información para establecer la fuente y el color del texto para el contexto del dispositivo asociado a la ventana del propietario.


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>Abrir un archivo

> [!Note]  
> A partir de Windows Vista, el cuadro de diálogo Archivo común se ha reemplazado por el cuadro de diálogo Elemento común cuando se usa para abrir un archivo. Se recomienda usar Common Item Dialog API en lugar de Common File Dialog API. Para obtener más información, vea [Common Item Dialog](/windows/win32/shell/common-file-dialog).

 

En este tema se describe  el código de ejemplo que muestra un cuadro de diálogo Abrir para que un usuario pueda especificar la unidad, el directorio y el nombre de un archivo que se va a abrir. El código de ejemplo inicializa primero una [**estructura OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y, a continuación, llama a la [**función GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) para mostrar el cuadro de diálogo.

En este ejemplo, el miembro **lpstrFilter** es un puntero a un búfer que especifica dos filtros de nombre de archivo que el usuario puede seleccionar para limitar los nombres de archivo que se muestran. El búfer contiene una matriz terminada en doble null de cadenas en la que cada par de cadenas especifica un filtro. El **miembro nFilterIndex** especifica que se usa el primer patrón cuando se crea el cuadro de diálogo.

En este ejemplo se establecen **las marcas \_ OFN PATHMUSTEXIST** **y OFN \_ FILEMUSTEXIST** en el **miembro Flags.** Estas marcas hacen que el cuadro de diálogo compruebe, antes de devolver, que la ruta de acceso y el nombre de archivo especificados por el usuario existen realmente.

La [**función GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) devuelve **TRUE si** el usuario hace clic en el botón **Aceptar** y existe la ruta de acceso y el nombre de archivo especificados. En este caso, el búfer al que apunta el **miembro lpstrFile** contiene la ruta de acceso y el nombre de archivo. El código de ejemplo usa esta información en una llamada a la función para abrir el archivo.

Aunque en este ejemplo no se establece la **marca OFN \_ EXPLORER,** todavía se muestra el cuadro de diálogo Abrir de estilo **explorador** predeterminado. Sin embargo, si desea proporcionar un procedimiento de enlace o una plantilla personalizada y desea la interfaz de usuario del Explorador, debe establecer la **marca OFN \_ EXPLORER.**

> [!Note]  
> En el lenguaje de programación C, una cadena entre comillas termina en NULL.

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>Mostrar el cuadro de diálogo Imprimir

En este tema se describe el código de ejemplo que muestra un **cuadro de** diálogo Imprimir para que un usuario pueda seleccionar opciones para imprimir un documento. El código de ejemplo inicializa primero una [**estructura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y, a continuación, llama a [**la función PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para mostrar el cuadro de diálogo.

En este ejemplo se establece **la marca \_ PD RETURNDC** en **el miembro Flags** de la [**estructura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Esto hace [**que PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelva un identificador de contexto de dispositivo a la impresora seleccionada en el **miembro hDC.** Puede usar el identificador para representar la salida en la impresora.

En la entrada, el código de ejemplo establece los **miembros hDevMode** y **hDevNames** en **NULL.** Si la función devuelve **TRUE**, estos miembros devuelven identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario y la información sobre la impresora. Puede usar esta información para preparar la salida que se enviará a la impresora seleccionada.


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>Usar la hoja de propiedades imprimir

En este tema se describe el código de ejemplo que muestra una **hoja** de propiedades Imprimir para que un usuario pueda seleccionar opciones para imprimir un documento. El código de ejemplo inicializa primero una [**estructura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) y, a continuación, llama a [**la función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar la hoja de propiedades.

El código de ejemplo establece la **marca \_ PD RETURNDC** en el **miembro Flags** de la [**estructura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Esto hace que [**la función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) devuelva un identificador de contexto de dispositivo a la impresora seleccionada en el **miembro hDC.**

En la entrada, el código de ejemplo establece los **miembros hDevMode** y **hDevNames** en **NULL.** Si la función devuelve **S \_ OK**, estos miembros devuelven identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario y la información sobre la impresora. Puede usar esta información para preparar la salida que se enviará a la impresora seleccionada.

Una vez completada la operación de impresión, el código de ejemplo libera los búferes [**DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) y llama a la [**función DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) para eliminar el contexto del dispositivo.


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>Configuración de la página impresa

En este tema se describe  el código de ejemplo que muestra un cuadro de diálogo Configuración de página para que un usuario pueda seleccionar los atributos de la página impresa, como el tipo de papel, el origen del papel, la orientación de la página y los márgenes de página. El código de ejemplo inicializa primero una [**estructura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) y, a continuación, llama a la [**función PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) para mostrar el cuadro de diálogo.

En este ejemplo se establece la marca **\_ PSD MARGINS** en el **miembro Flags** y se usa el **miembro rtMargin** para especificar los valores de margen iniciales. Establece la **marca PSD \_ INTHOUSANDTHSOFINCHES** para asegurarse de que el cuadro de diálogo expresa las dimensiones de margen en milésimas de pulgada.

En la entrada, el código de ejemplo establece los **miembros hDevMode** y **hDevNames** en **NULL.** Si la función devuelve **TRUE**, la función usa estos miembros para devolver identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario y la información sobre la impresora. Puede usar esta información para preparar la salida que se va a enviar a la impresora seleccionada.

En el ejemplo siguiente también se habilita [**un procedimiento de enlace PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar el dibujo del contenido de la página de ejemplo.


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



En el ejemplo siguiente se muestra un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) de ejemplo que dibuja el rectángulo de margen en el área de página de ejemplo:


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>Buscar texto

En este tema se describe el  código de ejemplo que muestra y administra un cuadro de diálogo Buscar para que el usuario pueda especificar los parámetros de una operación de búsqueda. El cuadro de diálogo envía mensajes al procedimiento de ventana para que pueda realizar la operación de búsqueda.

El código para mostrar y administrar **un** cuadro de diálogo Reemplazar es similar, salvo que usa la [**función ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) para mostrar el cuadro de diálogo. El **cuadro de** diálogo Reemplazar también envía mensajes en respuesta a los clics del usuario en los botones **Reemplazar** **y** Reemplazar todo.

Para usar el **cuadro de** **diálogo** Buscar o reemplazar, debe realizar tres tareas independientes:

1.  Obtenga un identificador de mensaje para el [**mensaje registrado findmsgstring.**](findmsgstring.md)
2.  Mostrar el cuadro de diálogo.
3.  [**Procese mensajes FINDMSGSTRING**](findmsgstring.md) cuando el cuadro de diálogo esté abierto.

Al inicializar la aplicación, llame a [**la función RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje para el [**mensaje registrado de FINDMSGSTRING.**](findmsgstring.md)


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Para mostrar un **cuadro de** diálogo Buscar, inicialice primero una [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y, a continuación, llame a la [**función FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) Tenga en cuenta que la estructura **FINDREPLACE** y el búfer de la cadena de búsqueda deben ser una variable global o estática para que no salga del ámbito antes de que se cierre el cuadro de diálogo. Debe establecer el miembro **hwndOwner para** especificar la ventana que recibe los mensajes registrados. Después de crear el cuadro de diálogo, puede moverlo o manipularlo mediante el identificador devuelto.


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



Cuando el cuadro de diálogo está abierto, el bucle de mensajes principal debe incluir una llamada a la [**función IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Pase un identificador al cuadro de diálogo como parámetro en la **llamada a IsDialogMessage.** Esto garantiza que el cuadro de diálogo procese correctamente los mensajes de teclado.

Para supervisar los mensajes enviados desde el cuadro de diálogo, el procedimiento de ventana debe comprobar el mensaje registrado de [**FINDMSGSTRING**](findmsgstring.md) y procesar los valores pasados en la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) como en el ejemplo siguiente.


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
