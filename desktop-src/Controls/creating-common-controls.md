---
title: Crear controles comunes
description: En este tema se describe cómo crear una ventana que pertenece a una clase de ventana definida en la biblioteca de controles comunes, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995739"
---
# <a name="creating-common-controls"></a><span data-ttu-id="f9960-103">Crear controles comunes</span><span class="sxs-lookup"><span data-stu-id="f9960-103">Creating Common Controls</span></span>

<span data-ttu-id="f9960-104">En este tema se describe cómo crear una ventana que pertenece a una clase de ventana definida en la biblioteca de controles comunes, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="f9960-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="f9960-105">Los controles más comunes pertenecen a una clase de ventana definida en el archivo DLL de control común.</span><span class="sxs-lookup"><span data-stu-id="f9960-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="f9960-106">La clase de ventana y el procedimiento de ventana correspondiente definen las propiedades, la apariencia y el comportamiento del control.</span><span class="sxs-lookup"><span data-stu-id="f9960-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="f9960-107">Para asegurarse de que se carga el archivo DLL de control común, incluya la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9960-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="f9960-108">Cree un control común especificando el nombre de la clase de ventana al llamar a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o especificando el nombre de clase adecuado en una plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9960-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="f9960-109">Cada tipo de control común tiene un conjunto de estilos de control que puede utilizar para modificar la apariencia y el comportamiento del control.</span><span class="sxs-lookup"><span data-stu-id="f9960-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="f9960-110">La biblioteca de controles comunes también incluye un conjunto de estilos de control que se aplican a dos o más tipos de controles comunes.</span><span class="sxs-lookup"><span data-stu-id="f9960-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="f9960-111">Los estilos de control comunes se describen en la sección de [estilos](common-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f9960-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9960-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9960-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9960-113">Acerca de los controles comunes</span><span class="sxs-lookup"><span data-stu-id="f9960-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 