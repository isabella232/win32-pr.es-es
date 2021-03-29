---
title: Controles de contenedor
description: Controles de contenedor
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487055"
---
# <a name="container-controls"></a><span data-ttu-id="cdbae-103">Controles de contenedor</span><span class="sxs-lookup"><span data-stu-id="cdbae-103">Container Controls</span></span>

<span data-ttu-id="cdbae-104">Como se describió anteriormente, los controles de contenedor son controles ActiveX que contienen visualmente otros controles.</span><span class="sxs-lookup"><span data-stu-id="cdbae-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="cdbae-105">La arquitectura de controles ActiveX especifica la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar los controles de contenedor.</span><span class="sxs-lookup"><span data-stu-id="cdbae-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="cdbae-106">Los contenedores también pueden admitir controles de contenedor sin admitir **ISimpleFrameSite**, aunque no se puede garantizar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="cdbae-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="cdbae-107">Por esta razón, existe una categoría de componentes para los controles SimpleFrameSite donde se requiere la funcionalidad completa de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="cdbae-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="cdbae-108">Para admitir controles de contenedor sin implementar [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un contenedor de controles ActiveX debe:</span><span class="sxs-lookup"><span data-stu-id="cdbae-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="cdbae-109">Active todos los controles en todo momento.</span><span class="sxs-lookup"><span data-stu-id="cdbae-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="cdbae-110">Reparent los controles contenidos al hWnd del control que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="cdbae-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="cdbae-111">Permanece el elemento primario del control contenedor.</span><span class="sxs-lookup"><span data-stu-id="cdbae-111">Remain the parent of the container control.</span></span>

 

 




