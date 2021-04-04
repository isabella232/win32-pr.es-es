---
title: Usar controles rebar
description: Esta sección contiene temas que muestran cómo crear y usar los controles rebar.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794031"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="9ab1e-103">Usar controles rebar</span><span class="sxs-lookup"><span data-stu-id="9ab1e-103">Using Rebar Controls</span></span>

<span data-ttu-id="9ab1e-104">Esta sección contiene temas que muestran cómo crear y usar los controles rebar.</span><span class="sxs-lookup"><span data-stu-id="9ab1e-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ab1e-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9ab1e-105">In this section</span></span>



| <span data-ttu-id="9ab1e-106">Tema</span><span class="sxs-lookup"><span data-stu-id="9ab1e-106">Topic</span></span>                                                                | <span data-ttu-id="9ab1e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ab1e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ab1e-108">Cómo crear controles rebar</span><span class="sxs-lookup"><span data-stu-id="9ab1e-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="9ab1e-109">Una aplicación crea un control rebar llamando a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando [**REBARCLASSNAME**](common-control-window-classes.md) como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="9ab1e-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="9ab1e-110">La aplicación debe registrar primero la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando el \_ \_ bit de las clases de ICC Cool en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9ab1e-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

