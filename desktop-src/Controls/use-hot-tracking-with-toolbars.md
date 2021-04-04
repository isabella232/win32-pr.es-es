---
title: Cómo usar Hot-Tracking con barras de herramientas
description: Cuando se mantiene el puntero del mouse sobre un elemento, el elemento pasa a estar activo. Si está habilitado el seguimiento activo, se resalta el elemento activo. Una barra de herramientas que se crea con el \_ estilo plano TBSTYLE, o una que usa estilos visuales, admite el seguimiento activo de forma predeterminada.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104077470"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="b0e24-105">Cómo usar Hot-Tracking con barras de herramientas</span><span class="sxs-lookup"><span data-stu-id="b0e24-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="b0e24-106">Cuando se mantiene el puntero del mouse sobre un elemento, el elemento pasa a estar activo.</span><span class="sxs-lookup"><span data-stu-id="b0e24-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="b0e24-107">Si está habilitado el seguimiento activo, se resalta el elemento activo.</span><span class="sxs-lookup"><span data-stu-id="b0e24-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="b0e24-108">Una barra de herramientas que se crea con el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) , o una que usa [estilos visuales](themes-overview.md), admite el seguimiento activo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b0e24-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="b0e24-109">El seguimiento activo requiere la creación de listas de imágenes. por lo tanto, no puede usar el mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) o la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para crear la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b0e24-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="b0e24-110">Cuando el mouse se desplaza sobre un botón de la barra de herramientas, el botón se describe para resaltarlo.</span><span class="sxs-lookup"><span data-stu-id="b0e24-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="b0e24-111">En la ilustración siguiente se muestra una barra de herramientas con el seguimiento activo habilitado; se mantiene el puntero del mouse en el botón Guardar cuando se tomó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b0e24-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![captura de pantalla de un cuadro de diálogo con una barra de herramientas de tres elementos; se describe el icono seleccionado](images/tb-withstyles.png)

<span data-ttu-id="b0e24-113">Si desea que un mapa de bits del botón de la barra de herramientas cambie cuando cambie el estado del control, almacene las distintas imágenes en [las listas de imágenes](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="b0e24-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="b0e24-114">Por ejemplo, algunas aplicaciones tienen botones de barra de herramientas en blanco y negro que se colorean cuando se seleccionan.</span><span class="sxs-lookup"><span data-stu-id="b0e24-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="b0e24-115">Las dos imágenes diferentes se almacenan en las listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0e24-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="b0e24-116">Las barras de herramientas admiten el uso de hasta tres listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0e24-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="b0e24-117">Normalmente, una aplicación tiene una lista de imágenes predeterminada, deshabilitada y de seguimiento activo.</span><span class="sxs-lookup"><span data-stu-id="b0e24-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="b0e24-118">Para establecer y recuperar listas de imágenes para botones de la barra de herramientas activa, use los mensajes [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) y [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e24-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b0e24-119">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="b0e24-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b0e24-120">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="b0e24-120">Technologies</span></span>

-   [<span data-ttu-id="b0e24-121">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="b0e24-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b0e24-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b0e24-122">Prerequisites</span></span>

-   <span data-ttu-id="b0e24-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="b0e24-123">C/C++</span></span>
-   <span data-ttu-id="b0e24-124">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="b0e24-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b0e24-125">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b0e24-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="b0e24-126">Usar Hot-Tracking con una barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="b0e24-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="b0e24-127">En el ejemplo de código siguiente se crea, se rellena y se asigna una lista de imágenes para los botones de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="b0e24-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="b0e24-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0e24-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e24-129">Usar controles Toolbar</span><span class="sxs-lookup"><span data-stu-id="b0e24-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="b0e24-130">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="b0e24-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




