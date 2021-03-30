---
description: En este tema se describe cómo recopilar información del trabajo de impresión del usuario.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: 'Cómo: recopilar información del trabajo de impresión del usuario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082636"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="2a643-103">Cómo: recopilar información del trabajo de impresión del usuario</span><span class="sxs-lookup"><span data-stu-id="2a643-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="2a643-104">En este tema se describe cómo recopilar información del trabajo de impresión del usuario.</span><span class="sxs-lookup"><span data-stu-id="2a643-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="2a643-105">Información general</span><span class="sxs-lookup"><span data-stu-id="2a643-105">Overview</span></span>

<span data-ttu-id="2a643-106">Recopile información del trabajo de impresión del usuario mediante una llamada a la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a643-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="2a643-107">Esta función muestra el cuadro de diálogo **Imprimir** común al usuario y devuelve la información del trabajo de impresión en una estructura de datos [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="2a643-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="2a643-108">El cuadro de diálogo **Imprimir** común se muestra cuando el usuario inicia un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2a643-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="2a643-109">El cuadro de diálogo **Imprimir** común es un cuadro de diálogo modal, lo que significa que el usuario no puede interactuar con la ventana principal hasta que se cierre el cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="2a643-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="2a643-110">Recopilar información del trabajo de impresión</span><span class="sxs-lookup"><span data-stu-id="2a643-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="2a643-111">Inicialice el elemento de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="2a643-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="2a643-112">Para que un programa pueda mostrar el cuadro de diálogo **Imprimir** común, debe asignar e inicializar una estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="2a643-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="2a643-113">A continuación, pasa esta estructura a la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , que muestra el cuadro de diálogo y devuelve los datos del trabajo de impresión en la misma estructura.</span><span class="sxs-lookup"><span data-stu-id="2a643-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="2a643-114">En el ejemplo de código siguiente se muestra cómo realiza este paso el programa de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2a643-114">The following code example shows how the sample program performs this step.</span></span>

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  <span data-ttu-id="2a643-115">Muestra el cuadro de diálogo **Imprimir** común.</span><span class="sxs-lookup"><span data-stu-id="2a643-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="2a643-116">Llame a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) con la estructura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) inicializada para mostrar el cuadro de diálogo **Imprimir** común y recopilar los datos de usuario, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a643-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="2a643-117">Guarde los campos de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e inicie el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2a643-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="2a643-118">La estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contiene los datos que describen las selecciones realizadas por el usuario en el cuadro de diálogo Imprimir.</span><span class="sxs-lookup"><span data-stu-id="2a643-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="2a643-119">Algunos miembros de la estructura **PRINTDLG** son identificadores de los objetos de memoria global.</span><span class="sxs-lookup"><span data-stu-id="2a643-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="2a643-120">El [programa de ejemplo de impresión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copia los datos de los objetos de memoria global en bloques de memoria que el programa administra y copia otros campos de la estructura **PRINTDLG** en los campos de una estructura de datos definida por el programa.</span><span class="sxs-lookup"><span data-stu-id="2a643-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="2a643-121">Después de almacenar los datos de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) en la estructura de datos del programa, puede abrir el cuadro de diálogo progreso de la impresión.</span><span class="sxs-lookup"><span data-stu-id="2a643-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="2a643-122">El procedimiento del cuadro de diálogo progreso de impresión controla los mensajes del cuadro de diálogo e inicia el subproceso de procesamiento de impresión.</span><span class="sxs-lookup"><span data-stu-id="2a643-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="2a643-123">En el ejemplo de código siguiente se muestra cómo copiar los datos de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) en la estructura de datos del programa y cómo iniciar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2a643-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  <span data-ttu-id="2a643-124">Si el usuario hace clic en el botón **Cancelar** en el cuadro de diálogo **Imprimir** común, no se realiza ningún otro procesamiento.</span><span class="sxs-lookup"><span data-stu-id="2a643-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
