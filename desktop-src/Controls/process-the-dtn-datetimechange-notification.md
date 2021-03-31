---
title: Cómo procesar la notificación de DTN_DATETIMECHANGE
description: En este tema se muestra cómo procesar la notificación de cambios realizados por el usuario en el control selector de fecha y hora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995775"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="ba038-103">Cómo procesar la notificación de \_ DATETIMECHANGE de DTN</span><span class="sxs-lookup"><span data-stu-id="ba038-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="ba038-104">En este tema se muestra cómo procesar la notificación de cambios realizados por el usuario en el control selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ba038-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ba038-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ba038-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ba038-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ba038-106">Technologies</span></span>

-   [<span data-ttu-id="ba038-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ba038-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ba038-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba038-108">Prerequisites</span></span>

-   <span data-ttu-id="ba038-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ba038-109">C/C++</span></span>
-   <span data-ttu-id="ba038-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ba038-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ba038-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ba038-111">Instructions</span></span>


<span data-ttu-id="ba038-112">Un control de DTP envía el código de notificación [ \_ DATETIMECHANGE de DTN](dtn-datetimechange.md) cada vez que se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="ba038-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="ba038-113">Por ejemplo, esta notificación se generará cuando el usuario cambie uno de los campos del control o, en el caso de que el control se establezca en el [**estilo \_ SHOWNONE de DTS**](date-and-time-picker-control-styles.md) , cuando el usuario cambie el estado de la casilla del control.</span><span class="sxs-lookup"><span data-stu-id="ba038-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="ba038-114">La aplicación debe incluir código para procesar \_ los mensajes de DTN DATETIMECHANGE que envía el control de DTP.</span><span class="sxs-lookup"><span data-stu-id="ba038-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="ba038-115">El siguiente ejemplo de código C++ es una función definida por la aplicación diseñada para indicar el estado de un control de DTP establecido en el estilo **\_ SHOWNONE de DTS** .</span><span class="sxs-lookup"><span data-stu-id="ba038-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="ba038-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba038-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba038-117">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ba038-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="ba038-118">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ba038-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ba038-119">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ba038-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




