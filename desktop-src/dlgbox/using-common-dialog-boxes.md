---
title: Usar cuadros de diálogo comunes
description: En esta sección se describen las tareas que invocan cuadros de diálogo comunes.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Biblioteca de cuadros de diálogo comunes, tareas
- cuadros de diálogo comunes, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "105695810"
---
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="c462e-105">Usar cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="c462e-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="c462e-106">En esta sección se describen las tareas que invocan cuadros de diálogo comunes:</span><span class="sxs-lookup"><span data-stu-id="c462e-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="c462e-107">Elegir un color</span><span class="sxs-lookup"><span data-stu-id="c462e-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="c462e-108">Elección de una fuente</span><span class="sxs-lookup"><span data-stu-id="c462e-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="c462e-109">Abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="c462e-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="c462e-110">Mostrar el cuadro de diálogo Imprimir</span><span class="sxs-lookup"><span data-stu-id="c462e-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="c462e-111">Usar la hoja de propiedades imprimir</span><span class="sxs-lookup"><span data-stu-id="c462e-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="c462e-112">Configuración de la página impresa</span><span class="sxs-lookup"><span data-stu-id="c462e-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="c462e-113">Buscar texto</span><span class="sxs-lookup"><span data-stu-id="c462e-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="c462e-114">Elegir un color</span><span class="sxs-lookup"><span data-stu-id="c462e-114">Choosing a Color</span></span>

