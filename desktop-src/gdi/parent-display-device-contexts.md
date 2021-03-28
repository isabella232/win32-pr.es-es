---
description: Un contexto de dispositivo primario permite a una aplicación minimizar el tiempo necesario para configurar la región de recorte de una ventana.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contextos de dispositivo de pantalla primaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984882"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="e8644-103">Contextos de dispositivo de pantalla primaria</span><span class="sxs-lookup"><span data-stu-id="e8644-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="e8644-104">Un *contexto de dispositivo primario* permite a una aplicación minimizar el tiempo necesario para configurar la región de recorte de una ventana.</span><span class="sxs-lookup"><span data-stu-id="e8644-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="e8644-105">Normalmente, una aplicación usa contextos de dispositivo primarios para acelerar el dibujo de ventanas de control sin necesidad de un contexto de dispositivo privado o de clase.</span><span class="sxs-lookup"><span data-stu-id="e8644-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="e8644-106">Por ejemplo, el sistema utiliza contextos de dispositivo primarios para los controles de botón de control y edición.</span><span class="sxs-lookup"><span data-stu-id="e8644-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="e8644-107">Los contextos de dispositivos primarios están pensados para usarse solo con ventanas secundarias, nunca con ventanas emergentes o de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e8644-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="e8644-108">Una aplicación puede especificar el \_ estilo CS PARENTDC para establecer la región de recorte de la ventana secundaria en la de la ventana primaria para que el elemento secundario pueda dibujar en el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="e8644-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="e8644-109">Al especificar CS \_ PARENTDC, se mejora el rendimiento de una aplicación porque no es necesario que el sistema siga recalculando el área visible para cada ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="e8644-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="e8644-110">Los valores de atributo establecidos por la ventana primaria no se conservan para la ventana secundaria; por ejemplo, la ventana primaria no puede establecer el pincel para sus ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="e8644-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="e8644-111">La única propiedad conservada es la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="e8644-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="e8644-112">La ventana debe recortar su propia salida a los límites de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e8644-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="e8644-113">Dado que la región de recorte del contexto del dispositivo primario es idéntica a la ventana primaria, la ventana secundaria podría dibujarse en toda la ventana primaria, pero el contexto del dispositivo primario no debe usarse de esta manera.</span><span class="sxs-lookup"><span data-stu-id="e8644-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="e8644-114">El sistema omite el estilo CS \_ PARENTDC si la ventana primaria usa un contexto de dispositivo privado o de clase, si la ventana primaria recorta sus ventanas secundarias, o si la ventana secundaria recorta sus ventanas secundarias o las ventanas del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="e8644-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



