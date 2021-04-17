---
description: En este tema se describe cómo recuperar un contexto de dispositivo de impresora.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Cómo: recuperar un contexto de dispositivo de impresora'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697390"
---
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="8e1b8-103">Cómo: recuperar un contexto de dispositivo de impresora</span><span class="sxs-lookup"><span data-stu-id="8e1b8-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="8e1b8-104">En este tema se describe cómo recuperar un contexto de dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="8e1b8-105">Puede recuperar un contexto de dispositivo de impresora llamando directamente a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o puede ser devuelto por un cuadro de diálogo de **impresión** común.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="8e1b8-106">Cuando se muestra un cuadro de diálogo **Imprimir** común, el usuario podrá seleccionar la impresora, las páginas del documento y el número de copias del documento que desee imprimir.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="8e1b8-107">El cuadro de diálogo **Imprimir** común devuelve estas selecciones en una estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="8e1b8-108">En este tema se describe cómo obtener un contexto de dispositivo de impresora mediante los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="8e1b8-109">Llamar a CreateDC</span><span class="sxs-lookup"><span data-stu-id="8e1b8-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="8e1b8-110">Mostrar un cuadro de diálogo de impresión común</span><span class="sxs-lookup"><span data-stu-id="8e1b8-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="8e1b8-111">Usar la función PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="8e1b8-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="8e1b8-112">Usar la función PrintDlg</span><span class="sxs-lookup"><span data-stu-id="8e1b8-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="8e1b8-113">Llamar a CreateDC</span><span class="sxs-lookup"><span data-stu-id="8e1b8-113">Call CreateDC</span></span>

<span data-ttu-id="8e1b8-114">Si conoce el dispositivo en el que desea imprimir, puede llamar a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) y pasar esa información directamente a la función.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="8e1b8-115">**CreateDC** devuelve un contexto de dispositivo en el que se puede representar el contenido que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="8e1b8-116">La llamada más sencilla para recuperar un contexto de dispositivo se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="8e1b8-117">El código de este ejemplo recupera un contexto de dispositivo en el dispositivo de pantalla predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="8e1b8-118">Para representar en una impresora específica, debe especificar "WINSPOOL" como el dispositivo y pasar el nombre correcto de la impresora a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="8e1b8-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="8e1b8-119">También puede pasar una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en la llamada a **CreateDC** si desea proporcionar datos de inicialización específicos del dispositivo para el controlador del dispositivo al crear el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="8e1b8-120">En el ejemplo siguiente se muestra una llamada a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) en la que se selecciona el controlador "WINSPOOL" y el nombre de la impresora se especifica mediante el nombre.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="8e1b8-121">Puede obtener la cadena de nombre de impresora exacta que se va a pasar a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) mediante una llamada a la función [**EnumPrinters**](enumprinters.md) .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="8e1b8-122">En el ejemplo de código siguiente se muestra cómo llamar a **EnumPrinters** y obtener los nombres de las impresoras locales y conectadas localmente.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="8e1b8-123">Dado que el tamaño del búfer necesario no se puede conocer de antemano, se llama dos veces a **EnumPrinters** .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="8e1b8-124">La primera llamada devuelve el tamaño del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="8e1b8-125">Esa información se utiliza para asignar un búfer del tamaño requerido y la segunda llamada a **EnumPrinters** devuelve los datos que desea.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="8e1b8-126">Mostrar un cuadro de diálogo de impresión común</span><span class="sxs-lookup"><span data-stu-id="8e1b8-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="8e1b8-127">Puede elegir entre dos cuadros de diálogo de **impresión** comunes para mostrar a un usuario; el cuadro de diálogo más reciente, que se puede mostrar mediante una llamada a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) y el cuadro de diálogo estilo anterior, que se puede mostrar mediante una llamada a la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="8e1b8-128">En las secciones siguientes se describe cómo llamar a cada cuadro de diálogo desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="8e1b8-129">Usar la función PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="8e1b8-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="8e1b8-130">Llame a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar la hoja de propiedades **Print** .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="8e1b8-131">Mediante el uso de la hoja de propiedades, el usuario puede especificar información sobre el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="8e1b8-132">Por ejemplo, el usuario puede seleccionar un intervalo de páginas para imprimir, el número de copias, etc.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="8e1b8-133">El **PrintDlgEx** también puede recuperar un identificador de un contexto de dispositivo para la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="8e1b8-134">Puede utilizar el identificador para representar la salida en la impresora.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="8e1b8-135">Para ver el código de ejemplo que muestra el uso de [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para recuperar un contexto de dispositivo de impresora, vea el tema sobre cómo usar la hoja de propiedades de impresión en [uso de cuadros de diálogo comunes](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="8e1b8-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="8e1b8-136">Usar la función PrintDlg</span><span class="sxs-lookup"><span data-stu-id="8e1b8-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="8e1b8-137">Si la aplicación se debe ejecutar en un sistema que no admite la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , como en un sistema que ejecuta una versión de Windows anterior a Windows 2000, o no necesita la funcionalidad adicional que proporciona la función **PrintDlgEx** , use la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="8e1b8-138">En los pasos siguientes se describe cómo mostrar el cuadro de diálogo común **Imprimir** estilo anterior.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="8e1b8-139">Inicialice la estructura de datos [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="8e1b8-140">Llame a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para mostrar el cuadro de diálogo **Imprimir** común al usuario.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="8e1b8-141">Si la llamada a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **true**, bloquee la memoria de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="8e1b8-142">Si la llamada **PrintDlg** devuelve **false**, el usuario presionó el botón **Cancelar** en el cuadro de diálogo **Imprimir** común, por lo que no hay nada más que procesar.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="8e1b8-143">Asigne un búfer de memoria local que sea lo suficientemente grande como para contener una copia de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="8e1b8-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="8e1b8-144">Copie la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta a la asignada localmente.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="8e1b8-145">Guarde la información que se devuelve en la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y que tendrá que procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="8e1b8-146">Libere el [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y los búferes de memoria a los que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="8e1b8-147">En el ejemplo de código siguiente se muestra cómo usar la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para obtener el contexto de dispositivo y el nombre de la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="8e1b8-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



<span data-ttu-id="8e1b8-148">Para obtener más información acerca de la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , vea "Mostrar el cuadro de diálogo Imprimir" en el tema sobre el [uso de cuadros de diálogo comunes](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="8e1b8-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