<span data-ttu-id="c462e-115">En este tema se describe el código de ejemplo que muestra un cuadro de diálogo de **color** para que un usuario pueda seleccionar un color.</span><span class="sxs-lookup"><span data-stu-id="c462e-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="c462e-116">En primer lugar, el código de ejemplo Inicializa una estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) y, a continuación, llama a la función [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="c462e-117">Si la función devuelve **true**, lo que indica que el usuario seleccionó un color, el código de ejemplo utiliza el color seleccionado para crear un nuevo pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="c462e-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="c462e-118">En este ejemplo se usa la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para inicializar el cuadro de diálogo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c462e-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="c462e-119">Inicializa el miembro **lpCustColors** con un puntero a una matriz estática de valores.</span><span class="sxs-lookup"><span data-stu-id="c462e-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="c462e-120">Los colores de la matriz son inicialmente negros, pero la matriz estática conserva los colores personalizados creados por el usuario para las llamadas posteriores a [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c462e-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="c462e-121">Establece la **marca \_ RGBINIT de CC** e inicializa el miembro **rgbResult** para especificar el color que se selecciona inicialmente al abrir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="c462e-122">Si no se especifica, la selección inicial es negra.</span><span class="sxs-lookup"><span data-stu-id="c462e-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="c462e-123">En el ejemplo se utiliza la variable estática *rgbCurrent* para conservar el valor seleccionado entre las llamadas a [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c462e-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="c462e-124">Establece la **marca \_ FULLOPEN de CC** , de modo que siempre se muestra la extensión de colores personalizados del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="c462e-125">Elección de una fuente</span><span class="sxs-lookup"><span data-stu-id="c462e-125">Choosing a Font</span></span>

<span data-ttu-id="c462e-126">En este tema se describe el código de ejemplo que muestra un cuadro de diálogo de **fuente** para que un usuario pueda elegir los atributos de una fuente.</span><span class="sxs-lookup"><span data-stu-id="c462e-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="c462e-127">En primer lugar, el código de ejemplo Inicializa una estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) y, a continuación, llama a la función [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="c462e-128">En este ejemplo se establece la marca **CF \_ SCREENFONTS** para especificar que el cuadro de diálogo solo debe mostrar fuentes de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c462e-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="c462e-129">Establece la marca **de \_ efectos de CF** para mostrar los controles que permiten al usuario seleccionar las opciones de tachado, subrayado y color.</span><span class="sxs-lookup"><span data-stu-id="c462e-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="c462e-130">Si [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **true**, lo que indica que el usuario hizo clic en el botón **Aceptar** , la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contiene información que describe los atributos de fuente y fuente seleccionados por el usuario, incluidos los miembros de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a la que apunta el miembro **lpLogFont** .</span><span class="sxs-lookup"><span data-stu-id="c462e-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="c462e-131">El miembro **rgbColors** contiene el color de texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c462e-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="c462e-132">En el código de ejemplo se utiliza esta información para establecer la fuente y el color del texto del contexto de dispositivo asociado a la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="c462e-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="c462e-133">Abrir un archivo</span><span class="sxs-lookup"><span data-stu-id="c462e-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="c462e-134">A partir de Windows Vista, el cuadro de diálogo de archivo común se ha sustituido por el cuadro de diálogo de elemento común cuando se usa para abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="c462e-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="c462e-135">Se recomienda usar la API de cuadro de diálogo Common item en lugar de la API Common File Dialog.</span><span class="sxs-lookup"><span data-stu-id="c462e-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="c462e-136">Para obtener más información, vea [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c462e-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="c462e-137">En este tema se describe el código de ejemplo que muestra un cuadro de diálogo **abierto** para que un usuario pueda especificar la unidad, el directorio y el nombre de un archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="c462e-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="c462e-138">En primer lugar, el código de ejemplo Inicializa una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y, a continuación, llama a la función [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="c462e-139">En este ejemplo, el miembro **lpstrFilter** es un puntero a un búfer que especifica dos filtros de nombre de archivo que el usuario puede seleccionar para limitar los nombres de archivo que se muestran.</span><span class="sxs-lookup"><span data-stu-id="c462e-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="c462e-140">El búfer contiene una matriz de cadenas terminada en un doble nulo, en la que cada par de cadenas especifica un filtro.</span><span class="sxs-lookup"><span data-stu-id="c462e-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="c462e-141">El miembro **nFilterIndex** especifica que el primer patrón se usa cuando se crea el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="c462e-142">En este ejemplo se establecen las marcas **OFN \_ PATHMUSTEXIST** y **OFN \_ FILEMUSTEXIST** en el miembro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="c462e-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="c462e-143">Estas marcas hacen que el cuadro de diálogo Compruebe, antes de que se devuelva, que la ruta de acceso y el nombre de archivo especificados por el usuario existen realmente.</span><span class="sxs-lookup"><span data-stu-id="c462e-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="c462e-144">La función [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) devuelve **true** si el usuario hace clic en el botón **Aceptar** y existe la ruta de acceso y el nombre de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="c462e-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="c462e-145">En este caso, el búfer señalado por el miembro **lpstrFile** contiene la ruta de acceso y el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c462e-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="c462e-146">En el código de ejemplo se utiliza esta información en una llamada a la función para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="c462e-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="c462e-147">Aunque este ejemplo no establece la marca **del \_ Explorador de OFN** , sigue mostrando el cuadro de diálogo **abrir** de estilo de explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c462e-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="c462e-148">Sin embargo, si desea proporcionar un procedimiento de enlace o una plantilla personalizada y desea la interfaz de usuario del explorador, debe establecer la marca **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="c462e-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="c462e-149">En el lenguaje de programación C, una cadena entre comillas termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="c462e-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="c462e-150">Mostrar el cuadro de diálogo Imprimir</span><span class="sxs-lookup"><span data-stu-id="c462e-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="c462e-151">En este tema se describe el código de ejemplo que muestra un cuadro de diálogo **Imprimir** para que un usuario pueda seleccionar las opciones de impresión de un documento.</span><span class="sxs-lookup"><span data-stu-id="c462e-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="c462e-152">En primer lugar, el código de ejemplo Inicializa una estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y, a continuación, llama a la función [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="c462e-153">En este ejemplo se establece la marca **PD \_ RETURNDC** en el miembro **Flags** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="c462e-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="c462e-154">Esto hace que [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelva un identificador de contexto de dispositivo a la impresora seleccionada en el miembro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="c462e-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="c462e-155">Puede utilizar el identificador para representar la salida en la impresora.</span><span class="sxs-lookup"><span data-stu-id="c462e-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="c462e-156">En la entrada, el código de ejemplo establece los miembros **hDevMode** y **hDevNames** en **null**.</span><span class="sxs-lookup"><span data-stu-id="c462e-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c462e-157">Si la función devuelve **true**, estos miembros devuelven los identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario e información sobre la impresora.</span><span class="sxs-lookup"><span data-stu-id="c462e-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="c462e-158">Puede usar esta información para preparar la salida que se va a enviar a la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c462e-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="c462e-159">Usar la hoja de propiedades imprimir</span><span class="sxs-lookup"><span data-stu-id="c462e-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="c462e-160">En este tema se describe el código de ejemplo que muestra una hoja de propiedades de **impresión** para que un usuario pueda seleccionar las opciones de impresión de un documento.</span><span class="sxs-lookup"><span data-stu-id="c462e-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="c462e-161">En primer lugar, el código de ejemplo Inicializa una estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) y, a continuación, llama a la función [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c462e-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="c462e-162">El código de ejemplo establece la marca **PD \_ RETURNDC** en el miembro **Flags** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="c462e-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="c462e-163">Esto hace que la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) devuelva un identificador de contexto de dispositivo a la impresora seleccionada en el miembro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="c462e-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="c462e-164">En la entrada, el código de ejemplo establece los miembros **hDevMode** y **hDevNames** en **null**.</span><span class="sxs-lookup"><span data-stu-id="c462e-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c462e-165">Si la función devuelve los valores **\_ correctos**, estos miembros devuelven los identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario e información sobre la impresora.</span><span class="sxs-lookup"><span data-stu-id="c462e-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="c462e-166">Puede usar esta información para preparar la salida que se va a enviar a la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c462e-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="c462e-167">Una vez completada la operación de impresión, el código de ejemplo libera los búferes [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)y [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) y llama a la función [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) para eliminar el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c462e-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="c462e-168">Configuración de la página impresa</span><span class="sxs-lookup"><span data-stu-id="c462e-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="c462e-169">En este tema se describe el código de ejemplo que muestra un cuadro de diálogo **Configurar página** para que un usuario pueda seleccionar los atributos de la página impresa, como el tipo de papel, el origen del papel, la orientación de la página y los márgenes de página.</span><span class="sxs-lookup"><span data-stu-id="c462e-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="c462e-170">En primer lugar, el código de ejemplo Inicializa una estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) y, a continuación, llama a la función [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="c462e-171">En este ejemplo se establece la marca de **\_ márgenes PSD** en el miembro **Flags** y se usa el miembro **rtMargin** para especificar los valores de margen iniciales.</span><span class="sxs-lookup"><span data-stu-id="c462e-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="c462e-172">Establece la marca **de \_ INTHOUSANDTHSOFINCHES PSD** para asegurarse de que el cuadro de diálogo expresa las dimensiones de los márgenes en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="c462e-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="c462e-173">En la entrada, el código de ejemplo establece los miembros **hDevMode** y **hDevNames** en **null**.</span><span class="sxs-lookup"><span data-stu-id="c462e-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="c462e-174">Si la función devuelve **true**, la función utiliza estos miembros para devolver los identificadores a las estructuras [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contienen la entrada del usuario e información sobre la impresora.</span><span class="sxs-lookup"><span data-stu-id="c462e-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="c462e-175">Puede usar esta información para preparar la salida que se va a enviar a la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c462e-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="c462e-176">En el ejemplo siguiente también se habilita un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar el dibujo del contenido de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c462e-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="c462e-177">En el ejemplo siguiente se muestra un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) de ejemplo que dibuja el rectángulo de margen en el área de la página de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c462e-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="c462e-178">Buscar texto</span><span class="sxs-lookup"><span data-stu-id="c462e-178">Finding Text</span></span>

<span data-ttu-id="c462e-179">En este tema se describe el código de ejemplo que muestra y administra un cuadro de diálogo **Buscar** para que el usuario pueda especificar los parámetros de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c462e-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="c462e-180">El cuadro de diálogo envía mensajes al procedimiento de ventana para que pueda realizar la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c462e-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="c462e-181">El código para mostrar y administrar un cuadro de diálogo **reemplazar** es similar, salvo que usa la función [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="c462e-182">El cuadro de diálogo **reemplazar** también envía mensajes en respuesta a los clics del usuario en los botones **reemplazar** y **reemplazar todo** .</span><span class="sxs-lookup"><span data-stu-id="c462e-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="c462e-183">Para usar el cuadro de diálogo **Buscar** o **reemplazar** , debe realizar tres tareas independientes:</span><span class="sxs-lookup"><span data-stu-id="c462e-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="c462e-184">Obtiene un identificador de mensaje para el mensaje registrado de [**FINDMSGSTRING**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="c462e-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="c462e-185">Mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="c462e-186">Procesa los mensajes [**FINDMSGSTRING**](findmsgstring.md) cuando el cuadro de diálogo está abierto.</span><span class="sxs-lookup"><span data-stu-id="c462e-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="c462e-187">Al inicializar la aplicación, llame a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje para el mensaje registrado [**FINDMSGSTRING**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="c462e-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="c462e-188">Para mostrar un cuadro de diálogo **Buscar** , primero inicialice una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) y, a continuación, llame a la función [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="c462e-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="c462e-189">Tenga en cuenta que la estructura **FINDREPLACE** y el búfer de la cadena de búsqueda deben ser una variable global o estática para que no salgan del ámbito antes de que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c462e-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="c462e-190">Debe establecer el miembro **hwndOwner** para especificar la ventana que recibe los mensajes registrados.</span><span class="sxs-lookup"><span data-stu-id="c462e-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="c462e-191">Después de crear el cuadro de diálogo, puede moverlo o manipularlo mediante el identificador devuelto.</span><span class="sxs-lookup"><span data-stu-id="c462e-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="c462e-192">Cuando el cuadro de diálogo está abierto, el bucle de mensajes principal debe incluir una llamada a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) .</span><span class="sxs-lookup"><span data-stu-id="c462e-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="c462e-193">Pase un identificador al cuadro de diálogo como parámetro en la llamada a **IsDialogMessage** .</span><span class="sxs-lookup"><span data-stu-id="c462e-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="c462e-194">Esto garantiza que el cuadro de diálogo procesa correctamente los mensajes del teclado.</span><span class="sxs-lookup"><span data-stu-id="c462e-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="c462e-195">Para supervisar los mensajes enviados desde el cuadro de diálogo, el procedimiento de ventana debe comprobar el mensaje registrado [**FINDMSGSTRING**](findmsgstring.md) y procesar los valores pasados en la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c462e-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
