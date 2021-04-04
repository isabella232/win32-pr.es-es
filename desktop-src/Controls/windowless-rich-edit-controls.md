---
title: Controles Rich Edit sin ventanas
description: Esta sección contiene información sobre los elementos de programación utilizados con controles Rich Edit sin ventana.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075326"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="6dc93-103">Controles Rich Edit sin ventanas</span><span class="sxs-lookup"><span data-stu-id="6dc93-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="6dc93-104">Esta sección contiene información sobre los elementos de programación utilizados con controles Rich Edit sin ventana.</span><span class="sxs-lookup"><span data-stu-id="6dc93-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="6dc93-105">El modelo de objetos componentes (COM) define un conjunto de interfaces para admitir objetos sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="6dc93-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="6dc93-106">Los objetos sin ventana pueden entrar en el estado activo en contexto sin tener su propia ventana, sino usar la ventana de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="6dc93-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="6dc93-107">Por lo tanto, un objeto sin ventana utiliza menos recursos del sistema y ofrece un mejor rendimiento a través de una activación y desactivación más rápidas.</span><span class="sxs-lookup"><span data-stu-id="6dc93-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="6dc93-108">Además, los objetos sin ventana pueden ser no rectangulares y transparentes.</span><span class="sxs-lookup"><span data-stu-id="6dc93-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="6dc93-109">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="6dc93-109">Overviews</span></span>



| <span data-ttu-id="6dc93-110">Tema</span><span class="sxs-lookup"><span data-stu-id="6dc93-110">Topic</span></span>                                                                          | <span data-ttu-id="6dc93-111">Contenido</span><span class="sxs-lookup"><span data-stu-id="6dc93-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dc93-112">Acerca de los controles de edición enriquecida sin ventanas</span><span class="sxs-lookup"><span data-stu-id="6dc93-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="6dc93-113">Un control Rich Edit sin ventana, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un [control Rich Edit](rich-edit-controls.md) sin proporcionar la ventana.</span><span class="sxs-lookup"><span data-stu-id="6dc93-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="6dc93-114">Functions</span><span class="sxs-lookup"><span data-stu-id="6dc93-114">Functions</span></span>



| <span data-ttu-id="6dc93-115">Tema</span><span class="sxs-lookup"><span data-stu-id="6dc93-115">Topic</span></span>                                            | <span data-ttu-id="6dc93-116">Contenido</span><span class="sxs-lookup"><span data-stu-id="6dc93-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dc93-117">**CreateTextServices**</span><span class="sxs-lookup"><span data-stu-id="6dc93-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="6dc93-118">La función [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea una instancia de un objeto de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="6dc93-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="6dc93-119">El objeto servicios de texto admite una variedad de interfaces, entre las que se incluyen [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y el modelo de objetos de texto (Tom).</span><span class="sxs-lookup"><span data-stu-id="6dc93-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="6dc93-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="6dc93-120">Interfaces</span></span>



| <span data-ttu-id="6dc93-121">Tema</span><span class="sxs-lookup"><span data-stu-id="6dc93-121">Topic</span></span>                                  | <span data-ttu-id="6dc93-122">Contenido</span><span class="sxs-lookup"><span data-stu-id="6dc93-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dc93-123">**ITextHost**</span><span class="sxs-lookup"><span data-stu-id="6dc93-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="6dc93-124">Un objeto de servicios de texto usa la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) para obtener los servicios de host de texto.</span><span class="sxs-lookup"><span data-stu-id="6dc93-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="6dc93-125">**ITextServices**</span><span class="sxs-lookup"><span data-stu-id="6dc93-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="6dc93-126">Extiende el TOM para proporcionar una funcionalidad adicional para la operación sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="6dc93-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





