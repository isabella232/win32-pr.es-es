---
title: Cómo crear controles estáticos
description: En el ejemplo de esta sección se muestra cómo crear un control estático animado.
ms.assetid: D2DA38CB-360C-49EC-90BC-9AFA88C4B751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217135a6590fcee60286d21f00233916c4eba967
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487378"
---
# <a name="how-to-create-static-controls"></a><span data-ttu-id="bc08e-103">Cómo crear controles estáticos</span><span class="sxs-lookup"><span data-stu-id="bc08e-103">How to Create Static Controls</span></span>

<span data-ttu-id="bc08e-104">En el ejemplo de esta sección se muestra cómo crear un control estático animado.</span><span class="sxs-lookup"><span data-stu-id="bc08e-104">The example in this section demonstrates how to create an animated static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bc08e-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="bc08e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bc08e-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="bc08e-106">Technologies</span></span>

-   [<span data-ttu-id="bc08e-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="bc08e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bc08e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc08e-108">Prerequisites</span></span>

-   <span data-ttu-id="bc08e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc08e-109">C/C++</span></span>
-   <span data-ttu-id="bc08e-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="bc08e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bc08e-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="bc08e-111">Instructions</span></span>

### <a name="create-a-static-control"></a><span data-ttu-id="bc08e-112">Crear un control estático</span><span class="sxs-lookup"><span data-stu-id="bc08e-112">Create a Static Control</span></span>

<span data-ttu-id="bc08e-113">En el ejemplo de código siguiente se usa un temporizador y el mensaje [**STM \_ SETICON**](stm-seticon.md) para animar un control de icono estático en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bc08e-113">The following code example uses a timer and the [**STM\_SETICON**](stm-seticon.md) message to animate a static icon control in a dialog box.</span></span>


```C++
#define MAXICONS 3 
#define HALF_SECOND 500

INT_PTR CALLBACK StaticDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam) 
{ 
    static HICON aIcons[MAXICONS]; 
    static UINT i = 0; 
    static UINT idTimer = 1; 

    switch (message) 
    { 
        case WM_INITDIALOG: 

            // Load the icon resources. g_hInst is the global instance handle.
            aIcons[i]   = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON1)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON2)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON3)); 
            
            // Reset the array index.
            i = 0;
 
            // Set a timer. 
            SetTimer(hDlg, idTimer, HALF_SECOND, (TIMERPROC) NULL); 
            return TRUE; 

        case WM_TIMER: 

            // Use STM_SETICON to associate a new icon with the static icon
            // control whenever a WM_TIMER message is received. 
            SendDlgItemMessage(hDlg, IDC_STATIC_ICON, STM_SETICON, 
                (WPARAM) aIcons[i], 0);                    

            // Reset the array index, if necessary.
            if (++i == MAXICONS)
                i = 0;

            return 0; 

        case WM_COMMAND: 
            if (wParam == IDOK 
                || wParam == IDCANCEL) 
            { 
                EndDialog(hDlg, TRUE); 
            } 
            return TRUE; 
 
        case WM_DESTROY: 
            KillTimer(hDlg, idTimer); 

            // Note that it is not necessary to call DestroyIcon here. LoadIcon
            // obtains a shared icon, which is valid as long as the module from 
            // which it was loaded is in memory. 
 
            return 0; 
    } 
    return FALSE; 

    UNREFERENCED_PARAMETER(lParam); 
} 
```



## <a name="remarks"></a><span data-ttu-id="bc08e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc08e-114">Remarks</span></span>

<span data-ttu-id="bc08e-115">El identificador del control de icono estático (IDI \_ static \_ Icon) se define en un archivo de encabezado global y los iconos se cargan desde los recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc08e-115">The identifier of the static icon control (IDI\_STATIC\_ICON) is defined in a global header file, and the icons are loaded from the application resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc08e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc08e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc08e-117">Usar controles estáticos</span><span class="sxs-lookup"><span data-stu-id="bc08e-117">Using Static Controls</span></span>](using-static-controls.md)
</dt> <dt>

<span data-ttu-id="bc08e-118">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bc08e-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




