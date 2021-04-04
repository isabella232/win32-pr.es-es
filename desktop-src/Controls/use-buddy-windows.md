---
title: Cómo usar las ventanas de amigos
description: Al establecer otros controles como ventanas de amigos para una barra de control, puede colocar automáticamente esos controles en los extremos de la barra de control como etiquetas.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075556"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="f5130-103">Cómo usar las ventanas de amigos</span><span class="sxs-lookup"><span data-stu-id="f5130-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="f5130-104">Al establecer otros controles como ventanas de amigos para una barra de control, puede colocar automáticamente esos controles en los extremos de la barra de control como etiquetas.</span><span class="sxs-lookup"><span data-stu-id="f5130-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="f5130-105">En la ilustración siguiente se muestra una barra de desplazamiento horizontal y vertical, ambas con controles estáticos como ventanas de amigos.</span><span class="sxs-lookup"><span data-stu-id="f5130-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![captura de pantalla que muestra un cuadro de diálogo con una barra de desplazamiento horizontal y una barra de desplazamiento vertical](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="f5130-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="f5130-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f5130-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="f5130-108">Technologies</span></span>

-   [<span data-ttu-id="f5130-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="f5130-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f5130-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5130-110">Prerequisites</span></span>

-   <span data-ttu-id="f5130-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="f5130-111">C/C++</span></span>
-   <span data-ttu-id="f5130-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="f5130-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f5130-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f5130-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="f5130-114">Usar ventanas de amigos</span><span class="sxs-lookup"><span data-stu-id="f5130-114">Use Buddy Windows</span></span>

<span data-ttu-id="f5130-115">En el ejemplo de código siguiente se crean las ventanas de amigos que se muestran en la ilustración.</span><span class="sxs-lookup"><span data-stu-id="f5130-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="f5130-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5130-116">Remarks</span></span>

<span data-ttu-id="f5130-117">**IDC \_ SLIDER1** e **IDC \_ SLIDER2** se crean trackbars en el editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5130-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5130-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5130-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5130-119">Usar controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="f5130-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




