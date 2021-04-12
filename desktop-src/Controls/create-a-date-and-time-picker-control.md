---
title: Cómo crear un control de selector de fecha y hora
description: En este tema se muestra cómo crear dinámicamente un control de selector de fecha y hora (DTP).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104271373"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="ff27c-103">Cómo crear un control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ff27c-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="ff27c-104">En este tema se muestra cómo crear dinámicamente un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ff27c-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="ff27c-105">El ejemplo de código de C++ que lo acompaña crea un control de DTP en un cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="ff27c-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="ff27c-106">Usa el estilo [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) para permitir que el usuario simule la desactivación de la fecha dentro del control.</span><span class="sxs-lookup"><span data-stu-id="ff27c-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff27c-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ff27c-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff27c-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ff27c-108">Technologies</span></span>

-   [<span data-ttu-id="ff27c-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ff27c-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ff27c-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ff27c-110">Prerequisites</span></span>

-   <span data-ttu-id="ff27c-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff27c-111">C/C++</span></span>
-   <span data-ttu-id="ff27c-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ff27c-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ff27c-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ff27c-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ff27c-114">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="ff27c-114">Step 1:</span></span>

<span data-ttu-id="ff27c-115">Registre la clase de ventana llamando a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y especificando el \_ \_ bit de clases de fecha de ICC en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff27c-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="ff27c-116">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="ff27c-116">Step 2:</span></span>

<span data-ttu-id="ff27c-117">Para crear el control de DTP, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="ff27c-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="ff27c-118">Especifique [**la \_ clase DATETIMEPICK**](common-control-window-classes.md) como clase de ventana y pase el identificador al cuadro de diálogo primario.</span><span class="sxs-lookup"><span data-stu-id="ff27c-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="ff27c-119">En el siguiente ejemplo de código de C++ se usa la función [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) para crear un cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="ff27c-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="ff27c-120">A continuación, llama a **CreateWindowEx** para crear el control de DTP.</span><span class="sxs-lookup"><span data-stu-id="ff27c-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="ff27c-121">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="ff27c-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="ff27c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff27c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff27c-123">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ff27c-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="ff27c-124">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ff27c-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ff27c-125">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ff27c-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 