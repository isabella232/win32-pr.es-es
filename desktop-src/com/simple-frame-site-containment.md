---
title: Contención de sitio de marco simple
description: Contención de sitio de marco simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994081"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="a8ebb-103">Contención de sitio de marco simple</span><span class="sxs-lookup"><span data-stu-id="a8ebb-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="a8ebb-104">Un control contenedor es un control ActiveX que es capaz de contener otros controles.</span><span class="sxs-lookup"><span data-stu-id="a8ebb-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="a8ebb-105">Un cuadro de grupo que contiene una colección de botones de radio es un ejemplo de un control contenedor.</span><span class="sxs-lookup"><span data-stu-id="a8ebb-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="a8ebb-106">Los controles de contenedor deben establecer el \_ bit de estado OLEMISC SIMPLEFRAME y deben llamar a la implementación [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="a8ebb-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="a8ebb-107">Un contenedor de controles ActiveX que admite controles de contenedor debe implementar **ISimpleFrameSite**.</span><span class="sxs-lookup"><span data-stu-id="a8ebb-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="a8ebb-108">CATId-{157083E0-2368-11cf-87B9-00AA006C8166} CATId \_ SimpleFrameControl</span><span class="sxs-lookup"><span data-stu-id="a8ebb-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8ebb-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8ebb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ebb-110">Categorías del componente</span><span class="sxs-lookup"><span data-stu-id="a8ebb-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




