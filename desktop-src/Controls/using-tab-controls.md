---
title: Usar controles de ficha
description: Este tema contiene dos ejemplos que usan controles de ficha.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488418"
---
# <a name="using-tab-controls"></a><span data-ttu-id="10f7e-103">Usar controles de ficha</span><span class="sxs-lookup"><span data-stu-id="10f7e-103">Using Tab Controls</span></span>

<span data-ttu-id="10f7e-104">Este tema contiene dos ejemplos que usan controles de ficha.</span><span class="sxs-lookup"><span data-stu-id="10f7e-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="10f7e-105">En el primer ejemplo se muestra cómo usar un control de pestaña para cambiar entre varias páginas de texto en la ventana principal de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="10f7e-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="10f7e-106">En el segundo ejemplo se muestra cómo utilizar un control de ficha para cambiar entre varias páginas de controles en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10f7e-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="10f7e-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="10f7e-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10f7e-108">Tema</span><span class="sxs-lookup"><span data-stu-id="10f7e-108">Topic</span></span></th>
<th><span data-ttu-id="10f7e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="10f7e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10f7e-110"><a href="create-a-tab-control-in-the-main-window.md">Cómo crear un control de pestaña en la ventana principal</a></span><span class="sxs-lookup"><span data-stu-id="10f7e-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="10f7e-111">En el ejemplo de esta sección se muestra cómo crear un control de pestaña y cómo mostrarlo en el área cliente de la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10f7e-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="10f7e-112">La aplicación muestra una tercera ventana (un control estático) en el área de presentación del control de ficha.</span><span class="sxs-lookup"><span data-stu-id="10f7e-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="10f7e-113">La ventana primaria coloca y ajusta el tamaño del control de pestaña y del control estático cuando procesa el mensaje de <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="10f7e-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="10f7e-114">En este ejemplo hay siete pestañas, una para cada día de la semana.</span><span class="sxs-lookup"><span data-stu-id="10f7e-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="10f7e-115">Cuando el usuario selecciona una pestaña, la aplicación muestra el nombre del día correspondiente en el control estático.</span><span class="sxs-lookup"><span data-stu-id="10f7e-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f7e-116"><a href="create-a-tabbed-dialog-box.md">Cómo crear un cuadro de diálogo con pestañas</a></span><span class="sxs-lookup"><span data-stu-id="10f7e-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="10f7e-117">En el ejemplo de esta sección se muestra cómo crear un cuadro de diálogo que usa pestañas para proporcionar varias páginas de controles.</span><span class="sxs-lookup"><span data-stu-id="10f7e-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="10f7e-118">El cuadro de diálogo principal es un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="10f7e-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="10f7e-119">Cada página de controles se define mediante una plantilla de cuadro de diálogo que tiene el estilo <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="10f7e-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="10f7e-120">Cuando se selecciona una ficha, se crea un cuadro de diálogo no modal para la página entrante y se destruye el cuadro de diálogo de la página saliente.</span><span class="sxs-lookup"><span data-stu-id="10f7e-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="10f7e-121">En muchos casos, puede implementar cuadros de diálogo de varias páginas más fácilmente mediante el uso de hojas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="10f7e-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="10f7e-122">Para obtener más información acerca de las hojas de propiedades, vea <a href="property-sheets.md">acerca de las hojas de propiedades</a>.</span><span class="sxs-lookup"><span data-stu-id="10f7e-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="10f7e-123">La plantilla del cuadro de diálogo principal simplemente define dos controles de botón.</span><span class="sxs-lookup"><span data-stu-id="10f7e-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="10f7e-124">Al procesar el mensaje de <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , el procedimiento de cuadro de diálogo crea un control de ficha y carga los recursos de plantilla de cuadro de diálogo para cada uno de los cuadros de diálogo secundarios.</span><span class="sxs-lookup"><span data-stu-id="10f7e-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

